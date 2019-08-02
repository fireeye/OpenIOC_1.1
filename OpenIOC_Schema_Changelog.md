# Detailed Changelogs from IOC 1.0

## License

Copyright 2013 Mandiant Corporation.  Licensed under the Apache 2.0 license.  

Mandiant licenses this file to you under the Apache License, Version
2.0 (the "License"); you may not use this file except in compliance with the
License.  You may obtain a copy of the License at:

        http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
implied.  See the License for the specific language governing
permissions and limitations under the License.

## Changes

1. Restructured the XML. OpenIOC now has thee distinct sections

    1. metadata: Description, creator, dates... Metadata that pertains to the entire IOC.

    1. criteria: Everything that used to be `<definition>`. This is the part of the IOC that performs the actual matching.

    1. parameters: Additional section for providing arbitrary metadata on
       specific <Indicator> and <IndicatorItem> elements.

1. Removed IOCs requirement to respect Lucene behaviors.

1. Added additional operators. Including the existing 'is' and 'contains', we
    now have the following: The following operators are expected to perform as
    they are described in XPath 2.0. Also, OpenIOC now respects Bool & Float variables in IOC terms files.

    ```
                   String  Md5sum  IPAddr  Integer DateTime Bool  Float
    is              yes     yes     yes     yes     yes      yes   yes
    contains        yes     no      no      no      no       no    no
    matches         yes     no      yes     no      no       no    no
    starts-with     yes     no      no      no      no       no    no
    ends-with       yes     no      no      no      no       no    no
    greater-than    no      no      no      yes     yes      no    yes
    less-than       no      no      no      yes     yes      no    yes
    ```

1. Moved operator negation out of the operator itself (isnot and containsnot) to its own
    attribute `IndicatorItem/@negate=true|false`.

1. Added case sensitivity `IndicatorItem/@preserve-case=true|false`.

    1. The behavior of `IndicatorItem/@preserve-case` should only apply to strings.  The table below states whether or not the given preserve-case value (true or false) is acceptable for a given content type.

        ```
                       String  Md5sum  IPAddr  Integer DateTime Bool  Float
        true            yes     no      no      no      no       no    no
        false           yes     yes     yes     yes     yes      yes   yes
        ```
        
    1. By default, the `IndicatorItem/@preserve-case` attribute should be set to 'false' when creating a IndicatorItem.

    1. The case sensitivity of a regular expression match, where `IndicatorItem/@condition='matches'`, should be determined by the `IndicatorItem/@preserve-case` term.
    
1. `IndicatorItem/@id` is now a required item. Previously it was not, allowing for Items to not have ids and still validate.
    
1. Added node context `Indicator/@node-context=xs:string`, this will allow for future ability to specify node-context to allow matches that consist of sibling or parent/child nodes that did not evaluate together properly in 1.0.

1. `IndicatorItem/content` and `IndicatorItem/context` are now `minOccurs=1` -- this prevents items from existing without content or without context (this is important now that we allow you to specify context).
    
1. Parameters now have two id attributes: `IOCParameter/@id` is a unique GUID to identify the parameter, and `IOCParameter/@ref-id` is used to show which element inside the IOC that specific parameter refers to.

1. All attributes of parameters are required to keep blank/improper parameters from being created/retained.

1. If you use a Link in the IOC metadata, the `rel` attribute is now required (i.e. there must actually be a link represented in the IOC xml, even if it is empty).

2019-08-02  Matthew Dunwoody  <matthew d0t dunwoody a t mandiant d0t com>

1. Added "platform" field, which contains a comma-delimited list of relevant/supported operating systems, e.g. "win,osx,linux".
