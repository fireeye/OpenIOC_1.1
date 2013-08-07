# IOC Terms Definitions

This document provides definitions for some IOC terms found in the iocterms files provided with the OpenIOC schema.

More information on OpenIOC can be found at OpenIOC.org

## Terms

### DNS Host

Audit Group & Name: DnsEntryItem/Host

Definition: The DnsEntryItem/Host is the cached host value of an attempted DNS lookup. This is stored locally in the host’s DNS cache, but only for a short period of time. 

Example:

    DNS Host contains "evildomain.com"

Use in an IOC: Use this term to find malicious hostnames that an infected host attempted to resolve, or to record hostnames for malware found in additional analysis.

Related Terms:

    Other network terms



### EventLog Message

Audit Group & Name: EventLogItem/message

Definition: This is the formatted event log message text that comes from Windows’ standard event logs. It may contain Tab and NewLine characters in it. The text varies and could be user logs, schedule tasks, service installations, and antivirus events, etc.

Example:

    EventLog Message contains ‘PSEXEC SERVICE service was successfully sent a start control’

Use in an IOC: Often used after initial sweeping to conduct further investigation, or to identify specific events created by some specific types of malicious tools or malware.

Related Terms:

    EventLog ID
    EventLog GenTime



### File ADS Name

Audit Group & Name: FileItem/StreamList/Stream/Name

Definition: Looks for alternate data streams associated with files on a disk. This term is the name of a file contained in an Alternate Data Stream on an NTFS file system that is attached to the end of a file. The name does not include the parent filename.

Example:

    File ADS Name is "evilhiddenfile"
    File ADS Name contains "evil"

Use in an IOC: Use this term to match filenames of files contained in alternate data streams, when you are looking for a particular stream.

Related Terms:

    File Name
    File Full Path
    Other File Attributes



### File Compile Time

Audit Group & Name: FileItem/PEInfo/PETimeStamp

Definition: This term describes an attribute of a Windows PE files that shows a timestamp of when the file was compiled. It uses the ISO 8601 format for date & time, based off of Zulu time zone. It can also describe a range between two times.

Example:

    File Compile Time is "2011-04-20T10:28:55Z"
    File Compile Time is "2011-04-20T10:28:55Z TO 2012-12-14T19:09:00Z"

Use in an IOC: You can use this to determine what files have been recently compiled, compiled at a specific time, or compiled during a range of times. This can detect recently compiled files, or help find anomalies against other file timestamp information.

Related Terms:

    File Created Time
    File Modified Time
    Other FileItem terms for constraining matches.



### File DLL Export Name

Audit Group & Name: FileItem/PEInfo/Exports/DllName

Definition: The name of the library that a function in the DLL export table is exported from.

Example:

    File DLL Export Name is "evildll.dll"

Use in an IOC: Use this IOC term to match malicious filename in the DLL export table. May be used in conjunction with other File terms to narrow down results

Related Terms:

    File Export Function
    File Export Count
    File Full Path
    File Name
    File Import Function



### File Export Count

Audit Group & Name: FileItem/PEInfo/Exports/NumberOfFunctions

Definition: The number of exported functions published by a given DLL.

Example:

    File Export Count is "5"

Use in an IOC: Used to narrow down potential DLLs that other PEInfo functions are applied to, or identify DLLs with unusual numbers of functions (very large or very small)

Related Terms:

    File DLL Export Name
    File Export Function
    Other FileItem terms



### File Export Function

Audit Group & Name: FileItem/PEInfo/Exports/ExportedFunctions/string

Definition: File Export Functions are functions in a Windows PE that are advertised so they can be called by other modules in other executables. They are listed in the PE File that offers them, usually by name. They are usually in DLLs, rarely in EXEs.

Example:

    File Export Function is "UnServiceInstall"

Use in an IOC: This term may be used to look for exports in files that do not usually have exports, or for unique exports in files that are specific to malicious tools, or combinations of exports that are specific to malicious software.

Related Terms:

    File Dll Export Name
    File Export Count
    Other FileItem terms for constraining matches.



### File Extension

Audit Group & Name: FileItem/FileExtension

Definition: The suffix of a file name that typically indicates the type of file it is (such as .exe).  This is derived from the filename itself, and is not indicative of whether or not a file is actually the type that it claims to be.

Example:

    File Extension is "exe"
    Not File Extension is "dll"

