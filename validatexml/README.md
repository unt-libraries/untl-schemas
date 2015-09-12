Validate XML Schema
==============


About
-----

This schema defines what the UNT Libraries considers to be a valid validatexml
instance. validatexml instances represent bags that are scheduled to be validated.
Validating here refers to checking the hashes of the bags. The bags referred to
here use the [BagIt specifications](www.digitalpreservation.gov/documents/bagitspec.pdf).


Requirements
------------

### Namespace ###

The namespace for all elements of a valid validatexml instance must be set to
"http://digital2.library.unt.edu/coda/validatexml/".


### validate ###

This is the root element of a validatexml instance. All the child elements of this
root element are listed below. All are required.


### identifier ###

This is the unique identifier of the bag to be validated.


### last_verified ###

The last date that the bag was validated.


### last_verified_status ###

The status given to the last validation of the bag.


### priority_change_date ###

The date the priority of the bag was last changed.


### priority ###

The current priority in the queue of the bag to be validated.


### server ###

The server on which the bag is located.


Schema
------

The schema can be viewed [here](https://github.com/unt-libraries/xml-schemas/blob/master/validatexml/validatexml.xsd).
