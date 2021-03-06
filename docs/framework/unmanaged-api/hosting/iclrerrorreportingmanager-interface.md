---
title: ICLRErrorReportingManager 인터페이스
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager
helpviewer_keywords:
- ICLRErrorReportingManager interface [.NET Framework hosting]
ms.assetid: ea8af0d5-4133-4472-8a1f-50570d7e85fa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a20b79dd5eda9c431511cc49e7e3adaa9486b2aa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61969847"
---
# <a name="iclrerrorreportingmanager-interface"></a>ICLRErrorReportingManager 인터페이스
오류 보고에 대 한 사용자 지정 스택 덤프를 구성 하려면 호스트를 사용할 수 있는 메서드를 제공 합니다.  
  
## <a name="methods"></a>메서드  
  
|메서드|설명|  
|------------|-----------------|  
|[BeginCustomDump 메서드](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md)|오류 보고에 대 한 사용자 지정 스택 덤프 구성을 지정합니다.|  
|[EndCustomDump 메서드](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md)|이전 호출에 의해 설정 된 사용자 지정 스택 덤프 구성을 지웁니다 `BeginCustomDump`합니다.|  
|[GetBucketParametersForCurrentException 메서드](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-getbucketparametersforcurrentexception-method.md)|Watson 버킷이 호출 스레드에서 현재 예외를 가져옵니다.|  
  
## <a name="remarks"></a>설명  
 `BeginCustomDump` 메서드는 사용자 지정 스택 덤프 구성을 설정 합니다. `EndCustomDump` 메서드를 사용자 지정 스택 덤프 구성을 지워지고 연결 된 모든 상태를 해제 합니다. 사용자 지정 덤프 완료 된 후 호출 되어야 합니다.  
  
> [!IMPORTANT]
>  호출 하지 못하면 `EndCustomDump` 메모리 누수를 발생 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** MSCorEE.h  
  
 **라이브러리:** MSCorEE.dll에 리소스로 포함  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [ECustomDumpItemKind 열거형](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md)
- [호스팅 인터페이스](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
