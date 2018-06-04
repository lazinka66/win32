---
Description: This class is used to report RSC capabilities on a network adapter.
ms.assetid: 7318262e-384e-45a4-8e2e-839840dda146
title: MSFT\_NetAdapterRscCapabilities class
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MSFT\_NetAdapterRscCapabilities class

This class is used to report RSC capabilities on a network adapter.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.

## Syntax

``` syntax
[Dynamic, Provider("NetAdapterCim")]
class MSFT_NetAdapterRscCapabilities
{
  boolean IPv4Supported;
  boolean IPv6Supported;
};
```

## Members

The **MSFT\_NetAdapterRscCapabilities** class has these types of members:

-   [Properties](#properties)

### Properties

The **MSFT\_NetAdapterRscCapabilities** class has these properties.

<dl> <dt>

**IPv4Supported**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates if Adapter supports RSC for IPv4 TCP packets

</dd> <dt>

**IPv6Supported**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates if Adapter supports RSC for IPv6 TCP packets

</dd> </dl>

## Requirements



|                                     |                                                                                              |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                    |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                               |
| Namespace<br/>                | Root\\StandardCimv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>NetAdapterCim.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>NetAdapterCim.dll</dt> </dl> |



 

 



