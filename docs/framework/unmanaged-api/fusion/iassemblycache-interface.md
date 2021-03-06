---
title: IAssemblyCache 인터페이스
ms.date: 03/30/2017
api_name:
- IAssemblyCache
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache
helpviewer_keywords:
- IAssemblyCache interface [.NET Framework fusion]
ms.assetid: 71ea170f-872d-4fc5-81b6-27da1dec9b19
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fc5f3a3d5bc5699a596bcc648a7153190c130f0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697682"
---
# <a name="iassemblycache-interface"></a>IAssemblyCache 인터페이스
Fusion 기술에서 사용 하 여 전역 어셈블리 캐시를 나타냅니다.  
  
## <a name="methods"></a>메서드  
  
|메서드|설명|  
|------------|-----------------|  
|[CreateAssemblyCacheItem 메서드](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblycacheitem-method.md)|새 참조를 가져옵니다 [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)합니다.|  
|[CreateAssemblyScavenger 메서드](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblyscavenger-method.md)|Fusion 기술에서 내부 용도로 예약 되어 있습니다.|  
|[InstallAssembly 메서드](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-installassembly-method.md)|전역 어셈블리 캐시에 지정된 된 어셈블리를 설치합니다.|  
|[QueryAssemblyInfo 메서드](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-queryassemblyinfo-method.md)|지정된 된 어셈블리에 대 한 요청 된 데이터를 가져옵니다.|  
|[UninstallAssembly 메서드](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-uninstallassembly-method.md)|전역 어셈블리 캐시에서 지정된 된 어셈블리를 제거합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** Fusion.h  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [Fusion 인터페이스](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [전역 어셈블리 캐시](../../../../docs/framework/app-domains/gac.md)