Use in an IOC: This term is usually used with other file item terms to help include or exclude certain types of files.

Related Terms:

    File PE Type
    Other FileItem terms



### File Full Path

Audit Group & Name: FileItem/FullPath

Definition: The File Full Path shows the entire path to a file from the root of the drive partition it is on, including the drive designation and the file extension.

Example:

    File Full Path is "C:\Windows\System32\autocheck.exe"
    File Full Path contains "AppData\log.txt"


Use in an IOC: Use of this term allows you to specify the exact path of where you expect to find a file, including the drive designation and the name of the file. It is usually used with the "contains" operator since it is so specific, but can be used with "is" when you want to specify an exact location. It is used less often than File Path, and is limited because it is so specific.

Related Terms:

    File Path
    File Name
    Other FileItem terms for constraining matches.



### File Import Function

Audit Group & Name: FileItem/PEInfo/ImportedModules/Module/ImportedFunctions/string

Definition: File Import Functions are functions called in other code modules by a Windows PE file when it executes. They are listed in the PE File that requires them, usually by name.

Example:

    File Import Function is "expungeconsolecommandhistoryw"

Use in an IOC: File Import Function can be used to find uniquely named functions or specific groups of functions used by attackers. Non-unique function names or groups of functions that are too generic can lead to false positives. Be careful when using with small groups of functions that might be called by normal windows programs.

Related Terms:

    File Import Name
    Other FileItem terms for constraining matches.



### File Import Name

Audit Group & Name: FileItem/PEInfo/ImportedModules/Module/Name

Definition: This Term indicates the name of DLLs that imported functions are called from. Imported functions are capabilities that are imported from other DLLs rather than being in the binary itself.

Example:

    File Import Name is "evildll.dll"
    Not File Import Name is "kernel32.dll"

Use in an IOC: Use with File Import Function to specify combinations of DLLs that imports are called from by a file and the imports themselves. Also, use this term to remove false positives by excluding legitimate files.

Related Terms:

    File Import Function



### File MD5

Audit Group & Name: FileItem/MD5Sum

Definition: File MD5 is the MD5 checksum of a file. This value is derived from using the MD5 cryptographic algorithm to determine a unique fingerprint for the file.

Example:

    File MD5 is "e4d909c290d0fb1ca068ffaddf22cbd0"

Use in an IOC: MD5 is used to match exact instances of a file. Aside from very rare cases, if you match on the MD5 of a file, you can assume it is the exact file that you have seen before. MD5 alone should not be relied upon for anything other than that use case.

Related Terms:

    Other FileItem terms for constraining matches.



### File Name

Audit Group & Name: FileItem/FileName

Definition: File Name is the name attribute of a file saved on disk.

Example:

    File Name is "foo.exe"

Use in an IOC: File Name is used to match the names of specific files. File names are highly mutable by attackers, so File Name should ONLY ever be used with other file attributes, unless the file name is extremely unusual or truly unique. Even then, other attributes of the file should be captured if possible.

Related Terms:

    File Size
    File Compile Time
    Other FileItem terms for constraining matches.



### File Path

Audit Group & Name: FileItem/FilePath

Definition: This term is the path to where a file resides on a file system starting from the root of the drive, but does not include the drive designation or the file name. This term also does not include trailing or following slashes or backslashes.

Example:

    File Path contains "Windows\System32"
    File Path is "Recycler"

Use in an IOC: Use of this term allows you to specify the path to a file, in a less specific manner than File Full Path. File Path is not specific to a drive designation, nor a specific file, thus allowing for more flexible matching trying to find files in specific locations.

Related Terms:

    File Full Path
    Other FileItem terms for constraining matches.



### File PE Detected Anomalies

Audit Group & Name: FileItem/PEInfo/DetectedAnomalies/string

Definition: This term indicates that there is an anomaly with the structure of a Windows PE file. Values returned for this are detailed in the MIR User Guide, Appendix I.

Example:

    File Detected Anomalies contains "contains_eof_data"

Use in an IOC: Some anomalies can be innocent, and just a result of faulty or benign code, and are best combined with other factors to identify specific pieces of malware that contain said anomalies. Other anomalies are much more likely to be malicious, such as contains_eof_data.

Related Terms:

    File Import Function
    File Export Function
    Other FileItem terms for constraining matches.



