Bag XML Schema
==============


About
-----

This schema defines what the UNT Libraries considers to be a valid bagxml
instance. A bagxml instance is an XML representation of a bag, as defined
by the BagIt specification
[here](http://www.digitalpreservation.gov/documents/bagitspec.pdf).


Requirements
------------

### Namespace ###

The namespace for all elements of a valid bagxml instance must be set to
"http://digital2.library.unt.edu/coda/bagxml/".


### codaXML ###

This is the root element of a bagxml instance. All the child elements of this
root element are listed below. All are required.


### name ###

The unique ID of the bag.


### fileCount ###

The number of files in the bag.


### payloadSize ###

The total size of the bag payload.


### bagitVersion ###

The version of the bagIt specification being used.


### lastVerified ###

The date of last verification.


### lastStatus ###

The last status of the bag. Can only be one of the following options:

* 'pass'
* 'fail'


### baggingDate ###

The date the bag was created.


### bagInfo ###

The bagInfo element can contain any number of item child elements, which contain
metadata about the bag itself.


#### item ####

An individual metadata 'item'. Must contain the following child elements:

* name
* body

This element can appear more than once.


##### name #####

The name of the bag metadata item.


##### body #####

The actual metadata.


Schema
------

The schema can be viewed [here](https://github.com/unt-libraries/xml-schemas/blob/master/bagxml/bagxml.xsd).
