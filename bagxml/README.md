Bag XML Schema
==============


Work-In-Progress
----------------

This readme, the schema, and the example document are all still a
work-in-progress. Major changes to all the three documents are expected
to take place.


About
-----

This schema defines what the UNT Libraries considers to be a valid bagxml
instance. A bagxml instance is an XML representation of a bag.


Requirements
------------

### Namespace ###

The namespace for all elements of a valid bagxml instance must be set to
"http://digital2.library.unt.edu/coda/bagxml/".


### codaXML ###

This is the root element of a bagxml instance. This element must contain all the
child elements listed below, with each appearing exactly once, with the exception
of the item grandchild element, which can occur any number of times.


### name ###

The unique ID of the bag.


### fileCount ###

The number of files in the bag.


### payloadSize ###

The total size of the bag payload.


### bagitVersion ###

The version of the bagIt specs being used.


### lastVerified ###

The date of last verification.


### bagInfo ###

The bagInfo element can contain any number of item child elements, which contain
metadata about the bag itself.


#### item ####

An individual metadata 'item'. Must contain the child elements name and body.


##### name #####

The name of the bag metadata item.


##### body #####

The actual metadata.


Schema
------

The schema can be viewed [here](https://github.com/unt-libraries/xml-schemas/blob/master/bagxml/bagxml.xsd).
