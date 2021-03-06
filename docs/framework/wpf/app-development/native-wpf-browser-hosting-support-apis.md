---
title: 네이티브 WPF 브라우저 호스팅 지원 API
ms.date: 03/30/2017
f1_keywords:
- AutoGeneratedOrientationPage
helpviewer_keywords:
- browser hosting support [WPF]
- WPF browser hosting support APIs [WPF]
ms.assetid: 82c133a8-d760-45fb-a2b9-3a997537f1d4
ms.openlocfilehash: eed20417b44b9af78c92871a619f2ccf857b6bba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61864466"
---
# <a name="native-wpf-browser-hosting-support-apis"></a>네이티브 WPF 브라우저 호스팅 지원 API
호스팅 [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] 응용 프로그램 웹 브라우저에서 액티브 문서 서버 (DocObject 라고도 함) WPF 호스트에서 등록 하 여 촉진 됩니다. [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] 활성화 하 고 활성 문서를 사용 하 여 통합 직접 수 있습니다. Xbap 및 Mozilla 브라우저에서 느슨한 XAML 문서를 호스트 하는 것에 대 한 [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] 하는 유사한 호스팅 환경을 제공 하는 NPAPI 플러그인을 제공 합니다 [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] 액티브 문서 서버 [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] 않습니다. 그러나 Xbap XAML을 호스트 하는 가장 쉬운 실용적인 방법은 다른 브라우저에서 문서를 독립 실행형 응용 프로그램은 Internet Explorer 웹 브라우저 컨트롤을 통해. 웹 브라우저 컨트롤의 복잡 한 활성 문서 서버 호스팅 환경을 제공 하면서 자체 호스트 및 사용자 지정 하 고, 해당 환경을 확장 하 고, 현재 활성 문서 개체와 직접 통신할 수 있도록 합니다.  
  
 합니다 [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] 액티브 문서 서버는 몇 가지 일반적인 호스팅 인터페이스를 포함 하 여 구현 [IOleObject](https://go.microsoft.com/fwlink/?LinkId=162049), [IOleDocument](https://go.microsoft.com/fwlink/?LinkId=162050)를 [IOleInPlaceActiveObject](https://go.microsoft.com/fwlink/?LinkId=162051), [IPersistMoniker](https://go.microsoft.com/fwlink/?LinkId=162045)하십시오 [IOleCommandTarget](https://go.microsoft.com/fwlink/?LinkId=162047)합니다. 이러한 인터페이스에서 반환 된 개체에서 쿼리 될 수 있습니다 웹 브라우저 컨트롤에서 호스팅되면 합니다 [IWebBrowser2::Document](https://go.microsoft.com/fwlink/?LinkId=162048) 속성입니다.  
  
## <a name="iolecommandtarget"></a>IOleCommandTarget  
 WPF 액티브 문서 서버 구현의 [IOleCommandTarget](https://go.microsoft.com/fwlink/?LinkId=162047) (null 명령 그룹 GUID)이 있는 표준 OLE 명령 그룹의 다양 한 탐색 관련 및 브라우저 전용 명령을 지원 합니다. 또한 CGID_PresentationHost 라는 사용자 지정 명령 그룹을 인식 합니다. 현재이 그룹 내에 정의 된 하나의 명령입니다.  
  
```  
DEFINE_GUID(CGID_PresentationHost, 0xd0288c55, 0xd6, 0x4f5e, 0xa8, 0x51, 0x79, 0xde, 0xc5, 0x1b, 0x10, 0xec);  
enum PresentationHostCommands {   
   PHCMDID_TABINTO = 1   
};  
```  
  
 PHCMDID_TABINTO PresentationHost Shift 키의 상태에 따라 해당 내용의 첫 번째 또는 마지막 포커스 가능 요소에 포커스를 전환 하도록 지시 합니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md)  
 [IWpfHostSupport](iwpfhostsupport.md)
