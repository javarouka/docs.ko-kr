---
title: ICorDebugStepperEnum::Next 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum::Next
helpviewer_keywords:
- Next method, ICorDebugStepperEnum interface [.NET Framework debugging]
- ICorDebugStepperEnum::Next method [.NET Framework debugging]
ms.assetid: d0ea0f30-e8d2-48b0-8477-e1a029ceb4dd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ac3165ab17eb1b4bc55a4bee4d2d2b467f8aefe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61987404"
---
# <a name="icordebugstepperenumnext-method"></a>ICorDebugStepperEnum::Next 메서드
ICorDebugStepper 인스턴스 수가 지정 된 현재 위치부터 시작 하는 열거형에서 가져옵니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT Next(  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugStepper *steppers[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a>매개 변수  
 `celt`  
 [in] 수가 `ICorDebugStepper` 인스턴스를 검색할 수 있습니다.  
  
 `steppers`  
 [out] 각각 가리키는 포인터 배열을 `ICorDebugStepper` 개체입니다.  
  
 `pceltFetched`  
 [out] 개수에 대 한 포인터 `ICorDebugStepper` 실제로 반환 된 인스턴스. 이 값은 null 일 수 있으면 `celt` 하나입니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** CorDebug.idl, CorDebug.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
