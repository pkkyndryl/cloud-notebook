# ipaddress-notes

Standards/Concepts: IP Addressing range standards

* RFC 1918: (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16)
  * https://en.wikipedia.org/wiki/Private\_network Private IPv4 addresses\[edit] The Internet Engineering Task Force (IETF) has directed the Internet Assigned Numbers Authority (IANA) to reserve the following IPv4 address ranges for private networks:[1](p4/) RFC1918 name IP address range Number of addresses Largest CIDR block (subnet mask) Host ID size Mask bits Classful description\[Note 1] 24-bit block 10.0.0.0 – 10.255.255.255 16777216 10.0.0.0/8 (255.0.0.0) 24 bits 8 bits single class A network 20-bit block 172.16.0.0 – 172.31.255.255 1048576 172.16.0.0/12 (255.240.0.0) 20 bits 12 bits 16 contiguous class B networks 16-bit block 192.168.0.0 – 192.168.255.255 65536 192.168.0.0/16 (255.255.0.0) 16 bits 16 bits 256 contiguous class C networks In practice, it is common to subdivide these ranges into smaller subnets.
  *
* RFC6598: Carrier Grade NAT (CGN) addresses
  * https://en.wikipedia.org/wiki/Carrier-grade\_NAT
    * IETF published RFC 6598, detailing a shared address space for use in ISP CGN deployments that can handle the same network prefixes occurring both on inbound and outbound interfaces. ARIN returned address space to the Internet Assigned Numbers Authority (IANA) for this allocation.\[4] The allocated address block is 100.64.0.0/10.\[5]
    * 100.64.0.0/10 is not public.   100.64.0.0/10 = 100.64.0.0–100.127.255.255
* GSNI Routable Addresses
  * Range
    * 129.x; 146.x ; 158.x
* DHCP
  * One means of sharing is dynamic address allocation using DHCP. We assume not all devices on a given network need to be online at the same time, so we lend an address out of a limited pool as a device needs it, and reclaim the address when the device is done with it. The address can then be given to some other needy device. We are statistically multiplexing the address pool.
  *

IP Address Format standards

* IPV6
* IPV4

Key points: Net Net

* There are Internet IP Addresses and Local IP Addresses
  * Local IP addresses are assigned to devices that are not internet accessible. I.e. behind a router
    * These addresses could be duplicated on the internet
    * Think specific identifiers to rooms in a house.
  * Internet IP Addresses are unique on the internet. ( AKA Public IP Address )
    * These need to be registered with
* With a network, no 2 devices can have the same internet address
  * i.e. in a local network each device must have a unique Local IP Address
  * all devices “attached” to the Internet must have a unique Internet IP Address
* To obtain an Internet IP address, or range of addresses, they must be requested from an Internet IP Address Registry.
  * The registry manages the database of Internet IP addresses.
* Private, non-internet accessible networks leverage the RFC 1918 standard
  * Can’t reach the internet if you are not using RFC 1918
  * RFC1918 addresses can be reused in different networks, they are not globally unique
* All messages sent over the internet have a Source IP Address and an Destination IP Address.
  * https://en.wikipedia.org/wiki/IPv4
  * Source IP Address is the address of the source machine ( think return address )
  * Destination IP Address is the target IP Address.. ( where you are sending it to)
* All traffic going from a private to a public network must have Internet IP Addresses for all messages traversing the internet
  * This is because if you only were to use private IP Addresses these can be duplicated on the network and your message may end up somewhere you don’t intend.
* You can go from Private to Internet IP Addresses, but you need to go through a device that implements Network Address Translation ( NAT).
  * There are 2 types of NAT:
    * Source NAT (SNAT ), which changes the source IP address of each message.
      * For private to public traffic the source IP address needs to be changed from a private IP address to an Internet IP Address
    * Destination NAT ( DNAT ) changes the destination IP Address of each message.
      * For messaging coming into a private network from the public network, the destination IP Address has to be something recognizable in the private network
* Carrier Grade IP Addresses: ( aka Large Scale NAT )
  * A defined and reserved range of IP Addresses that can be send over the internet without NATing. \[ VALIDATE ]
  * The allocated address block is 100.64.0.0/10
  * This is what the Platform DRES uses
* IBM Maintains a datacenter and customer network that operates on RFC 6598 Address
  * These are known as GSNI Addresses
  * These can’t reach the internet
* CIDR block

https://www.dummies.com/computers/pcs/what-is-an-ip-address/

https://www.ultratools.com/tools/ipWhoisLookup

Understanding Carrier Grade NAT

Any general-use IP protocol stack that supports IPv6 also supports IPv4. That is, it is dual stack capable. “General-use” is an important qualifier here: Certainly there will be specialized devices that support only IPv6. But these devices – until we get to some unspecified time in the future where IPv4 no longer exists – function in “walled garden” applications such as sensor or control networks that have distinct boundaries and never interact with IPv4. The important significance of dual stacking is that if one of the devices in a two-way conversation can speak both IPv4 and IPv6, it does not matter if the device on the other end is restricted to one or the other version. As long as one of the two speakers is “bilingual,” a conversation can take place.

Dual stacking is therefore the simplest way to begin deploying IPv6. If all the devices in an IPv6-enabled network are dual stacked, they can speak to any destination whether it is IPv4 or IPv6. This is extremely important in the early stages of deployment, when the vast majority of destination content on the public Internet is still IPv4-only. The glaring problem with dual stacking, as I discussed in the previous post, is that the chief reason why we need to begin deploying IPv6 at all is that we are quickly running out of IPv4 addresses. How do you put both an IPv6 address and an IPv4 address on every interface if you have run out of IPv4 addresses?

