---
title: "ICorDebugValue::GetSize Method | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "reference"
apiname: 
  - "ICorDebugValue.GetSize"
apilocation: 
  - "mscordbi.dll"
apitype: "COM"
f1_keywords: 
  - "ICorDebugValue::GetSize"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GetSize method, ICorDebugValue interface [.NET Framework debugging]"
  - "ICorDebugValue::GetSize method [.NET Framework debugging]"
ms.assetid: 445a9ee3-e050-4f3a-931a-96b0efb00110
caps.latest.revision: 14
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
---
# ICorDebugValue::GetSize Method
Gets the size, in bytes, of this "ICorDebugValue" object.  
  
## Syntax  
  
```  
HRESULT GetSize (  
    [out] ULONG32   *pSize  
);  
```  
  
#### Parameters  
 `pSize`  
 [out] The size, in bytes, of this value object.  
  
## Remarks  
 If the value's type is a reference type, this method returns the size of the pointer rather than the size of the object.  
  
 The `ICorDebugValue::GetSize` method returns `COR_E_OVERFLOW` for objects that are larger than 4 GB on 64-bit platforms. Use the [ICorDebugValue3::GetSize64](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) method instead for objects that are larger than 4 GB.  
  
## Requirements  
 **Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorDebug.idl, CorDebug.h  
  
 **Library:** CorGuids.lib  
  
 **.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## See Also  
    
 [GetSize64 Method](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md)