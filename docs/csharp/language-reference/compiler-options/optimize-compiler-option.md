---
title: -optimize(C# 컴파일러 옵션)
ms.date: 07/20/2015
f1_keywords:
- /optimize
helpviewer_keywords:
- /optimize compiler option [C#]
- -o compiler option [C#]
- optimize compiler option [C#]
- /o compiler option [C#]
- -optimize compiler option [C#]
- compiler optimization [C#]
- o compiler option [C#]
ms.assetid: 6dd5b6f2-cd1d-4593-a9f4-1c2ed9404ca0
ms.openlocfilehash: 25a9ee1b27836dfb00dcbc72712ed068639fa2fc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59320034"
---
# <a name="-optimize-c-compiler-options"></a>-optimize(C# 컴파일러 옵션)
**-optimize** 옵션은 컴파일러에서 더 작지만 빠르고 효율적인 출력 파일을 만들기 위해 수행하는 최적화 기능을 사용하거나 사용하지 않도록 설정합니다.  
  
## <a name="syntax"></a>구문  
  
```console  
-optimize[+ | -]  
```  
  
## <a name="remarks"></a>주의  
 또한 **-optimize**는 런타임에 코드를 최적화하도록 공용 언어 런타임에 알립니다.  
  
 최적화는 기본적으로 사용되지 않습니다. 최적화를 사용하려면 **-optimize+** 를 지정합니다.  
  
 어셈블리에서 사용할 모듈을 빌드하는 경우 어셈블리의 설정과 동일한 **-optimize** 설정을 사용합니다.  
  
 **-o**는 **-optimize**의 약식 형태입니다.  
  
 **-optimize** 및 [-debug](../../../csharp/language-reference/compiler-options/debug-compiler-option.md) 옵션을 함께 사용할 수 있습니다.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면  
  
1. 프로젝트 **속성** 페이지를 엽니다.  
  
2. **빌드** 속성 페이지를 클릭합니다.  
  
3. **코드 최적화** 속성을 수정합니다.  
  
 이 컴파일러 옵션을 프로그래밍 방식으로 설정하는 방법에 대한 자세한 내용은 <xref:VSLangProj80.CSharpProjectConfigurationProperties3.Optimize%2A>을 참조하세요.  
  
## <a name="example"></a>예제  
 `t2.cs`를 컴파일하고 컴파일러 최적화를 사용하도록 설정합니다.  
  
```console  
csc t2.cs -optimize  
```  
  
## <a name="see-also"></a>참고 항목

- [C# 컴파일러 옵션](../../../csharp/language-reference/compiler-options/index.md)
- [프로젝트 및 솔루션 속성 관리](/visualstudio/ide/managing-project-and-solution-properties)
