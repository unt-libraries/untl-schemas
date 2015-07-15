UNIX File Output Schemas
========================

About
-----

These schemas define what are considered by the UNT Libraries to be valid
unixFileOutput XML/JSON. These instances are representations of the output
obtained when executing the `file` program on a particular file in a UNIX
shell.

Requirements
------------

### Root Element ###

#### XML ####
The root element must be `<unixFileOutput>`. The namespace is required to be
set to `http://digital2.library.unt.edu/unixFileOutput.xsd`. This element must
contain the following 5 child elements:

* `<identifier>`
* `<version>`
* `<output>`
* `<mimeType>`
* `<magicLocation>`

Note that these child elements can appear in any order, so long as they all
occur exactly 1 time.

#### JSON ####
The root of the JSON document is an object containing the following keys:

* "identifier":
* "version":
* "output":
* "mimeType":
* "magicLocation":

Note that these keys can appear in any order, so long as they all appear
exactly 1 time.

### Identifier ###
The `identifier` is a string containing the file identifier.

### Version ###
The `version` is a string containing the version of the file program that was
used.

### Output ###
The `output` is a string containing the output obtained when the file program
was run.

### Mime-Type ###
The `mimeType` is a string containing the mime-type of the file.

### Magic Location ###
The `magicLocation` is a string containing the magic location of the file.

Schemas
------

The XML schema can be found
[here](https://github.com/unt-libraries/xml-schemas/blob/master/unixFileOutput/unixFileOutput.xsd).

The JSON schema can be found
[here](https://github.com/unt-libraries/xml-schemas/blob/master/unixFileOutput/unixFileOutput.json).
