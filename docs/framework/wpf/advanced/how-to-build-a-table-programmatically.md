---
title: '방법: 프로그래밍 방식으로 테이블 작성'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tables [WPF], creating programmatically
ms.assetid: e3ca88f3-6e94-4b61-82fc-42104c10b761
ms.openlocfilehash: 315154b37218c0a6845f0a46149fc056780ee650
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051314"
---
# <a name="how-to-build-a-table-programmatically"></a>방법: 프로그래밍 방식으로 테이블 작성
다음 예제에서는 프로그래밍 방식으로 만드는 방법을 <xref:System.Windows.Documents.Table> 콘텐츠로 채웁니다. 5 개의 행에는 테이블의 내용을 지정 됩니다 (나타낸 <xref:System.Windows.Documents.TableRow> 에 포함 된 개체를 <xref:System.Windows.Documents.Table.RowGroups%2A> 개체) 및 6 개의 열 (나타내는 <xref:System.Windows.Documents.TableColumn> 개체). 행은 전체 테이블의 제목을 지정하는 제목 행, 테이블의 데이터 열을 설명하는 헤더 행 및 요약 정보가 포함된 바닥글 행 등의 여러 다른 프레젠테이션 용도로 사용됩니다.  “제목”, “헤더” 및 “바닥글” 행의 개념은 테이블에 고유한 것이 아니며, 여러 다른 특성이 있는 행일 뿐입니다. 테이블 셀의 텍스트, 이미지 또는 거의 모든 기타 구성 될 수 있는 실제 콘텐츠를 포함 [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] 요소입니다.  
  
## <a name="example"></a>예제  
 먼저를 <xref:System.Windows.Documents.FlowDocument> 만들어집니다 호스트에는 <xref:System.Windows.Documents.Table>, 및 새 <xref:System.Windows.Documents.Table> 만들어지고의 콘텐츠에 추가 <xref:System.Windows.Documents.FlowDocument>합니다.  
  
 [!code-csharp[TableSnippets#_TableCreate](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tablecreate)]
 [!code-vb[TableSnippets#_TableCreate](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tablecreate)]  
  
## <a name="example"></a>예제  
 다음으로 6 <xref:System.Windows.Documents.TableColumn> 개체를 만들어 테이블의 추가 <xref:System.Windows.Documents.Table.Columns%2A> 서식이 적용 된 컬렉션입니다.  
  
> [!NOTE]
>  테이블의 <xref:System.Windows.Documents.Table.Columns%2A> 컬렉션 표준 인덱스를 사용 합니다.  
  
 [!code-csharp[TableSnippets#_TableCreateColumns](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tablecreatecolumns)]
 [!code-vb[TableSnippets#_TableCreateColumns](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tablecreatecolumns)]  
  
## <a name="example"></a>예제  
 다음으로 제목 행을 만들어 서식이 적용된 테이블에 추가합니다.  제목 행은 테이블의 6개 열에 모두 걸친 단일 셀을 포함하게 됩니다.  
  
 [!code-csharp[TableSnippets#_TableAddTitleRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddtitlerow)]
 [!code-vb[TableSnippets#_TableAddTitleRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddtitlerow)]  
  
## <a name="example"></a>예제  
 다음으로 헤더 행을 만들어 테이블에 추가하고, 헤더 행의 셀을 만들어 콘텐츠로 채웁니다.  
  
 [!code-csharp[TableSnippets#_TableAddHeaderRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddheaderrow)]
 [!code-vb[TableSnippets#_TableAddHeaderRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddheaderrow)]  
  
## <a name="example"></a>예제  
 다음으로 데이터 행을 만들어 테이블에 추가하고, 이 행의 셀을 만들어 콘텐츠로 채웁니다.  이 행을 작성하는 것은 헤더 행을 작성하는 것과 비슷합니다. 단, 약간 다른 서식이 지정됩니다.  
  
 [!code-csharp[TableSnippets#_TableAddDataRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableadddatarow)]
 [!code-vb[TableSnippets#_TableAddDataRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableadddatarow)]  
  
## <a name="example"></a>예제  
 마지막으로 바닥글 행을 만들어 추가하고 서식을 지정합니다.  제목 행과 마찬가지로 바닥글에는 테이블의 6개 열에 모두 걸친 단일 셀이 포함됩니다.  
  
 [!code-csharp[TableSnippets#_TableAddFooterRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddfooterrow)]
 [!code-vb[TableSnippets#_TableAddFooterRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddfooterrow)]  
  
## <a name="see-also"></a>참고자료

- [테이블 개요](table-overview.md)
