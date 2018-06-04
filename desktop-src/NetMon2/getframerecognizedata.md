---
Description: The GetFrameRecognizeData function returns a table of RECOGNIZEDATA structures. Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: GetFrameRecognizeData function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# GetFrameRecognizeData function

The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures. Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.

## Syntax


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## Parameters

<dl> <dt>

*hFrame* \[in\]
</dt> <dd>

Handle to a frame.

</dd> </dl>

## Return value

If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.

If the function is not successful, the return value is zero.

## Remarks

[*Experts*](https://www.bing.com/search?q=*Experts*) and [*parsers*](https://www.bing.com/search?q=*parsers*) can call the **GetFrameRecognizeData** function.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                           |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Library<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 



