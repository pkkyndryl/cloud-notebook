# Remember Forte’ ? ( a look into the past)

__Original blog publish date: May,11 2015__

One of the interesting technologies to emerge in the 90’s was a tool and language called Forte’ from a company of the same name. In the days of client/server and PowerBuilder, this company came out with a enterprise grade product that was aimed at development of complex distributed services solutions.

The company and product, frankly was ahead of it’s time, and it faced the early Java headwinds, but the distributed systems architecture it espoused and enabled did set the stage for the SOA stage that was yet to hit full force and the microservices architecture concepts and techniques that have been emerging recently.

Those of us who were involved in this work recall the “best practice” conversations we had with Paul Butterworth, chief architect.   These included:

1. design for loose coupling.
1. design for subsystems to be deployed and upgraded independently.
1. design large grained components and interfaces. ( this during the heady days of OO ).
1. design subsystems to model the business; don’t do fine grained OO.
1. design for stateless behavior to enable scaling.
1. pass few large messages vs lot’s of smaller messages.
1. have clearly defined interfaces ( now called APIs).
1. Keep the data supporting subsystems loosely coupled to avoid coupling at the database.  ( this caused no end of arguments with the Data Architects … remember this was before NoSQL )

As you can see, these best practices still are relevant in the world of micro services architecture.   This work, and what I learned from it, are reflect in the paper I wrote years back and I’ll be building on this foundation as I get into the next posts.