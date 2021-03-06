---
title: <oidMap> 요소
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#oidMap
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/oidMap
helpviewer_keywords:
- <oidMap> element
- oidMap element
ms.assetid: 7f0c2246-c070-4748-b96a-2f66a296c539
ms.openlocfilehash: 80564c5895e08884f78a4ec7c955ecdb11126e35
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705170"
---
# <a name="oidmap-element"></a>\<oidMap > 요소
ASN.1 클래스 개체 식별자 (OID) 매핑이 들어 있습니다.  
  
 \<configuration>  
\<mscorlib>  
\<cryptographySettings>  
\<oidMap>  
  
## <a name="syntax"></a>구문  
  
```xml  
<oidMap>   
</oidMap>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
 없음  
  
### <a name="child-elements"></a>자식 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<oidEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md)|ASN.1 OID 이름에 매핑됩니다.|  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|`configuration`|공용 언어 런타임 및 .NET Framework 애플리케이션에서 사용하는 모든 구성 파일의 루트 요소입니다.|  
|`cryptographySettings`|암호화 설정이 포함되어 있습니다.|  
|`mscorlib`|포함 된 `cryptographySettings` 요소입니다.|  
  
## <a name="example"></a>예제  
 다음 예제에서는 사용 하는 방법을 보여 줍니다 합니다  **\<oidMap >** 해당 해시 알고리즘의 구현에 RIPEMD-160 해시 알고리즘의 OID의 매핑을 포함 하는 요소입니다.  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RIPEMD-160" class="MyCrypto"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"  name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a>참고자료

- [구성 파일 스키마](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [암호화 설정 스키마](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)
- [Cryptographic Services](../../../../../docs/standard/security/cryptographic-services.md)
- [암호화 클래스 구성](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
- [개체 식별자를 암호화 알고리즘에 매핑](../../../../../docs/framework/configure-apps/map-object-identifiers-to-cryptography-algorithms.md)
