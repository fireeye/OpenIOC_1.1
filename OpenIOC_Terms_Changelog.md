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

2019-08-02  Matthew Dunwoody  <matthew d0t dunwoody a t mandiant d0t com>

    * Updated term titles to reflect level of support (unsupported, deprecated) and supported operating systems 
    (where not supported on all of Windows, OSX and Linux) in FireEye Endpoint Security
    * Updated term-source for FireEye terms from "application/vnd.mandiant.mir" to "application/vnd.fireeye.endpoint"
    * Added DnsEntryItem/RecordData/PrimaryServerName
    * Added DnsEntryItem/RecordData/AdministratorName
    * Added DnsEntryItem/RecordData/SerialNumber
    * Added DnsEntryItem/RecordData/Refresh
    * Added DnsEntryItem/RecordData/Refresh
    * Added DnsEntryItem/RecordData/Retry
    * Added DnsEntryItem/RecordData/Retry
    * Added DnsEntryItem/RecordData/Expire
    * Added DnsEntryItem/RecordData/Expire
    * Added DnsEntryItem/RecordData/DefaultTimeToLive
    * Added DnsEntryItem/RecordData/DefaultTimeToLive
    * Added DnsEntryItem/RecordData/MailboxName
    * Added DnsEntryItem/RecordData/MailboxErrorsName
    * Added DnsEntryItem/RecordData/MxHost
    * Added DnsEntryItem/RecordData/Preference
    * Added DnsEntryItem/RecordData/String
    * Added DnsEntryItem/RecordData/Blob
    * Added DnsEntryItem/RecordData/IPv6Address
    * Added DnsEntryItem/RecordData/Algorithm
    * Added DnsEntryItem/RecordData/Protocol
    * Added DnsEntryItem/RecordData/KeyFlags
    * Added DnsEntryItem/RecordData/Signer
    * Added DnsEntryItem/RecordData/TypeCovered
    * Added DnsEntryItem/RecordData/LabelCount
    * Added DnsEntryItem/RecordData/OriginalTimeToLive
    * Added DnsEntryItem/RecordData/ExpirationDate
    * Added DnsEntryItem/RecordData/DateSigned
    * Added DnsEntryItem/RecordData/KeyTag
    * Added DnsEntryItem/RecordData/AddressType
    * Added DnsEntryItem/RecordData/ATMAddress
    * Added DnsEntryItem/RecordData/NextHost
    * Added DnsEntryItem/RecordData/Type
    * Added DnsEntryItem/RecordData/TargetHost
    * Added DnsEntryItem/RecordData/Priority
    * Added DnsEntryItem/RecordData/Weight
    * Added DnsEntryItem/RecordData/Port
    * Added DnsEntryItem/RecordData/Order
    * Added DnsEntryItem/RecordData/Flags
    * Added DnsEntryItem/RecordData/Services
    * Added DnsEntryItem/RecordData/RegularExpression
    * Added DnsEntryItem/RecordData/Replacement
    * Added DnsEntryItem/RecordData/DigestType
    * Added DnsEntryItem/RecordData/DigestLength
    * Added DnsEntryItem/RecordData/Digest
    * Added DnsEntryItem/RecordData/KeyLength
    * Added DnsEntryItem/RecordData/PublicKey
    * Added DnsEntryItem/RecordData/KeyName
    * Added DnsEntryItem/RecordData/Key
    * Added DnsEntryItem/RecordData/CreationDate
    * Added DnsEntryItem/RecordData/Error
    * Added DnsEntryItem/RecordData/Mode
    * Added DnsEntryItem/RecordData/SignatureLength
    * Added DnsEntryItem/RecordData/Signature
    * Added DnsEntryItem/RecordData/FudgeTime
    * Added DnsEntryItem/RecordData/OriginalXid
    * Added DnsEntryItem/RecordData/MappingFlag
    * Added DnsEntryItem/RecordData/WinsServerIPv4Address
    * Added DnsEntryItem/RecordData/LookupTimeout
    * Added DnsEntryItem/RecordData/CacheTimeout
    * Added DnsEntryItem/RecordData/Bitmask
    * Added DnsEntryItem/RecordData/Data
    * Added RouteEntryItem/ValidLifetime
    * Added RouteEntryItem/PreferredLifetime
    * Added RouteEntryItem/IsLoopback
    * Added RouteEntryItem/IsAutoconfigureAddress
    * Added RouteEntryItem/IsPublish
    * Added RouteEntryItem/IsImmortal
    * Added RouteEntryItem/Origin
    * Added RouteEntryItem/Flags
    * Added RouteEntryItem/MTU
    * Added SudoLogItem/timestamp
    * Added SudoLogItem/ModifiedTimestamp
    * Added SudoLogItem/suOrSudo
    * Added SudoLogItem/username
    * Added SudoLogItem/tty
    * Added SudoLogItem/pwd
    * Added SudoLogItem/userExecuteAs
    * Added SudoLogItem/command
    * Added SudoLogItem/success
    * Added SudoLogItem/SourceLog
    * Added FileItem/PEInfo/Sections/Section/Entropy/AverageValue
    * Added ProcessItem/SectionList/MemorySection/PEInfo/ImportedModules/Module/NumberOfFunctions
    * Added ProcessItem/SectionList/MemorySection/MemD5
    * Added RegistryItem/SecurityID
    * Added FileItem/Group
    * Added FileItem/GroupID
    * Added FileItem/Permissions
    * Added FileItem/PEInfo/Sections/Section/Entropy/AverageValue
    * Added FileItem/PEInfo/DigitalSignature/CertificateChain
    * Added FileItem/DigitalSignature/SignatureExists
    * Added FileItem/DigitalSignature/SignatureVerified
    * Added FileItem/DigitalSignature/CertificateSubject
    * Added FileItem/DigitalSignature/CertificateIssuer
    * Added FileItem/DigitalSignature/CertificateChain
    * Added FileItem/DigitalSignature/Description
    * Added PersistenceItem/FileItem/Md5sum
    * Added PersistenceItem/FileItem/StreamList/Stream/Md5sum
    * Added PersistenceItem/ServiceItem/pathmd5sum
    * Added PersistenceItem/ServiceItem/serviceDLLmd5sum
    * Added PersistenceItem/md5sum
    * Added PersistenceItem/pathAttributes/md5sum
    * Added PersistenceItem/pathmd5sum
    * Added PersistenceItem/serviceDLLmd5sum
    * Added PersistenceItem/FileItem/Sha1sum
    * Added PersistenceItem/FileItem/StreamList/Stream/Sha1sum
    * Added PersistenceItem/ServiceItem/pathsha1sum
    * Added PersistenceItem/ServiceItem/serviceDLLsha1sum
    * Added PersistenceItem/sha1sum
    * Added PersistenceItem/pathAttributes/sha1sum
    * Added PersistenceItem/pathsha1sum
    * Added PersistenceItem/serviceDLLsha1sum
    * Added PersistenceItem/FileItem/Sha256sum
    * Added PersistenceItem/FileItem/StreamList/Stream/Sha256sum
    * Added PersistenceItem/ServiceItem/pathsha256sum
    * Added PersistenceItem/ServiceItem/serviceDLLsha256sum
    * Added PersistenceItem/sha256sum
    * Added PersistenceItem/pathAttributes/sha256sum
    * Added PersistenceItem/pathsha256sum
    * Added PersistenceItem/serviceDLLsha256sum
    * Added PersistenceItem/FileItem/PEInfo/Type
    * Added PersistenceItem/FileItem/PEInfo/Subsystem
    * Added PersistenceItem/FileItem/PEInfo/BaseAddress
    * Added PersistenceItem/FileItem/PEInfo/PETimeStamp
    * Added PersistenceItem/FileItem/PEInfo/PEChecksum/PEFileRaw
    * Added PersistenceItem/FileItem/PEInfo/PEChecksum/PEFileAPI
    * Added PersistenceItem/FileItem/PEInfo/PEChecksum/PEComputedAPI
    * Added PersistenceItem/FileItem/PEInfo/ExtraneousBytes
    * Added PersistenceItem/FileItem/PEInfo/Sections/NumberOfSections
    * Added PersistenceItem/FileItem/PEInfo/Sections/ActualNumberOfSections
    * Added PersistenceItem/FileItem/PEInfo/Sections/Section/Name
    * Added PersistenceItem/FileItem/PEInfo/Sections/Section/Type
    * Added PersistenceItem/FileItem/PEInfo/Sections/Section/SizeInBytes
    * Added PersistenceItem/FileItem/PEInfo/Sections/Section/DetectedCharacteristics
    * Added PersistenceItem/FileItem/PEInfo/Sections/Section/Entropy/AverageValue
    * Added PersistenceItem/FileItem/PeakEntropy
    * Added PersistenceItem/FileItem/PeakCodeEntropy
    * Added PersistenceItem/FileItem/PEInfo/ImportedModules/Module/Name
    * Added PersistenceItem/FileItem/PEInfo/ImportedModules/Module/NumberOfFunctions
    * Added PersistenceItem/FileItem/PEInfo/ImportedModules/Module/ImportedFunctions/string
    * Added PersistenceItem/FileItem/PEInfo/Exports/ExportsTimeStamp
    * Added PersistenceItem/FileItem/PEInfo/Exports/NumberOfFunctions
    * Added PersistenceItem/FileItem/PEInfo/Exports/NumberOfNames
    * Added PersistenceItem/FileItem/PEInfo/Exports/DllName
    * Added PersistenceItem/FileItem/PEInfo/Exports/ExportedFunctions/string
    * Added PersistenceItem/FileItem/PEInfo/DetectedAnomalies/string
    * Added PersistenceItem/FileItem/PEInfo/DetectedEntryPointSignature/Name
    * Added PersistenceItem/FileItem/PEInfo/DetectedEntryPointSignature/Type
    * Added PersistenceItem/FileItem/PEInfo/Sections/Section/DetectedSignatureKeys/string
    * Added PersistenceItem/FileItem/PEInfo/EpJumpCodes/Depth
    * Added PersistenceItem/FileItem/PEInfo/EpJumpCodes/Opcodes
    * Added PersistenceItem/FileItem/PEInfo/DigitalSignature/SignatureExists
    * Added PersistenceItem/FileItem/PEInfo/DigitalSignature/SignatureVerified
    * Added PersistenceItem/FileItem/PEInfo/DigitalSignature/Description
    * Added PersistenceItem/FileItem/PEInfo/DigitalSignature/CertificateIssuer
    * Added PersistenceItem/FileItem/PEInfo/DigitalSignature/CertificateSubject
    * Added PersistenceItem/ServiceItem/pathSignatureExists
    * Added PersistenceItem/ServiceItem/pathSignatureVerified
    * Added PersistenceItem/ServiceItem/pathSignatureDescription
    * Added PersistenceItem/ServiceItem/pathCertificateSubject
    * Added PersistenceItem/ServiceItem/pathCertificateIssuer
    * Added PersistenceItem/ServiceItem/serviceDLLCertificateSubject
    * Added PersistenceItem/ServiceItem/serviceDLLCertificateIssuer
    * Added PersistenceItem/ServiceItem/serviceDLLSignatureExists
    * Added PersistenceItem/ServiceItem/serviceDLLSignatureVerified
    * Added PersistenceItem/ServiceItem/serviceDLLSignatureDescription
    * Added PersistenceItem/SignatureExists
    * Added PersistenceItem/SignatureVerified
    * Added PersistenceItem/SignatureDescription
    * Added PersistenceItem/CertificateSubject
    * Added PersistenceItem/CertificateIssuer
    * Added PersistenceItem/DigitalSignature/SignatureExists
    * Added PersistenceItem/DigitalSignature/SignatureVerified
    * Added PersistenceItem/DigitalSignature/CertificateSubject
    * Added PersistenceItem/DigitalSignature/CertificateIssuer
    * Added PersistenceItem/DigitalSignature/CertificateChain
    * Added PersistenceItem/DigitalSignature/Description
    * Added PersistenceItem/FileItem/PEInfo/ResourceInfoList/ResourceInfoItem/Name
    * Added PersistenceItem/FileItem/PEInfo/ResourceInfoList/ResourceInfoItem/Type
    * Added PersistenceItem/FileItem/PEInfo/ResourceInfoList/ResourceInfoItem/Size
    * Added PersistenceItem/FileItem/PEInfo/ResourceInfoList/ResourceInfoItem/Language
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/Language
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/ProductName
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/ProductVersion
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/Comments
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/CompanyName
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/FileDescription
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/FileVersion
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/InternalName
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/LegalCopyright
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/OriginalFilename
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/LegalTrademarks
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/PrivateBuild
    * Added PersistenceItem/FileItem/PEInfo/VersionInfoList/VersionInfoItem/SpecialBuild
    * Added PersistenceItem/FileItem/DevicePath
    * Added PersistenceItem/FileItem/FullPath
    * Added PersistenceItem/FileItem/Drive
    * Added PersistenceItem/FileItem/FilePath
    * Added PersistenceItem/FileItem/FileName
    * Added PersistenceItem/FileItem/FileExtension
    * Added PersistenceItem/FileItem/SizeInBytes
    * Added PersistenceItem/FileItem/Created
    * Added PersistenceItem/FileItem/Modified
    * Added PersistenceItem/FileItem/Accessed
    * Added PersistenceItem/FileItem/Entry
    * Added PersistenceItem/FileItem/Changed
    * Added PersistenceItem/FileItem/FilenameCreated
    * Added PersistenceItem/FileItem/FilenameModified
    * Added PersistenceItem/FileItem/FilenameAccessed
    * Added PersistenceItem/FileItem/FilenameChanged
    * Added PersistenceItem/FileItem/FileAttributes
    * Added PersistenceItem/FileItem/Username
    * Added PersistenceItem/FileItem/SecurityID
    * Added PersistenceItem/FileItem/SecurityType
    * Added PersistenceItem/FileItem/INode
    * Added PersistenceItem/FileItem/detectedAnomaly
    * Added PersistenceItem/FileItem/StreamList/Stream/SizeInBytes
    * Added PersistenceItem/FileItem/StreamList/Stream/Name
    * Added PersistenceItem/RegistryItem/Path
    * Added PersistenceItem/RegistryItem/Type
    * Added PersistenceItem/RegistryItem/Modified
    * Added PersistenceItem/RegistryItem/NumSubKeys
    * Added PersistenceItem/RegistryItem/NumValues
    * Added PersistenceItem/RegistryItem/Hive
    * Added PersistenceItem/RegistryItem/KeyPath
    * Added PersistenceItem/RegistryItem/Username
    * Added PersistenceItem/RegistryItem/SecurityID
    * Added PersistenceItem/RegistryItem/ValueName
    * Added PersistenceItem/RegistryItem/Text
    * Added PersistenceItem/RegistryItem/ReportedLengthInBytes
    * Added PersistenceItem/RegistryItem/Value
    * Added PersistenceItem/RegistryItem/detectedAnomaly
    * Added PersistenceItem/ServiceItem/name
    * Added PersistenceItem/ServiceItem/descriptiveName
    * Added PersistenceItem/ServiceItem/description
    * Added PersistenceItem/ServiceItem/mode
    * Added PersistenceItem/ServiceItem/startedAs
    * Added PersistenceItem/ServiceItem/path
    * Added PersistenceItem/ServiceItem/arguments
    * Added PersistenceItem/ServiceItem/serviceDLL
    * Added PersistenceItem/ServiceItem/status
    * Added PersistenceItem/ServiceItem/pid
    * Added PersistenceItem/ServiceItem/type
    * Added PersistenceItem/ServiceItem/detectedAnomaly
    * Added PersistenceItem/RegPath
    * Added PersistenceItem/RegText
    * Added PersistenceItem/RegValue
    * Added PersistenceItem/RegContext
    * Added PersistenceItem/RegOwner
    * Added PersistenceItem/RegModified
    * Added PersistenceItem/FilePath
    * Added PersistenceItem/LinkFilePath
    * Added PersistenceItem/PersistenceType
    * Added PersistenceItem/FileOwner
    * Added PersistenceItem/FileCreated
    * Added PersistenceItem/FileModified
    * Added PersistenceItem/FileAccessed
    * Added PersistenceItem/FileChanged
    * Added PersistenceItem/ServiceName
    * Added PersistenceItem/ServicePath
    * Added PersistenceItem/serviceDLL
    * Added PersistenceItem/descriptiveName
    * Added PersistenceItem/arguments
    * Added PersistenceItem/mode
    * Added PersistenceItem/startedAs
    * Added PersistenceItem/status
    * Added PersistenceItem/pathSignatureExists
    * Added PersistenceItem/pathSignatureVerified
    * Added PersistenceItem/pathSignatureDescription
    * Added PersistenceItem/pathCertificateSubject
    * Added PersistenceItem/pathCertificateIssuer
    * Added PersistenceItem/serviceDLLSignatureExists
    * Added PersistenceItem/serviceDLLSignatureVerified
    * Added PersistenceItem/serviceDLLSignatureDescription
    * Added PersistenceItem/serviceDLLCertificateSubject
    * Added PersistenceItem/serviceDLLCertificateIssuer
    * Added PersistenceItem/detectedAnomaly
    * Added PersistenceItem/name
    * Added PersistenceItem/userName
    * Added PersistenceItem/groupName
    * Added PersistenceItem/reference
    * Added PersistenceItem/keepAlive
    * Added PersistenceItem/disabled
    * Added PersistenceItem/alias
    * Added PersistenceItem/path
    * Added PersistenceItem/pathAttributes/owner
    * Added PersistenceItem/pathAttributes/group
    * Added PersistenceItem/pathAttributes/size
    * Added PersistenceItem/pathAttributes/accessedTime
    * Added PersistenceItem/pathAttributes/modifiedTime
    * Added PersistenceItem/pathAttributes/changedTime
    * Added PersistenceItem/pathAttributes/createdTime
    * Added PersistenceItem/type
    * Added ModuleItem/Md5sum
    * Added ModuleItem/Sha1sum
    * Added ModuleItem/Sha256sum
    * Added ModuleItem/Module
    * Added ModuleItem/Size
    * Added ModuleItem/UsedByList/Module
    * Added ModuleItem/Status
    * Added ModuleItem/Address
    * Added ModuleItem/Filename
    * Added ModuleItem/License
    * Added ModuleItem/AliasList/Alias/Name
    * Added ModuleItem/SrcVersion
    * Added ModuleItem/DependsList/Depends/Module
    * Added ModuleItem/Retpoline
    * Added ModuleItem/Intree
    * Added ModuleItem/Vermagic
    * Added ModuleItem/Signat
    * Added ModuleItem/Signer
    * Added ModuleItem/SigKey
    * Added ModuleItem/SigHashAlgorithm
    * Added ModuleItem/ParmList/Parm/Name
    * Added ArpEntryItem/IPv6Address
    * Added ArpEntryItem/InterfaceType
    * Added ArpEntryItem/State
    * Added ArpEntryItem/IsRouter
    * Added ArpEntryItem/LastReachable
    * Added ArpEntryItem/LastUnreachable
    * Added QuarantineEventItem/User
    * Added QuarantineEventItem/EventIdentifier
    * Added QuarantineEventItem/TimeStamp
    * Added QuarantineEventItem/AgentBundleIdentifier
    * Added QuarantineEventItem/AgentName
    * Added QuarantineEventItem/DataURLString
    * Added QuarantineEventItem/TypeNumber
    * Added QuarantineEventItem/OriginURLString
    * Added QuarantineEventItem/SenderName
    * Added QuarantineEventItem/SenderAddress
    * Added QuarantineEventItem/OriginTitle
    * Added ProcessItem/HandleList/Handle/FileDescriptor
    * Added ProcessItem/HandleList/Handle/User
    * Added ProcessItem/HandleList/Handle/Device
    * Added ProcessItem/HandleList/Handle/Size
    * Added ProcessItem/HandleList/Handle/INode
    * Added ProcessItem/HandleList/Handle/SocketType
    * Added ProcessItem/HandleList/Handle/SocketProtocol
    * Added ProcessItem/HandleList/Handle/SocketState
    * Added ProcessItem/HandleList/Handle/SocketLocalAddress
    * Added ProcessItem/HandleList/Handle/SocketLocalPort
    * Added ProcessItem/HandleList/Handle/SocketRemoteAddress
    * Added ProcessItem/HandleList/Handle/SocketRemotePort
    * Added ProcessItem/HandleList/Handle/Md5sum
    * Added ProcessItem/HandleList/Handle/Sha1sum
    * Added ProcessItem/HandleList/Handle/Sha256sum
    * Added GroupItem/GroupName
    * Added GroupItem/fullname
    * Added GroupItem/groupguid
    * Added GroupItem/userlist/username
    * Added GroupItem/gid
    * Added TaskItem/DigitalSignature/SignatureExists
    * Added TaskItem/DigitalSignature/SignatureVerified
    * Added TaskItem/DigitalSignature/CertificateSubject
    * Added TaskItem/DigitalSignature/CertificateIssuer
    * Added TaskItem/DigitalSignature/CertificateChain
    * Added TaskItem/DigitalSignature/Description
    * Added TaskItem/path
    * Added TaskItem/arguments
    * Added TaskItem/userName
    * Added TaskItem/groupName
    * Added TaskItem/disabled
    * Added TaskItem/triggers/trigger/type
    * Added TaskItem/triggers/trigger/delay
    * Added TaskItem/triggers/trigger/schedule
    * Added TaskItem/triggers/trigger/details
    * Added TaskItem/reference
    * Added TaskItem/crontabPath
    * Added TaskItem/crontabMinute
    * Added TaskItem/crontabHour
    * Added TaskItem/crontabDayOfMonth
    * Added TaskItem/crontabMonth
    * Added TaskItem/crontabDayOfWeek
    * Added TaskItem/crontabEvent
    * Added TaskItem/crontabCommand
    * Added TaskItem/crontabPeriod
    * Added TaskItem/crontabDelay
    * Added TaskItem/crontabJobIdentifier
    * Added SystemRestoreItem/ChangeEvent
    * Added SystemRestoreItem/ProcessName
    * Added SystemRestoreItem/DebugInfoProcessId
    * Added SystemRestoreItem/DebugInfoThreadId
    * Added SystemRestoreItem/DebugInfoProcessName
    * Added SystemRestoreItem/DebugInfoTimeStamp
    * Added SystemRestoreItem/OriginalVolumePath
    * Added SystemRestoreItem/NewFileName
    * Added VolumeItem/DeviceID
    * Added VolumeItem/RemoteFS
    * Added VolumeItem/RemoteAddress
    * Added VolumeItem/VolumeID
    * Added VolumeItem/TotalSize
    * Added VolumeItem/FreeSize
    * Added VolumeItem/MountPoint
    * Added VolumeItem/Flags/Ejectable
    * Added VolumeItem/Flags/Removable
    * Added VolumeItem/Flags/ReadOnly
    * Added VolumeItem/Flags/Logical
    * Added VolumeItem/Flags/RAID
    * Added UserItem/shell
    * Added UserItem/userid
    * Added UserItem/userguid
    * Added UserItem/autologin
    * Added ShellHistoryItem/FileOrder
    * Added ShellHistoryItem/Command
    * Added ShellHistoryItem/UserName
    * Added ShellHistoryItem/Shell
    * Added ShellHistoryItem/Timestamp
    * Added FormHistoryItem/EncryptedUsername
    * Added FormHistoryItem/PasswordChangedDate
    * Added DriverItem/PEInfo/ImportedModules/Module/NumberOfFunctions
    * Added DriverItem/IRP_MJ_CREATE
    * Added DriverItem/IRP_MJ_CREATE_NAMED_PIPE
    * Added DriverItem/IRP_MJ_CLOSE
    * Added DriverItem/IRP_MJ_WRITE
    * Added DriverItem/IRP_MJ_READ
    * Added DriverItem/IRP_MJ_QUERY_INFORMATION
    * Added DriverItem/IRP_MJ_SET_INFORMATION
    * Added DriverItem/IRP_MJ_QUERY_EA
    * Added DriverItem/IRP_MJ_SET_EA
    * Added DriverItem/IRP_MJ_FLUSH_BUFFERS
    * Added DriverItem/IRP_MJ_QUERY_VOLUME_INFORMATION
    * Added DriverItem/IRP_MJ_SET_VOLUME_INFORMATION
    * Added DriverItem/IRP_MJ_DIRECTORY_CONTROL
    * Added DriverItem/IRP_MJ_FILE_SYSTEM_CONTROL
    * Added DriverItem/IRP_MJ_DEVICE_CONTROL
    * Added DriverItem/IRP_MJ_INTERNAL_DEVICE_CONTROL
    * Added DriverItem/IRP_MJ_SHUTDOWN
    * Added DriverItem/IRP_MJ_LOCK_CONTROL
    * Added DriverItem/IRP_MJ_CLEANUP
    * Added DriverItem/IRP_MJ_CREATE_MAILSLOT
    * Added DriverItem/IRP_MJ_QUERY_SECURITY
    * Added DriverItem/IRP_MJ_SET_SECURITY
    * Added DriverItem/IRP_MJ_POWER
    * Added DriverItem/IRP_MJ_SYSTEM_CONTROL
    * Added DriverItem/IRP_MJ_DEVICE_CHANGE
    * Added DriverItem/IRP_MJ_QUERY_QUOTA
    * Added DriverItem/IRP_MJ_SET_QUOTA
    * Added DriverItem/IRP_MJ_PNP
    * Added eventItem/dnsLookupEvent/timestamp
    * Added eventItem/dnsLookupEvent/hostname
    * Added eventItem/dnsLookupEvent/pid
    * Added eventItem/dnsLookupEvent/process
    * Added eventItem/dnsLookupEvent/processPath
    * Added eventItem/dnsLookupEvent/username
    * Added eventItem/imageLoadEvent/timestamp
    * Added eventItem/imageLoadEvent/fullPath
    * Added eventItem/imageLoadEvent/filePath
    * Added eventItem/imageLoadEvent/drive
    * Added eventItem/imageLoadEvent/fileName
    * Added eventItem/imageLoadEvent/fileExtension
    * Added eventItem/imageLoadEvent/devicePath
    * Added eventItem/imageLoadEvent/pid
    * Added eventItem/imageLoadEvent/username
    * Added eventItem/imageLoadEvent/parentPid
    * Added eventItem/imageLoadEvent/process
    * Added eventItem/imageLoadEvent/processPath
    * Added eventItem/processEvent/timestamp
    * Added eventItem/processEvent/eventType
    * Added eventItem/processEvent/pid
    * Added eventItem/processEvent/processPath
    * Added eventItem/processEvent/process
    * Added eventItem/processEvent/parentPid
    * Added eventItem/processEvent/parentProcessPath
    * Added eventItem/processEvent/parentProcess
    * Added eventItem/processEvent/username
    * Added eventItem/processEvent/startTime
    * Added eventItem/processEvent/md5
    * Added eventItem/processEvent/processCmdLine
    * Added eventItem/ipv4NetworkEvent/timestamp
    * Added eventItem/ipv4NetworkEvent/remoteIP
    * Added eventItem/ipv4NetworkEvent/remotePort
    * Added eventItem/ipv4NetworkEvent/localIP
    * Added eventItem/ipv4NetworkEvent/localPort
    * Added eventItem/ipv4NetworkEvent/protocol
    * Added eventItem/ipv4NetworkEvent/pid
    * Added eventItem/ipv4NetworkEvent/process
    * Added eventItem/ipv4NetworkEvent/processPath
    * Added eventItem/ipv4NetworkEvent/username
    * Added eventItem/fileWriteEvent/timestamp
    * Added eventItem/fileWriteEvent/fullPath
    * Added eventItem/fileWriteEvent/filePath
    * Added eventItem/fileWriteEvent/drive
    * Added eventItem/fileWriteEvent/fileName
    * Added eventItem/fileWriteEvent/fileExtension
    * Added eventItem/fileWriteEvent/devicePath
    * Added eventItem/fileWriteEvent/pid
    * Added eventItem/fileWriteEvent/process
    * Added eventItem/fileWriteEvent/processPath
    * Added eventItem/fileWriteEvent/writes
    * Added eventItem/fileWriteEvent/numBytesSeenWritten
    * Added eventItem/fileWriteEvent/lowestFileOffsetSeen
    * Added eventItem/fileWriteEvent/dataAtLowestOffset
    * Added eventItem/fileWriteEvent/textAtLowestOffset
    * Added eventItem/fileWriteEvent/closed
    * Added eventItem/fileWriteEvent/size
    * Added eventItem/fileWriteEvent/md5
    * Added eventItem/fileWriteEvent/username
    * Added eventItem/fileWriteEvent/parentProcessPath
    * Added eventItem/fileWriteEvent/parentPid
    * Added eventItem/fileWriteEvent/openTime
    * Added eventItem/fileWriteEvent/openDuration
    * Added eventItem/fileWriteEvent/eventReason
    * Added eventItem/urlMonitorEvent/timestamp
    * Added eventItem/urlMonitorEvent/hostname
    * Added eventItem/urlMonitorEvent/requestUrl
    * Added eventItem/urlMonitorEvent/urlMethod
    * Added eventItem/urlMonitorEvent/userAgent
    * Added eventItem/urlMonitorEvent/httpHeader
    * Added eventItem/urlMonitorEvent/remoteIpAddress
    * Added eventItem/urlMonitorEvent/remotePort
    * Added eventItem/urlMonitorEvent/localPort
    * Added eventItem/urlMonitorEvent/pid
    * Added eventItem/urlMonitorEvent/process
    * Added eventItem/urlMonitorEvent/processPath
    * Added eventItem/urlMonitorEvent/username
    * Added eventItem/regKeyEvent/timestamp
    * Added eventItem/regKeyEvent/hive
    * Added eventItem/regKeyEvent/keyPath
    * Added eventItem/regKeyEvent/path
    * Added eventItem/regKeyEvent/originalPath
    * Added eventItem/regKeyEvent/eventType
    * Added eventItem/regKeyEvent/pid
    * Added eventItem/regKeyEvent/process
    * Added eventItem/regKeyEvent/processPath
    * Added eventItem/regKeyEvent/valueName
    * Added eventItem/regKeyEvent/valueType
    * Added eventItem/regKeyEvent/value
    * Added eventItem/regKeyEvent/text
    * Added eventItem/regKeyEvent/username
    * Added eventItem/addressNotificationEvent/timestamp
    * Added eventItem/addressNotificationEvent/address
    * Added DiskItem/DevicePath
    * Added DiskItem/DiskConnection
    * Added DiskItem/Type
    * Added QuarantineListItem/QuarId
    * Added QuarantineListItem/CorrelationId
    * Added QuarantineListItem/QuarantineTime
    * Added QuarantineListItem/Final
    * Added QuarantineListItem/ObjectType
    * Added QuarantineListItem/FilePath
    * Added QuarantineListItem/FileSize
    * Added QuarantineListItem/FileMD5
    * Added QuarantineListItem/FileSHA1
    * Added QuarantineListItem/FileState
    * Added PortItem/isIPv6
    * Added RegistryItem/SecurityID
    * Added LoginHistoryItem/Path
    * Added LoginHistoryItem/StartTime
    * Added LoginHistoryItem/EndTime
    * Added LoginHistoryItem/SessionLength
    * Added LoginHistoryItem/Hostname
    * Added LoginHistoryItem/IsRemoteLogin
    * Added LoginHistoryItem/IPv4Address
    * Added LoginHistoryItem/IPv6Address
    * Added LoginHistoryItem/Username
    * Added LoginHistoryItem/RecordType
    * Added LoginHistoryItem/PID
    * Added LoginHistoryItem/Terminal
    * Added LoginHistoryItem/IsFailedLogin
    * Added ServiceItem/md5sum
    * Added ServiceItem/sha1sum
    * Added ServiceItem/sha256sum
    * Added ServiceItem/pathCertificateChain
    * Added ServiceItem/DigitalSignature/SignatureExists
    * Added ServiceItem/DigitalSignature/SignatureVerified
    * Added ServiceItem/DigitalSignature/CertificateSubject
    * Added ServiceItem/DigitalSignature/CertificateIssuer
    * Added ServiceItem/DigitalSignature/Description
    * Added ServiceItem/machServices/machService
    * Added ServiceItem/userName
    * Added ServiceItem/groupName
    * Added ServiceItem/reference
    * Added Syslog/ID
    * Added Syslog/Time
    * Added Syslog/Date
    * Added Syslog/Level
    * Added Syslog/PID
    * Added Syslog/UID
    * Added Syslog/GID
    * Added Syslog/Host
    * Added Syslog/Sender
    * Added Syslog/Facility
    * Added Syslog/Message
    * Added Syslog/LogFile
    * Added Syslog/LogFileModified
    * Added CookieHistoryItem/IsHTTPOnly
    * Added CookieHistoryItem/LastVisitDate
    * Added SystemInfoItem/containmentState
    * Added SystemInfoItem/containmentWhitelistArray/ip
    * Added SystemInfoItem/biosInfo/biosType
    * Added SystemInfoItem/drives
    * Added SystemInfoItem/platform
    * Added SystemInfoItem/procConfigInfo/vmGuest
    * Added SystemInfoItem/procConfigInfo/virtualization
    * Added SystemInfoItem/procConfigInfo/iommu
    * Added SystemInfoItem/procConfigInfo/lpcDevice
    * Added SystemInfoItem/kernelVersion
    * Added SystemInfoItem/OSbitness
    * Added SystemInfoItem/timezone
    * Added SystemInfoItem/gmtoffset
    * Added SystemInfoItem/clockSkew
    * Added SystemInfoItem/stateAgentStatus
    * Added SystemInfoItem/networkArray/networkInfo/ipArray/ipInfo/ipv6Address
    * Added SystemInfoItem/primaryIpv4Address
    * Added SystemInfoItem/primaryIpAddress
    * Added SystemInfoItem/loggedOnUser
    * Added SystemInfoItem/appVersion
    * Added SystemInfoItem/appCreated

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
