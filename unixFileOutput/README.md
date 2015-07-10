UNIX File Output XML Schema
===========================

About
-----

This schema defines what is considered by the UNT Libraries to be a valid
unixFileOutput XML element. This element is a representation of the output
obtained when executing the `file` program on a particular file in a UNIX
shell. This element in no way refers to the actual contents of any particular
file.

Requirements
------------

### Root Element ###
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

### Identifier Element ###
The `<identifier>` child element is a string containing the file identifier.

### Version Element ###
The `<version>` child element is a string containing the version of the file
program that was used.

### Output ###
The `<output>` child element is a string containing the output obtained when the
file program was run.

### Mime-Type Element ###
The `<mimeType>` child element is a string containing the mime-type of the file.

### Magic Location ###
The `<magicLocation>` child element is a string containing the magic location of
the file.

Schema
------

The actual schema can be found
[here](https://github.com/unt-libraries/xml-schemas/blob/master/unixFileOutput/unixFileOutput.xsd).
