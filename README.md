OpenIOC_1.1
===========

A place to put stuff about OpenIOC 1.1



Major Changes from IOC 1.0:
===========================

1. Restructured the XML. OpenIOC now has thee distinct sections

--metadata
  Description, creator, dates...

--criteria
  Everything that used to be <definition>

--parameters
  Additional section for providing arbitrary metadata on <Indicator> and <IndicatorItem> elements.
    

Removed IOCs requirement to respect Lucene behaviors.

Added additional operators. Including the existing 'is' and 'contains', we now have the following:
The following operators are expected to perform as they are described in XPath 2.0

---------------String  Md5sum  IPAddr  Integer DateTime
is              yes     yes     yes     yes     yes
contains        yes     no      no      no      no
matches         yes     no      yes     no      no
begins-with     yes     no      no      no      no
ends-with       yes     no      no      no      no
greater-than    no      no      no      yes     yes
less-than       no      no      no      yes     yes

Moved operator negation out of the operator itself (isnot) to its own attribute IndicatorItem/@negate=true|false

Added case sensitivity IndicatorItem/@preserve-case=true|false

