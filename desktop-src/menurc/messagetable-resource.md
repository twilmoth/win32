---
title: MESSAGETABLE resource
description: Defines the ID and file of an application's message table resource. Message tables are special string resources used in event logging and with the FormatMessage function. The file contains a binary message table generated by the message compiler, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- MESSAGETABLE resource Menus and Other Resources
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: article
ms.date: 05/31/2018
---

# MESSAGETABLE resource

Defines the ID and file of an application's message table resource. Message tables are special string resources used in event logging and with the [**FormatMessage**](https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage) function. The file contains a binary message table generated by the message compiler, MC.EXE.

The message compiler also generates a resource script file that contains the **MESSAGETABLE** statements you need to include the message table resources in the compiled resource file. Use the [**\#include**](-include.md) directive to include this resource script into your main resource script.

``` syntax
nameID MESSAGETABLE filename
```

## Parameters

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Unique name or a 16-bit unsigned integer value identifying the resource.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Name of the file that contains the resource. The name must be a valid file name; it must be a full path if the file is not in the current working directory.

</dd> </dl>

Certain attributes are also supported for backward compatibility. For more information, see [Common Resource Attributes](common-resource-attributes.md).

## Examples

The following example defines a **MESSAGETABLE** resource:

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## See also

<dl> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




