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
root element are listed below.


### name ###

The unique ID of the bag.

* Required: yes
* Count: 1


### fileCount ###

The number of files in the bag.

* Required: yes
* Count: 1


### payloadSize ###

The total size of the bag payload.

* Required: yes
* Count: 1


### bagitVersion ###

The version of the bagIt specification being used.

* Required: yes
* Count: 1


### lastVerified ###

The date of last verification.

* Required: yes
* Count: 1


### lastStatus ###

The last status of the bag.

* Required: no
* Count: 0 or 1


### baggingDate ###

The date the bag was created.

* Required: no
* Count: 0 or 1


### bagInfo ###

The bagInfo element can contain any number of item child elements, which contain
metadata about the bag itself.

* Required: yes
* Count: 1


#### item ####

An individual metadata 'item'. Must contain the child elements name and body.

* Required: yes
* Count: 1 or more


##### name #####

The name of the bag metadata item.

* Required: yes
* Count: 1


##### body #####

The actual metadata.

* Required: yes
* Count: 1


Schema
------

The schema can be viewed [here](https://github.com/unt-libraries/xml-schemas/blob/master/bagxml/bagxml.xsd).
