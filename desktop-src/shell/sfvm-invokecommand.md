---
Description: Notifies the callback object that one of its toolbar or menu commands has been invoked by the user. Used by IShellFolderViewCB::MessageSFVCB.
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND message
ms.topic: article
ms.date: 05/31/2018
---

# SFVM\_INVOKECOMMAND message

Notifies the callback object that one of its toolbar or menu commands has been invoked by the user. Used by [**IShellFolderViewCB::MessageSFVCB**](https://msdn.microsoft.com/en-us/library/Bb774968(v=VS.85).aspx).


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## Parameters

<dl> <dt>

*idCmd* \[in\]
</dt> <dd>

The command ID of the selected toolbar or menu item.

</dd> </dl>

## Remarks

This message serves essentially the same function as a [**WM\_COMMAND**](https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx) message in a conventional window procedure. It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.

## Requirements



|                                     |                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                          |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