The fact of the matter is that we actually ran out of globally unique IPv4 addresses a long time ago. You may ask (sounding a little like Tevye), “How can this be? The IANA still has 28 /8 IPv4 address blocks that have not yet been allocated. That’s about 469 million addresses. We have not run out of IPv4 addresses!”

My answer is that we have given ourselves the illusion of having enough IPv4 addresses by nicely sharing the addresses we have. One means of sharing is dynamic address allocation using DHCP. We assume not all devices on a given network need to be online at the same time, so we lend an address out of a limited pool as a device needs it, and reclaim the address when the device is done with it. The address can then be given to some other needy device. We are statistically multiplexing the address pool.

That worked fine in the 1990s, but more and more these days network-connected devices want to be “always on.” That means devices hold on to the addresses they’re given, reducing the number of addresses that can be shared on an as-needed basis.

The other means of sharing globally unique IPv4 addresses, and by far the more successful, is the venerable Network Address Translation (NAT). Specifically NAT44, which translates an IPv4 address to another IPv4 address.  Private (RFC1918) IPv4 addresses are used within a given network; the assumption here being that within a network most IP devices only want to talk to other IP devices in the same network.

But because RFC1918 addresses can be reused in different networks, they are not globally unique. When a device on one network wants to talk to a device in a different administrative domain, reachable across the public Internet, there is no guarantee that the two devices are not using the same address. There is also no way for routers in the public domain to differentiate between networks using the same address blocks.

So we put NAT44 (normally residing either in a router or a firewall) at the edge of the network where it interfaces to the public Internet. The NAT has one or more globally unique IPv4 addresses. and as a packet passes from its inside or private interface to its outside or public interface, NAT replaces the packet’s private IPv4 address with one of its public IPv4 addresses. The NAT “remembers” which inside device the packet came from by mapping the inside address to the outside address.

If NAT44 did no more than I have described so far, it would have the same problem as dynamic address allocation: The pool of available addresses would not scale to the demands of modern networks of “always-on” devices. The assumption that most network-internal devices talk to other network-internal devices most of the time is no longer valid, as more and more data exchanges are across the public Internet.

NAT44 overcomes this scaling problem by using not only its pool of public IPv4 addresses but also the port numbers available with each of the addresses. TCP and UDP headers support up to 65,536 port numbers, most of which are unused. So by mapping an internal \[private address, port] tuple to an outside \[public address, port] tuple, NAT44 is really mapping sessions rather than devices and can support a very large number of sessions with each public address.

This approach has variously been called Network Address and Port Translation (NAPT), Port Address Translation (PAT), address overloading, or IP masquerading in the past. These days it’s just considered a standard function of NAT44. NAT has been around since the early to mid 1990s, when it was one of several short-term solutions (along with DHCP, RFC1918 addresses, and CIDR) created to slow the depletion of IPv4 while a next-generation Internet Protocol – which eventually became IPv6 – was developed. Back then it was just called NAT, not NAT44, because translating an IPv4 address to another IPv4 address was the only option there was. There was no need to distinguish it from, say, NAT64, because IPv6 did not yet exist and so something that could translate between IPv4 and IPv6 did not yet exist either.

Getting back to the dual stack dilemma that service providers face: Why not NAT the IPv4 half of dual stack connections to customers? That gets customers started on IPv6 while still providing IPv4 connectivity.

This is the basis for Carrier Grade NAT (CGN). Traditional NAT – CPE NAT –  appears at the edge of the customer network where it connects to a service provider, and translates between private IPv4 addresses within the customer network and one or a few public addresses assigned by the provider. CGN appears within the service provider network. It, too, translates between private and public IPv4 addresses; the private side of the CGN faces the provider’s customers.

In other words, CGN enables service providers to assign private RFC 1918 IPv4 addresses to their customers rather than public, globally unique IPv4 addresses. Once again NAT comes to the rescue of a dwindling address supply.

It also raises the question: Why not just use CGN and forget about IPv6? I’ll address that question (forgive the pun) in a later post, after we’ve looked further into the various CGN issues and architectural options. The first issue around CGN is the name. There is no real distinction between a CGN and any other NAT, other than the assumption that if it appears in a service provider network it is probably going to be on a carrier class router. But there are no specified qualities that make CGN “carrier grade” in and of itself.

Because nothing really defines the “Carrier Grade” part of CGN, a movement is afoot to change the name to “Large Scale NAT” (LSN). I kicked off this article using the term CGN, because that’s still the term most people are familiar with. But I’m going to pull a switcheroo and use “Large Scale NAT” in subsequent articles, now that I’ve had a chance to explain why the name is changing: LSN better reflects the intent of a NAT that serves a large number of service provider customers, say in a single PoP, and must scale to a massive amount of customer traffic.

Also by taking the “carrier” reference out of the name it better reflects the fact that LSN is a NAT solution that can be used in more than just service provider scenarios. It can be useful in any large-scale network. Apart from the need to scale, the other big issue with LSN is the fact that it is used to assign RFC 1918 addresses to customers, which then use the addresses on the “public” side of their own NATs. Those CPE NATs are then translating from customer-side RFC 1918 addresses to provider-side RFC 1918 addresses. So end-user traffic is now passing through a two-tiered or hierarchical NAT architecture rather than a single device. That architecture, and the issues that arise from having private IPv4 addresses between the LSN and the CPE NATs, are the subjects of my next post.
