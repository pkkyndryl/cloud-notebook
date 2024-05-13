# EC2   
Last Updated: {{ git_revision_date_localized }}

![](../images/aws-compute-basics.drawio..svg)

## Some Key Points relative to the picture above
1. There are numerous instance types that can impact the costs. Make sure you understand them. [See this site](https://ec2instances.info)
1. Remember, the `Instance Store` volume may be fast, but you loose the data stored on it when the instance is terminated UNLESS you take action to copy the data somewhere.
1. For example: SCSI disks --> /dev/sda/sda1, /dev/sda/sd2, etc... [more info](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/device_naming.html)
1. But requires the use of a specific command. See the page on EBS & EFS.


__NOTE: You can right click on the image and download it. Each diagram is an SVG file created using DrawIO. That means you can edit the downloaded file with DrawIO__
