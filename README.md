# OpenIOC 1.1 DRAFT -- README

## Authors:

Copyright 2013 Mandiant Corporation.  Licensed under the Apache 2.0
license.  Developed for Mandiant by:


David Ross
Jason Shiffer
Tony Dell
William Gibb
Doug Wilson

correspondence for the authors may be sent to openioc A T mandiant D O T com


## License

The documents in this repository are made available under the terms of the
Apache License , Version 2.0. See the "LICENSE " file for more information.

## Description

This repository contains a revised schema, iocterms file, and other supporting
documents which are the basis for a draft of a revised version of OpenIOC that we are
calling OpenIOC 1.1.

The updated OpenIOC 1.1 schema and a changelog are included. That changelog
details the changes in schema from OpenIOC 1.0. An updated set of iocterms
are included, as well as definitions of what selected commonly used terms mean.

We are publishing this draft as a means of garnering public comment. If you are
interested in commenting, please contact one of the authors, or join the OpenIOC
google group at https://groups.google.com/forum/#!forum/openioc 

A utility for working with OpenIOC 1.1 programmatically has been released at
https://github.com/mandiant/ioc_writer - Please go to that URL for more info.

An experimental version of the IOC Editor has been created for working with
OpenIOC 1.1. Please contact one of the authors if you are interested in
obtaining a copy of this tool.

## What's new in OpenIOC 1.1?

A quick rundown of some of the changes:

An IOC under OpenIOC 1.1 has three distinct sections.

    1. Metadata - the traditional metadata header that contains metadata about
       the entire Indicator

    2. Criteria - the "matching" section -- a boolean logical evaluation that
       determines whether or not you have found evil, as defined by this specific 
       indicator.

    3. Parameters - This section is entirely new, although it houses the "comments"
       from OpenIOC 1.0 among other things. Parameters are assignable metadata,
       that can be applied to any element in the Criteria section of the IOC. The
       significance of the Parameters section will be discussed later.
    
We've moved away from unexpected behavior of operators that were due to OpenIOC 1.0
respecting Lucene. OpenIOC is usually used to generate Xpath expressions to query
data sources, so OpenIOC 1.1 operators behave as the would in Xpath 2.0. Please see the
changelog to see what operators we support.

In respecting Xpath operators, OpenIOC now supports regular expressions with the
"matches" operator. This feature is one that is still being heavily tested for
potential pros and cons. Additionally, negation now works the way that most users
will expect.

## The Parameters Section

Parameters are metadata that can be assigned to any specific object within the
Criteria of an IOC. This may not sound like much, but it allows for application
specific logic or controls to be applied to an IOC, without muddying up the schema for
the matching or needing to be interwoven with the criteria section.

We've had many requests to add in various features that may only be of interest to
certain groups or industries, such as confidence scoring, release-to/data control
markings, sequences, and other features. Trying to build all of these in and allow
for all cases would create a schema bloated with features that are not fully fleshed
out yet, and that not everyone needs.

Parameters can be used to apply application or organization specific logic that can
then be passed along with the IOC, or restricted inside of a sharing boundary as
the creator sees fit.

With parameters, we are basically allowing folks to "roll their own" on some of the
features they want that are not included yet. We envision this as a test-ground for
new ideas and features -- and, if something seems to work well and be universally
needed, we can then consider adopting it into schema. Some ideas will just work
better living outside the matching/criteria section as parameters no matter what.

We feel that this solution allows flexibility and customization for different
organizational needs and workflows, while still providing for the standardization
needed for the Criteria section.

## Per file descriptions

schemas/ioc.xsd - This is the XML schema document for OpenIOC 1.1.

OpenIOC_Schema_Changelog.md - This is a changelog for changes between
        OpenIOC 1.0 and OpenIOC 1.1.

iocterms/current.iocterms - This is a .iocterms file, containing a list of IOC
        Terms. This file can that can be used in the Windows IOC editor, IOCe.

OpenIOC_Terms_Changelog.md - This is a changlog for the current.iocterms file.

IOC_Terms_Defs.md - This document provides definitions and examples for what
        some of the most commonly used IOC terms mean.

## Files which are licensed under the Apache 2.0 License 

(see the LICENSE file for more information):

    Title                   Filename
    =====                   ========
    OpenIOC 1.1 Schema      schemas/ioc.xsd
    Schema changelog        OpenIOC_Schema_Changelog.md
    .iocterms file          iocterms/current.iocterms
    iocterms changelog      OpenIOC_Terms_Changelog.txt
    IOC Terms Definitions   IOC_Terms_Defs.md
