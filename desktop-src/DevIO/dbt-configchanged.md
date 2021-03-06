---
Description: The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock. An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED event
ms.topic: article
ms.date: 05/31/2018
---

# DBT\_CONFIGCHANGED event

The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock. An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.

To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## Parameters

<dl> <dt>

*hwnd* 
</dt> <dd>

A handle to a window.

</dd> <dt>

*uMsg* 
</dt> <dd>

The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.

</dd> <dt>

*wParam* 
</dt> <dd>

Set to DBT\_CONFIGCHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Set to zero.

</dd> </dl>

## Return value

Return **TRUE**.

## Requirements



|                                     |                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP<br/>                                                            |
| Minimum supported server<br/> | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## See also

<dl> <dt>

[Device Events](device-events.md)
</dt> <dt>

[Device Management Events](device-management-events.md)
</dt> <dt>

[**WM\_DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




