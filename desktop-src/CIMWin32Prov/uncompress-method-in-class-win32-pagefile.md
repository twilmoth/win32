---
Description: Uncompresses the logical paging file (or directory) specified in the object path.
ms.assetid: 9bd98ba8-068e-49af-8dd4-e5ee987eb31d
ms.tgt_platform: multiple
title: Uncompress method of the Win32_PageFile class
ms.topic: article
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- Win32_PageFile.Uncompress
api_type: 
- COM
api_location: 
- CIMWin32.dll
---

# Uncompress method of the Win32\_PageFile class

The **Uncompress** [WMI class](https://docs.microsoft.com/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.

This topic uses Managed Object Format (MOF) syntax. For more information about using this method, see [Calling a Method](https://docs.microsoft.com/windows/desktop/WmiSdk/calling-a-method).

## Syntax


```mof
uint32 Uncompress();
```



## Parameters

This method has no parameters.

## Return value

Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.

<dl> <dt>

**0**
</dt> <dd>

The request was successful.

</dd> <dt>

**2**
</dt> <dd>

Access was denied.

</dd> <dt>

**8**
</dt> <dd>

An unspecified failure occurred.

</dd> <dt>

**9**
</dt> <dd>

The name specified was not valid.

</dd> <dt>

**10**
</dt> <dd>

The object specified already exists.

</dd> <dt>

**11**
</dt> <dd>

The file system is not NTFS.

</dd> <dt>

**12**
</dt> <dd>

The platform is not Windows.

</dd> <dt>

**13**
</dt> <dd>

The drive is not the same.

</dd> <dt>

**14**
</dt> <dd>

The directory is not empty.

</dd> <dt>

**15**
</dt> <dd>

There has been a sharing violation.

</dd> <dt>

**16**
</dt> <dd>

The start file specified was not valid.

</dd> <dt>

**17**
</dt> <dd>

A privilege required for the operation is not held.

</dd> <dt>

**21**
</dt> <dd>

A parameter specified is not valid.

</dd> </dl>

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[Operating System Classes](https://docs.microsoft.com/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32\_PageFile**](win32-pagefile.md)
</dt> </dl>

 

 




