---
Description: The event type class for the RequestErrorEvent event.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: d46764d7-a9b0-4ea9-9a73-e10e22a2c8cc
ms.prod: windows-server-dev
ms.technology:
- asp.net
- windows-management-instrumentation
ms.tgt_platform: multiple
title: RequestErrorEvent class
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# RequestErrorEvent class

The event type class for the **RequestErrorEvent** event.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.

## Syntax

``` syntax
[Dynamic, EventType(77), EventLevel(3), EventVersion(1), EventTypeName("RequestErrorEvent")]
class RequestErrorEvent : BaseErrorEvent
{
  uint8   SECURITY_DESCRIPTOR[];
  uint64  TIME_CREATED;
  string  EventTime;
  string  EventID;
  sint64  SequenceNumber;
  sint64  Occurrence;
  sint32  EventCode;
  sint32  EventDetailCode;
  string  EventMessage;
  string  ApplicationDomain;
  string  TrustLevel;
  string  ApplicationVirtualPath;
  string  ApplicationPath;
  string  MachineName;
  string  CustomEventDetails;
  string  SecurityDescriptor = "O:BAG:BAD:(A;;0x10000001;;;S-1-5-11)";
  sint32  ProcessID;
  string  ProcessName;
  string  AccountName;
  string  ExceptionType;
  string  ExceptionMessage;
  string  RequestPath;
  string  RequestUrl;
  string  UserHostAddress;
  string  UserName;
  boolean UserAuthenticated;
  string  UserAuthenticationType;
  string  RequestThreadAccountName;
  sint32  ThreadID;
  string  ThreadAccountName;
  string  StackTrace;
  boolean IsImpersonating;
};
```

## Members

The **RequestErrorEvent** class has these types of members:

-   [Properties](#properties)

### Properties

The **RequestErrorEvent** class has these properties.

<dl> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (3), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The account name.

</dd> <dt>

**ApplicationDomain**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (8), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The application domain.

</dd> <dt>

**ApplicationPath**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (11), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The application path.

</dd> <dt>

**ApplicationVirtualPath**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (10), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The application virtual path.

</dd> <dt>

**CustomEventDetails**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (13), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

Custom event details.

</dd> <dt>

**EventCode**
</dt> <dd> <dl> <dt>

Data type: **sint32**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (5)
</dt> </dl>

The event code.

</dd> <dt>

**EventDetailCode**
</dt> <dd> <dl> <dt>

Data type: **sint32**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (6)
</dt> </dl>

The event detail code.

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (2), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The identifier of the event.

</dd> <dt>

**EventMessage**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (7), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The message that describes the event.

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (1), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The time the event occurred.

</dd> <dt>

**ExceptionMessage**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (2), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The exception message.

</dd> <dt>

**ExceptionType**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (1), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The type of exception.

</dd> <dt>

**IsImpersonating**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (10)
</dt> </dl>

Is impersonating. True if impersonating; otherwise, false.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (12), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The name of the machine.

</dd> <dt>

**Occurrence**
</dt> <dd> <dl> <dt>

Data type: **sint64**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (4)
</dt> </dl>

The *n*th occurrence of the event.

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Data type: **sint32**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (1)
</dt> </dl>

The process identifier.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (2), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The name of the process.

</dd> <dt>

**RequestPath**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (1), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The path of the request.

</dd> <dt>

**RequestThreadAccountName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (6), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The name of the account that requested the thread.

</dd> <dt>

**RequestUrl**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (1), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The URL of the request.

</dd> <dt>

**SECURITY\_DESCRIPTOR**
</dt> <dd> <dl> <dt>

Data type: **uint8** array
</dt> <dt>

Access type: Read-only
</dt> </dl>

Descriptor used by the event provider to determine which users can receive the event. This property is inherited from [**\_\_Event**](https://msdn.microsoft.com/windows/desktop/4d2e4715-041c-49e9-b948-a148dfe85483). For more information about constants used to set this security descriptor, see [WMI Security Constants](https://msdn.microsoft.com/windows/desktop/f6808f50-a1fd-434f-8a42-efa3afbe7871).

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Descriptor used by the event provider to determine which users can receive the event.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Data type: **sint64**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (3)
</dt> </dl>

The event sequence number.

</dd> <dt>

**StackTrace**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (9), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The stack trace.

</dd> <dt>

**ThreadAccountName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (8), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The account name associated with the thread.

</dd> <dt>

**ThreadID**
</dt> <dd> <dl> <dt>

Data type: **sint32**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (7)
</dt> </dl>

The identifier of the thread.

</dd> <dt>

**TIME\_CREATED**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Unique value that indicates the time at which the event was generated. This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601. The information is in the Coordinated Universal Times (UTC) format. This property is inherited from [**\_\_Event**](https://msdn.microsoft.com/windows/desktop/4d2e4715-041c-49e9-b948-a148dfe85483).

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://www.bing.com/search?q=Scripting in WMI).

</dd> <dt>

**TrustLevel**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (9), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The level of code access security (CAS) that is applied to the application.

</dd> <dt>

**UserAuthenticated**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (4)
</dt> </dl>

Is the user authenticated. True if authenticated; otherwise, false

</dd> <dt>

**UserAuthenticationType**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (5), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The type of user authentication.

</dd> <dt>

**UserHostAddress**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (2), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The user host address.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **WmiDataId** (3), **StringTermination** ("NullTerminated"), **format** ("w")
</dt> </dl>

The user name.

</dd> </dl>

## Requirements



|                                     |                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                               |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root\\aspnet<br/>                                                                |
| MOF<br/>                      | <dl> <dt>AspNet.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>MSCoree.dll</dt> </dl> |



 

 



