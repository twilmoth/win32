---
title: IMsRdpClient3 AdvancedSettings4 property
description: Retrieves a pointer to the IMsRdpClientAdvancedSettings3 interface.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- AdvancedSettings4 property Remote Desktop Services
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient3 interface
- IMsRdpClient3 interface Remote Desktop Services , AdvancedSettings4 property
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient4 interface
- IMsRdpClient4 interface Remote Desktop Services , AdvancedSettings4 property
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient5 interface
- IMsRdpClient5 interface Remote Desktop Services , AdvancedSettings4 property
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient6 interface
- IMsRdpClient6 interface Remote Desktop Services , AdvancedSettings4 property
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient7 interface
- IMsRdpClient7 interface Remote Desktop Services , AdvancedSettings4 property
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient8 interface
- IMsRdpClient8 interface Remote Desktop Services , AdvancedSettings4 property
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient9 interface
- IMsRdpClient9 interface Remote Desktop Services , AdvancedSettings4 property
- AdvancedSettings4 property Remote Desktop Services , IMsRdpClient10 interface
- IMsRdpClient10 interface Remote Desktop Services , AdvancedSettings4 property
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: article
ms.date: 05/31/2018
---

# IMsRdpClient3::AdvancedSettings4 property

Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.

This property is read-only.

## Syntax


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## Property value

Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface. The interface can be used to set advanced settings for the client control.

## Error codes

If the method succeeds, **S\_OK** is returned. Any other **HRESULT** value indicates that the call failed.

## Remarks

This property cannot be set when the control is connected.

For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).

## Requirements



|                                     |                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                               |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                         |
| Type library<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff<br/>       |



## See also

<dl> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





