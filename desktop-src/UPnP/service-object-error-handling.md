---
title: Service Object Error Handling
description: When an error occurs in a service object, the return value for the call IDispatch Invoke should be DISP\_E\_EXCEPTION, and the pExceptInfo parameter pointer to an EXCEPTINFO structure in the should be filled in.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
---

# Service Object Error Handling

When an error occurs in a service object, the return value for the call [**IDispatch::Invoke**](https://msdn.microsoft.com/en-us/library/ms221479(v=VS.71).aspx) should be DISP\_E\_EXCEPTION, and the *pExceptInfo* parameter pointer to an [**EXCEPTINFO**](https://msdn.microsoft.com/en-us/library/ms221133(v=VS.71).aspx) structure in the should be filled in.

Specifically, the **bstrSource**, and **bstrDescription** members of the [**EXCEPTINFO**](https://msdn.microsoft.com/en-us/library/ms221133(v=VS.71).aspx) structure are used by the Device Host with UPnP technology to create a UPnP Fault response; **bstrSource** is the error code and **bstrDescription** is the error description.

 

 




