UNIX File Output XML Schema
===========================

About
-----

This schema defines what is considered by the UNT Libraries to be a valid
unix_file_output XML element. This element is a representation of the output
obtained when executing the `file` program on a particular file in a UNIX
shell. This element in no way refers to the actual contents of any particular
file.

Requirements
------------

### Root Element ###
The root element must be `<unix_file_output>`. No attributes are allowed. This
element contains the following 5 required child elements:

* `<identifier>`
* `<version>`
* `<output>`
* `<mimetype>`
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
The `<mimetype>` child element is a string containing the mime-type of the file.

### Magic Location ###
The `<magicLocation>` child element is a string containing the magic location of
the file.

Schema
------

```xml
<?xml version="1.0"?>
<xs:schema xmlns:sx="http://www.w3.org/2001/XMLSchema">

<xs:element name="unix_file_output">
  <xs:complexType>
    <xs:all>
      <xs:element name="identifier" type="xs:string"/>
      <xs:element name="version" type="xs:string"/>
      <xs:element name="output" type="xs:string"/>
      <xs:element name="mimetype" type="xs:string"/>
      <xs:element name="magiclocation" type="xs:string"/>
    </xs:all>
  </xs:complexType>
</xs:element>
```
