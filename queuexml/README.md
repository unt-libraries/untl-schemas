Queue XML Schema
================


About
-----

This schema defines what the UNT Libraries considers to be a valid queuexml instance.
A queuexml instance is an XML representation of a queue of
[bags](http://www.digitalpreservation.gov/documents/bagitspec.pdf) that are waiting to
be harvested.


Requirements
------------

### Namespace ###

The namespace for all elements of a valid queuexml instance must be set to
"http://digital2.library.unt.edu/coda/queuexml/".


### queueEntry ###

This is the root element of a queuexml instance.  All the child elements of this root
element are listed below.


### ark ###

The bag's unique identifier.


### oxum ###

The payload-oxum of the bag. This follows the form of `num_bytes.num_files`. For instance,
a bag that has a total size of 245189 8-bit bytes and a total of 35 files, would have an
oxum of `245189.35`.


### urlListLink ###




### status ###

The ingestion status of the bag, expressed as an integer.


### start ###

The datetime that indicates when the ingestion was started.


### end ###

The datetime that indicates when the ingestion was completed.


### position ###

The 1-based position in the queue.


Schema
------

The schema can be viewed [here](https://github.com/unt-libraries/xml-schemas/blob/master/queuexml/queuexml.xsd).
