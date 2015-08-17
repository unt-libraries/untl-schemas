Node XML Schema
===============


About
-----

This schema defines what the UNT Libraries considers to be a valid
nodexml instance. A nodexml instance is an XML representation of a
storage node. Specifically, the nodes represented are the storage
nodes for bags, which follow the 
[BagIt](http://www.digitalpreservation.gov/documents/bagitspec.pdf)
format.


Requirements
------------


### Namespace ###

The namespace for all elements of a valid nodexml instance must be set to
"http://digital2.library.unt.edu/coda/nodexml/".


### node ###

This is the root element of a nodexml instance. This root element must contain
a single instance of each of the following child elements:

* name
* url
* path
* capacity
* size
* lastChecked


### name ###

The name of the storage node.


### url ###

The full URL of the storage node.


### path ###

The path on disk of the storage node.


### capacity ###

The total capacity of the storage node in bytes.


### size ###

How much (in bytes) of the capacity is in use.


### lastChecked ###

The last date the node was checked.


Schema
------

The schema can be viewed [here](https://github.com/unt-libraries/xml-schemas/blob/master/nodexml/nodexml.xsd).