### File PE Type

Audit Group & Name: FileItem/PEInfo/Type

Definition: This indicates whether a PE file is an executable or DLL by looking at the actual file header instead of the file extension.

Example:

    AND
        File PE Type is "DLL"
        File Name is "Evil.txt"

    AND
        File PE Type is "executable"
        Not File Extension is "exe"

Use in an IOC: Use this term to match the value of the PE Type from an executable file’s PE header. It is a way of searching for seemingly innocent files that may actually be mislabeled .dll or .exe files.

Related Terms:

    File Extension



### File Section Name

Audit Group & Name: FileItem/PEInfo/Sections/Section/Name

Definition: This is a named section of a Windows PE file.  These represent code or data portions of a PE file.

Example:

    File Section Name contains ".code"
    File Section Name contains ".data"
    File Section Name contains ".upx1"

Use in an IOC: Use this term to identify files with uncommon or unique section names within an environment.

Related Terms:

    Other FileItem terms



### File Size

Audit Group & Name: FileItem/SizeInBytes

Definition: The File Size is the size of a file represented in number of bytes. It can be a number or a range

Example:

    File Size is "12300"
    File Size is "101000 TO 120000"

Use in an IOC: File Size is used with other file operators to indicate specific instances of a file. It can be used to distinguish between two files with the same name (that are actually different files) or in conjunction with other file attributes to show recurrence of the same file.

Related Terms:

    File Name
    File Compile Time
    Other FileItem terms for constraining matches.



### File Strings

Audit Group & Name: FileItem/StringList/string

Definition: A string found within a file.

Example:

    File Strings contains "xyzpdq13"

Use in an IOC: This term is used to match against unique strings in malicious files. It may be for informational purposes or further investigation versus an initial hit, as a strings audit is very time consuming to conduct. Very unique strings often are strong enough to stand alone at the top level of an indicator.

Related Terms:

    Other FileItem Terms



### Network DNS

Audit Group & Name: Network/DNS

Definition: This is the FQDN of a DNS lookup. This is for informational purposes, and is not found in MIR audits.

Example:

    DNS is "www.malwaredomain.com"
    DNS contains "malwaredomain.com"

Use in an IOC: This term is used mainly for reference, so that the context of DNS entries observed in the course of an investigation can be communicated to future consumers of the IOC.

Related Terms:

    Other Network Items



### Network String URI

Audit Group & Name: Network/URI

Definition: The URI portion of an HTTP or related network request.

Example:

    Network String URI contains "/cgi_bin/evil.php"

Use in an IOC: Used for reference to identify network communication strings.

Related Terms:

    Other Network terms

    

### Prefetch Accessed File

Audit Group & Name: PrefetchItem/AccessedFileList/AccessedFile

Definition: A full path to a file found in the prefetch list created by Windows. This list is of files that are commonly used or accessed, and may additionally show when a particular executable was launched. The prefetch list is stored in a subfolder of the Windows system folder.

Example:

    Prefetch Accessed File is "C:\WINDOWS\system32\evil.dll"
    Prefetch Accessed File contains "evil.exe"

Use in an IOC: Use this term to find files accessed by programs executed on the system. If malware consists of a collection of files, but only one of them is actually executed while others are just accessed, this term might be useful to find the accessed file.

Related Terms:

    FileItem/FullPath
    FileItem/FileName
    FileItem/Path
    PrefetchItem/ApplicationFullPath



### Prefetch Application Full Path

Audit Group & Name: PrefetchItem/ApplicationFullPath

Definition: This is the full path, including drive letter and directories, of an executable for which a prefetch file was created after that file was executed by the operating system.

Example:

    Prefetch Application Full Path is "C:\temp\malware.exe"
    Prefetch Application Full Path contains "malware.exe"

Use in an IOC: Use this term to find malicious filenames or paths of executables that ran on a system and created prefetch entries. You can use this term to look for instances of malware named the same as a normal file, but in the wrong directory by looking at the full path.

Related Terms:

    File Full Path
    File Name
    File Path
    Prefetch File Executed
    Prefetch Accessed File



### Prefetch File Executed

Audit Group & Name: PrefetchItem/ApplicationFileName

Definition: This is the name of an executable for which Windows created a prefetch file for after execution. The term does not include the full path, just the name of the file.

