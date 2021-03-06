---
Description: Removes all Certificate objects from a Recipients collection.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Recipients.Clear method
ms.topic: article
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
---

# Recipients.Clear method

\[The **Clear** method is available for use in the operating systems specified in the Requirements section. Instead, use the [**CmsRecipientCollection Class**](https://msdn.microsoft.com/library/0y59h9e9(v=VS.90).aspx) in the [**System.Security.Cryptography.Pkcs**](https://msdn.microsoft.com/library/6see7k14(v=VS.100).aspx) namespace.\]

The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.

## Syntax


```VB
Recipients.Clear()
```



## Parameters

This method has no parameters.

## Return value

This method does not return a value. An application that uses this method must contain code to handle an exception raised by this method.

## Requirements



|                            |                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistributable<br/> | CAPICOM 2.0 or later on Windows Server 2003 and Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## See also

<dl> <dt>

[**Cryptography Objects**](cryptography-objects.md)
</dt> <dt>

[**Recipients**](recipients.md)
</dt> </dl>

 

 




