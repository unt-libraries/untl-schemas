.. -*- coding: utf-8 -*-

=================================================
UNTL Descriptive Metadata Definition: Version 3.0
=================================================

:Authors: Daniel G. Alemneh & Mark E. Phillips
:Date: 2009-02-05
:Version: 3.01
:Copyright: This document has been placed in the public domain.

.. contents::
.. sectnum::

This is work in progress, it should be read as such.


Overview
========
The University of North Texas Libraries (UNTL) actively promote metadata-based digital resource management.  The UNT Libraries' Digital Projects Unit monitors national and international standards-related activities and conducts research into the theoretical and practical applications of metadata, creating a detailed schema to facilitate consistency among departments and institutions participating in collaborative digital projects.  This document empowers metadata creators to describe digital objects in a consistent way that ensures long-term access.

The UNT Libraries' metadata element set comprises Dublin Core-based descriptive metadata and detailed technical and preservation information recording how digital resources are identified, created, formatted, arranged in relevant software applications, and sustained with application of appropriate preservation procedures.  While promoting interoperability with widely accepted standards, the recommended UNT Libraries' metadata elements allow flexibility at the local level to integrate with existing and anticipated content, processes, and systems.

The UNT Libraries' Metadata Initiative progressed on many fronts.  This (version-3.0) guideline is a product of a series of revision activities.  Version-3.0 is indeed a major revision of the UNTL metadata guidelines that offers many new and improved features, including major changes in the handling of sub-elements and qualifiers or refinements.  It should be noted that in order to comply with evolving internal and external requirements, the UNT Libraries' metadata creation guideline will remain under continuous review.

An older version of the specification of all UNTL metadata elements and related maintenance activities, including element refinements, mapping, and controlled terms, available at: http://www.library.unt.edu/digitalprojects/metadata

If you have any comments or suggestions regarding the metadata elements, please contact Daniel Gelaw Alemneh at daniel.alemneh@unt.edu.


Element Reference Guide
-----------------------

Properties of the UNTL data dictionary descriptions:

:Element: Name of element that is used in the machine-readable encoded document.
:Label: Human-friendly version of the element name.  The full name of the element is usually a word or phrase that identifies the element's purpose.  In the tag library, the element name follows the tag name on the page defining that element and appears with initial capital letters.
:Sub Elements: Sub-elements an element has.  If an element lists its sub-elements, each sub-element has its own entry and gets the same treatment as an element in its description.
:Definition: A brief statement that represents or defines the element.
:Comment: Additional information about the element, including intended use or how values may be obtained.
:Obligation: Indicates whether or not the element value is mandatory: "Required" or "Not required".
:Repeatability: Indicates whether or not the element can take multiple values: "Repeatable" or "Not repeatable".
:Data Type: Indicates what values the element can take: "String", "Boolean", or "Date/Time".
:Data Constraint: Indicates how the values should be encoded, i.e. whether the element value should be taken from a controlled vocabulary, or if it can take any form.
:Qualifier: Further refinements that allow for more precision about what an element means.


Top Level Elements
==================


Title
-----

:Element: title
:Label: Title
:Sub Elements: None
:Definition: The name given to the resource.
:Comment: This element will record the name given to the resource at the individual file (document) level.  Typically, a title will be a name by which the resource is formally known.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/title-qualifiers/


Creator
--------

:Element: creator
:Label: Creator
:Sub Elements: type_, name_, info_
:Definition: The creator is the person, agency, or organization primarily responsible for creating the intellectual content of the resource.
:Comment: Use the creator element to describe the maker at the object level.  Examples are author, editor, sculptor, photographer, composer, etc.  Multiple creators may be associated with the same digital object.  For the maker of a collection, or a lesser contributor to an individual object, use the Contributor element instead.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/agent-qualifiers/


Contributor
-----------

:Element: contributor
:Label: Contributor
:Sub Elements: type_, name_, info_
:Definition: The contributor is the person, agency, or organization that has played an important but secondary role in creating the content of the resource and is not specified in the creator element.
:Comment: Use the contributor element to describe the maker of a collection, or a lesser contributor to an individual object.  Examples are collector, donor, transcriber, printer, etc.  Multiple contributors may be associated with the same digital object.  For the primary maker at the object level, use the Creator element instead.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/agent-qualifiers/


Publisher
---------

:Element: publisher
:Label: Publisher
:Sub Elements: location_, name_, info_
:Definition: The publisher is an entity responsible for making the resource available.
:Comment: Typically, the name of a publisher should be used to indicate the entity.  A publisher may be a business, an organization, a service, a government agency, or, rarely, a person.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: None


Date
----