Example:

    Prefetch File Executed is "blah.exe"
    Prefetch File Executed contains "blah.exe"
    Prefetch File Executed contains "blah"

Use in an IOC: Use this term to find malicious filenames of executables that ran on a system and had prefetch entries created.

Related Terms:

    File Full Path
    File Name
    File Path
    Prefetch Application Full Path
    Prefetch Accessed File

 

### Port Remote IP

Audit Group & Name: PortItem/RemoteIP

Definition: The Port Remote IP is any remote IP address that is communicating with the Windows host that is captured in real-time when an audit is run. This is reported in the TP/IP connection table.

Example:

    Port Remote IP is "192.168.1.1"

Use in an IOC: This Term is often used for contextual information. It records the remote IP address that a host is currently communicating with, and may be used if remote IPs of C2 servers or other suspicious systems are known.

Related Terms:

    Other Network Terms



### Process Handle Name

Audit Group & Name: ProcessItem/HandleList/Handle/Name

Definition: The name of a named handle associated with a running process.

Example:

    Process Handle Name contains "evilMutex"

Use in an IOC: This term is often used to describe Mutexes or "Mutants" which can be unique to malware processes. It can be used with Process Handle Type as well, but it is not necessary.  The use of this term is NOT limited to describing mutexes.

Related Terms:

    Process Name
    Process HandleList Type
    Other Process Items



### Process Handle Type

Audit Group & Name: ProcessItem/HandleList/Handle/Type

Definition: The type of handle that a Windows process currently has opened. A handle is a connection from a process to an object or resource in the Windows operating system. Handle types are defined for each version of Windows, but there are common names across most versions.

Example:

    Process Handle is "File"
    Process Handle is "Event"
    Process Handle is "Mutant"
    Process Handle is "Registry Key"

Use in an IOC: Use this term to specify the type of handle that a process has open. Common handle types that are useful in IOCs are “mutant,” “event,” and “file.” Never use this term by itself.

Related Terms:

    Process HandleList Name
    Process Name
    Process Path



### Process Path

Audit Group & Name: ProcessItem/path

Definition: The full path (without drive letter) to a directory that a process is running out of. The process path does not include the name of the running process.

Example:

    ProcessItem/path contains "WINDOWS\system32"
    ProcessItem/path is "Windows\ "

Use in an IOC: Use this term to match the path that a process is running from. You can use this to look for files with the correct names that are running from the wrong locations, or other anomalous behavior. You can also use this to look for files running from a particular directory without knowing an exact file name.

Related Terms:

    File Full Path
    Process Name



### Process Name

Audit Group & Name: ProcessItem/name

Definition: This is the name of the process that is identified on the system.

Example:

    Process Name is "IEXPLORE.EXE"

Use in an IOC: This may be used to identify running processes on a system.

Related Terms:

    Process Path



### Process Section Name

Audit Group & Name: ProcessItem/SectionList/MemorySection/Name

Definition: The full path (drive letter, directory, and file name) to a file that is loaded into that section of a process’s memory.

Example:

    Process Section Name contains "system32\cmd.exe"
    Process Section Name is "C:\WINDOWS\system32\cmd.exe"

Use in an IOC: Use this IOC term to match names of sections loaded in a process. The section name will usually be a full path to a library or file on disk.

Related Terms:

    File Full Path
    Process Path
    Process Name



### Registry Path

Audit Group & Name: RegistryItem/Path

Definition: The location of a Key in the Windows Registry, including everything from the Hive Name down to the Key Name.

Example:

    Registry Path contains "Services\RasAuto\Parameters"
    Registry Path is "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\RasAuto\Parameters\ServiceDLL"

Use in an IOC: Registry Path is usually used in conjunction with Registry Text, ANDed together to describe a Key location and what the value of the Key is. Registry Path is much like File Full Path, and usually best used with contains to depict a specific portion of the path, though it can be used to indicate the entire path from a Hive down to the Key Name.

Related Terms:

    Registry Text
    Registry Value Name
    Other RegistryItem terms for constraining matches.



### Registry Text

Audit Group & Name: RegistryItem/Text

Definition: The value of an entry designated by a Registry Value Name inside a Registry Key. 

Example:

    Registry Text contains "svchost.exe"
    Registry Text is "svchost.exe"

Use in an IOC: Registry Text is usually used in conjunction with Registry Text, ANDed together to describe a value of a Registry Key, and the location of where that Key may be found in the registry. 

