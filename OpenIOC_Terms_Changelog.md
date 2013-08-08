# current.iocterms changelog

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

2013-06-04  William Gibb  <william d0t gibb a t mandiant d0t com>

    * Added ProcessItem/SectionList/MemorySection/PEInfo/Exports/DllName

2013-05-14  Tony Dell  <tony d0t dell a t mandiant d0t com>

    * CookieHistoryItem/IsSecure: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * DriverItem/PEInfo/DigitalSignature/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * DriverItem/PEInfo/DigitalSignature/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * DriverItem/PEInfo/Sections/Section/Entropy/CurveData/float: 
    changing from [int] [xs:int] to [float] [xs:string]

    * DriverItem/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * DriverItem/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * FileItem/PEInfo/DigitalSignature/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * FileItem/PEInfo/DigitalSignature/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * FileItem/PEInfo/Sections/Section/Entropy/CurveData/float: 
    changing from [int] [xs:int] to [float] [xs:string]

    * FileItem/PeakCodeEntropy: 
    changing from [int] [xs:int] to [float] [xs:string]

    * FileItem/PeakEntropy: 
    changing from [int] [xs:int] to [float] [xs:string]

    * HookItem/DigitalSignatureHooked/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * HookItem/DigitalSignatureHooked/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * HookItem/DigitalSignatureHooking/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * HookItem/DigitalSignatureHooking/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ProcessItem/SectionList/MemorySection/DigitalSignature/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ProcessItem/SectionList/MemorySection/DigitalSignature/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ProcessItem/SectionList/MemorySection/Injected: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ProcessItem/SectionList/MemorySection/PEInfo/DigitalSignature/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ProcessItem/SectionList/MemorySection/PEInfo/DigitalSignature/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ProcessItem/SectionList/MemorySection/PEInfo/Sections/Section/Entropy/CurveData/float: 
    changing from [int] [xs:int] to [float] [xs:string]

    * RouteEntryItem/IsIPv6: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ServiceItem/pathSignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ServiceItem/pathSignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ServiceItem/serviceDLLSignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * ServiceItem/serviceDLLSignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * TaskItem/ActionList/Action/DigitalSignature/SignatureExists: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * TaskItem/ActionList/Action/DigitalSignature/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * TaskItem/SignatureVerified: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * TaskItem/TriggerList/Trigger/TriggerEnabled: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * UserItem/disabled: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * UserItem/lockedout: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * UserItem/passwordrequired: 
    changing from [string] [xs:string] to [bool] [xs:string]

    * VolumeItem/IsMounted: 
    changing from [string] [xs:string] to [bool] [xs:string]