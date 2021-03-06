---
title: AssemblyBindInfo 구조체
ms.date: 03/30/2017
api_name:
- AssemblyBindInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyBindInfo
helpviewer_keywords:
- AssemblyBindInfo structure [.NET Framework hosting]
ms.assetid: 6fc01e98-c2e7-49de-ab9f-95937cc89017
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce79987c7fcf45b8d10dcc4613e053ee735941de
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946847"
---
# <a name="assemblybindinfo-structure"></a>AssemblyBindInfo 구조체
참조 된 어셈블리에 대 한 자세한 정보를 제공합니다.  
  
## <a name="syntax"></a>구문  
  
```  
typedef struct _AssemblyBindInfo {  
    DWORD       dwAppDomainId;  
    LPCWSTR     lpReferencedIdentity;  
    LPCWSTR     lpPostPolicyIdentity;  
    DWORD       ePolicyLevel;  
} AssemblyBindInfo;  
```  
  
## <a name="members"></a>멤버  
  
|멤버|설명|  
|------------|-----------------|  
|`dwAppDomainId`|에 대 한 고유 식별자를 `IStream` 에 대 한 호출에서 반환 된 [ihostassemblystore:: Provideassembly](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md)에 참조 된 어셈블리를 로드 하는 합니다.|  
|`lpReferencedIdentity`|참조 된 어셈블리에 대 한 고유 식별자입니다.|  
|`lpPostPolicyIdentity`|바인딩 정책 값을 적용 한 후 참조 된 어셈블리에 대 한 식별자입니다.|  
|`ePolicyLevel`|중 하나는 [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) 어떤 버전 관리 정책이 있는 경우 적용할 참조 된 어셈블리를 나타내는 값입니다.|  
  
## <a name="remarks"></a>설명  
 고유 식별자를 제공 하는 호스트 `dwAppDomainId` 는 CLR (공용 언어 런타임)에 있습니다. 호출한 후 `IHostAssemblyStore::ProvideAssembly` 런타임 식별자를 사용 하 여 결정을 반환 하는지 여부를 내용의 `IStream` 매핑되어 있는 합니다. 그렇다면 런타임 스트림에 다시 매핑하는 것이 아니라 기존 복사본을 로드 합니다. 런타임에서에서 반환 된 스트림을 대 한 조회 키로이 식별자도 사용에 대 한 호출 [ihostassemblystore:: Providemodule](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-providemodule-method.md)합니다. 따라서 식별자 어셈블리 요청 및 요청 모듈에 대 한 고유 해야 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** MSCorEE.idl  
  
 **라이브러리:** MSCorEE.dll에 리소스로 포함  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [호스팅 구조체](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
- [ICLRAssemblyIdentityManager 인터페이스](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [ICLRAssemblyReferenceList 인터페이스](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [IHostAssemblyManager 인터페이스](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [IHostAssemblyStore 인터페이스](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
- [ModuleBindInfo 구조체](../../../../docs/framework/unmanaged-api/hosting/modulebindinfo-structure.md)