Related Terms:

    Registry Path
    Registry Value Name
    Other RegistryItem terms for constraining matches.

 

### Registry ValueName

Audit Group & Name: RegistryItem/ValueName

Definition: This is the name of a registry value (REG_SZ, REG_DWORD, REG_KEY, etc..) that is present in a registry key.

Example:

    Registry ValueName is "ServiceDLL"

Use in an IOC: This term allows for flexibility when identifying values that are associated with specific Registry Paths or Registry Text fields.

Related Terms:

    Registry Path
    Registry Text



### Service Descriptive Name

Audit Group & Name: ServiceItem/descriptiveName

Definition: The long descriptive name of a Windows service displayed in the service manager list. This is the name that appears in the services manager control panel.

Example:

    Service Descriptive Name is "Desktop Help Session Manager"

Use in an IOC: Use this to find anomalies or malicious service names. You can search for malicious services that an attacker installs, that may have a descriptive name that is similar to a legitimate service, but has subtle (or not so subtle) differences that could be found using this term.

Related Terms:

    Registry Text
    Service Path
    Service DLL
    Service Name



### Service DLL

Audit Group & Name: ServiceItem/serviceDLL

Definition: The path to the DLL loaded by a service, including the name of the DLL itself. 

Example:

    Service DLL contains "system32\evil.dll"
    Not Service DLL contains "system32\good.dll"

Use in an IOC: This term is usually used with contains, since it is the path and file name of the DLL loaded by a service. This can be used to identify DLLs that are malicious that are loaded by compromised or malicious services, or it could be used to exclude legitimate DLLs to remove false positives.

Related Terms:

    Service Path
    Service Name



### Service DLL MD5

Audit Group & Name: ServiceItem/serviceDLLmd5sum

Definition: This is the MD5 hash value of a dynamic link library loaded by a Windows service. For services that run as DLLs, this is the MD5 checksum of that DLL.

Example:

    Service DLL MD5 is "a9a3daa780ca6c9671a19d52456705b4"

Use in an IOC: Use this to match the MD5s of known malicious Service DLLs.  This is similar to looking for a File MD5, but for services only.

Related Terms:

    File MD5
    Service DLL Path
    Registry Text
    Service DLL
    Service Name



### Service Name

Audit Group & Name: ServiceItem/Name

Definition: This Term is the short name of a service as it is stored in the Windows Registry. 

Example:

    Service Name is "windowzupdate"

Use in an IOC: This term is often used to look for known malicious services, or in conjunction with other terms to look for anomalies from expected service behavior.

Related Terms:

    Service Path



### Service Path

Audit Group & Name: ServiceItem/path

Definition: The path to and including the name of an executable used to launch a service.

Example:

    Service Path contains "evilfile.exe"
    Service Path contains "system32\svch0st.exe"

Use in an IOC: This is usually used to specify the executable used to launch a service with a "contains" specifying the file name in question, or the file and a portion of the path leading to it.

Related Terms:

    Other ServiceItems



### Snort

Audit Group & Name: Snort/Snort

Definition: This allows embedding a complete snort signature into an IndicatorItem.

Example:

    <Snort Signature encoded in field>

Use in an IOC: Used to encapsulate a Snort signature in an IOC

Related Terms:

    Network DNS
    DNS Host
    Network String URI



### SystemRestore Original Filename

Audit Group & Name: SystemRestoreItem/OriginalFileName    

Definition: A file name and path not including the drive letter of a file that was copied by the Windows XP system restore mechanism. This only pertains to specific files with certain extensions. Please consult Windows XP documentation for the functioning of the Windows XP system restore mechanism.

Example:

    SystemRestore Original Filename contains "\WINDOWS\Installer\evilfile.msi"

Use in an IOC: Use this term in an IOC to search for a filename or path in the system restore points on a Windows XP system. Using this term may allow an investigator to find evidence of files that were once on a system, but were subsequently deleted after the creation of a restore point.

Example: 

Related Terms:

    File Full Path
    SystemRestore Original Short File Name



### YARA

Audit Group & Name: YARA/YARA

Definition: This allows embedding a complete YARA signature into an IndicatorItem.

Example:

        <YARA Signature encoded in field>

Use in an IOC: Used to encapsulate a YARA signature in an IOC file.

Related Terms:

    File Strings