:Element: date
:Label: Date
:Sub Elements: None
:Definition: Dates associated with events in the life cycle of the resource.
:Comment: As defined in a profile of ISO 8601 [W3CDTF], follows the YYYY-MM-DD format.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: Date/Time
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/date-qualifiers/


Language
--------

:Element: language
:Label: Language
:Sub Elements: None
:Definition: The language(s) of the intellectual content of the resource.
:Comment: This will be the language(s) in which a text is written or the spoken language(s) of audio or video.  Visual images normally do not have a language unless there is significant text in a caption or in the image itself.  Because of the global nature of the Internet, use of this field is recommended.  Preferred usage is to utilize a standard schema for language names as defined by ISO639-2 (three-letter language codes), followed optionally by a two-letter country code (taken from the ISO 3166 standard).
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: http://purl.org/NET/UNTL/vocabularies/languages/
:Qualifier: None


Description
-----------

:Element: description
:Label: Description
:Sub Elements: None
:Definition: Both content and physical descriptions of the resource.
:Comment: Content description may include but is not limited to: an abstract, table of contents, reference to a graphical representation of content, or a free-text account of the content.  Physical description will be used for physical dimensions, extent, pagination, process (tintype, daguerreotype, woodcut, etc.), and related physical details of the original item.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/description-qualifiers/


Subject-Keyword
---------------

:Element: subject
:Label: Subject-Keyword
:Sub Elements: None
:Definition: The subject or topic of the resource that succinctly describes the content of the resource.  It is expressed by headings, keywords, phrases, or names; or terms for significantly associated people, places, events, etc.
:Comment: Typically, a subject will be expressed as keywords, key phrases, or defined headings that describe the topic of the resource.  In order to facilitate browsing in the Portal, at least one subject must be chosen from the UNTL Browse Subjects list.  Recommended best practice is to select additional values from a controlled vocabulary.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: Partly constrained by: [http://purl.org/NET/UNTL/subjects/]
:Qualifier: http://purl.org/NET/UNTL/vocabularies/subject-qualifiers/


Coverage
--------

:Element: coverage
:Label: Coverage
:Sub Elements: None
:Definition: The spatial and/or temporal characteristics of the intellectual content of the resource.
:Comment: Coverage is the extent or scope of the content of the resource.  It will typically include spatial location (a place name or geographic coordinates) and a temporal period (a period label, date, or date range).
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: Partially constrained by the following controlled vocabularies: [http://purl.org/NET/UNTL/vocabularies/coverage-eras/]
:Qualifier: http://purl.org/NET/UNTL/vocabularies/coverage-qualifiers/


Source
------

:Element: source
:Label: Source
:Sub Elements: None
:Definition: Information about a resource from which the current resource is derived.
:Comment: This element can be used to describe the original (physical or digital) resource from which the current digital resource is derived.  The present resource may be derived from the source resource in whole or in part.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/sourceQualifiers/


Relation
--------

:Element: relation
:Label: Relation
:Sub Elements: None
:Definition: Information about another resource that is related to the current resource.  It includes an expression of the relationship type.
:Comment: Relation is simply a reference to a related resource.  It is essential to maintaining a history of the change of a related digital resource.  It specifies any other information resources, which were judged to be significantly related to the digital resource being described and necessary for preservation management.  It also enables a digital resource to be linked to earlier or later versions/editions of it, other forms of it, to its metadata, and other objects, including finding aids.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/relation-qualifiers/


Collection
----------

:Element: collection
:Label: Collection
:Sub Elements: None
:Definition: Collection name refers to a larger group of resources with a unique collective title to which the resource being described belongs.
:Comment: Use the drop-down list to select a controlled collection name.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: http://purl.org/NET/UNTL/vocabularies/collections/
:Qualifier: None


Institution
-----------

:Element: institution
:Label: Institution
:Sub Elements: None
:Definition: A consistent reference to the institution or administrative unit that owns the digital resource for which metadata was created.
:Comment: Use the drop-down list to select a controlled institution name.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: http://purl.org/NET/UNTL/vocabularies/institutions/
:Qualifier: None


Rights
------
:Element: rights
:Label: Rights
:Sub Elements: None
:Definition: Rights information provides complete information about rights held in and over the resource.  Describes the conditions under which the work may be used, distributed, reproduced, etc., how these conditions may change over time, and whom to contact regarding the copyright of the work.
:Comment: Access describes the level of access that the resource is allowed.  License represents rights of license associated with the resources.  Rights holder is the one who holds the license/rights to the resources.  Rights statement provides statement or a link to a detailed statement of the rights for the resource.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: Partly constrained by: [http://purl.org/NET/UNTL/vocabularies/rights-access] and [http://purl.org/NET/UNTL/vocabularies/rights-licenses/].
:Qualifier: http://purl.org/NET/UNTL/vocabularies/rights-qualifiers/


Resource Type
-------------

:Element: resourceType
:Label: Resource Type
:Sub Elements: None
:Definition: The type or category of the primary content of the resource.
:Comment: To be selected from a controlled list.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: http://purl.org/NET/UNTL/vocabularies/resource-types/
:Qualifier: None


Format
------

:Element: format
:Label: Format
:Sub Elements: None
:Definition: The digital manifestation of the resource.
:Comment: To be selected from a controlled list.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: http://purl.org/NET/UNTL/vocabularies/formats/
:Qualifier: None


Identifier
----------

:Element: identifier
:Label: Identifier
:Sub Elements: None
:Definition: A unique identifier or "permanent name" for a resource that identifies it uniquely and persistently.
:Comment: Recommended best practice is to identify the resource by means of a string or number conforming to a formal identification system.  An identifier for an object that identifies it uniquely, enables links to metadata about it, and to other objects related to it.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/identifier-qualifiers/


Note
----

:Element: note
:Label: Note
:Sub Elements: None
:Definition: The note element will serve as a "catch-all" field for additional information that facilitates discovery of the resource, but cannot be entered in other elements.
:Comment: None
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/note-qualifiers/


Degree Information
------------------

:Element: degree
:Label: Degree Information
:Sub Elements: None
:Definition: Degree information provides detail information associated with the work as it appears within the work.
:Comment: None
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: Partly constrained by: [http://purl.org/NET/UNTL/vocabularies/degree-levels/]
:Qualifier: http://purl.org/NET/UNTL/vocabularies/degree-information/


Citation Information
------------------

:Element: citation
:Label: Citation Information
:Sub Elements: None
:Definition: Citation information related to the object being described.
:Comment: None
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/citationQualifiers/


Metadata Information
--------------------

:Element: meta
:Label: Metadata Information
:Sub Elements: None
:Definition: The metadata information entity records information about the metadata creation and the history of changes made, including: by whom: (name of the person doing the creation/revision), when: (date/time that the creation and/or change to the metadata information was completed).
:Comment: This is actually an automated process.  However, if information on changes to the metadata needed to be recorded, metadata modification action should be recorded in the Note (non-display) area.  Recording information about changes to the metadata record underscores the importance of the metadata record itself as a component of the digital object that requires continuous management over time.
:Obligation: Not required
:Repeatability: Repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: http://purl.org/NET/UNTL/vocabularies/meta-qualifiers/


Primary Source
--------------

:Element: primarySource
:Label: Primary Source
:Sub Elements: None
:Definition: Material giving a firsthand account of a historical subject.
:Comment: Primary sources give a firsthand account of a historical subject.  They include materials such as diaries, letters, maps, memoirs, newspapers, oral histories, photographs, and pictures.  Secondary sources are descriptions of a subject based on primary sources.  It is possible that the same document can be a primary source in one aspect, and secondary in another.
:Obligation: Not required
:Repeatability: Not Repeatable
:Data Type: Boolean
:Data Constraint: [0, 1] (0=False, 1=True)
:Qualifier: None


Sub Elements
============

Sub elements add the ability to further describe specific metadata elements.

type
----

:Element: type
:Label: Type
:Sub Elements: None
:Definition: Used to designate if a creator or contributor is an individual or an organization.
:Comment: None
:Obligation: Not required
:Repeatability: Not repeatable
:Data Type: String
:Data Constraint: per, org, event
:Qualifier: None


name
----

:Element: name
:Label: Name
:Sub Elements: None
:Definition: The name of a person, organization, or event (conference, meeting, etc.) associated in some way with the resource.
:Comment: None
:Obligation: Required
:Repeatability: Not repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: None


info
----

:Element: info
:Label: Info
:Sub Elements: None
:Definition: Contains facts about the name_.
:Comment: This sub-element extends the creator, contributor, and publisher element by providing further information about the entity primarily responsible for making the content of the resource.  Any qualifiers such as dates, title, fuller form of name, other form of name, corporate names, contact (email and physical) addresses, jurisdiction, etc. can be recorded in this field.  Because creator information is a displayed field, care should be taken with formulating the text, and it should not be used for sensitive personal information such as the unpublished phone number or home address of a donor.
:Obligation: Not required
:Repeatability: Not repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: None


location
--------

:Element: location
:Label: Location
:Sub Elements: None
:Definition: The place of publication of the original work.
:Comment: None
:Obligation: Not required
:Repeatability: Not repeatable
:Data Type: String
:Data Constraint: None
:Qualifier: None
