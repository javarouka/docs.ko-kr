---
title: '방법: 데이터베이스에 행 삽입'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 44d99680-69c7-4879-a732-f6771b334211
ms.openlocfilehash: cb2319d51e0518114a04eea2fc7ab6b5a836b7ff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61903073"
---
# <a name="how-to-insert-rows-into-the-database"></a>방법: 데이터베이스에 행 삽입
연결 된 개체를 추가 하 여 데이터베이스에 행을 삽입할 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Table%601> 컬렉션과 다음 데이터베이스에 변경 내용을 제출 합니다. [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 변경 내용을 적절 한 SQL에 변환 `INSERT` 명령입니다.  
  
> [!NOTE]
>  [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], `Insert` 및 `Update` 데이터베이스 작업에 대한 `Delete` 기본 메서드를 재정의할 수 있습니다. 자세한 내용은 [사용자 지정 Insert, Update 및 Delete 작업](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md)합니다.  
>   
>  Visual Studio를 사용 하 여 개발자가 사용할 수는 [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] 같은 목적을 위해 저장된 프로시저를 개발 합니다.  
  
 다음 단계에서는 올바른 <xref:System.Data.Linq.DataContext>를 사용하여 사용자가 Northwind 데이터베이스에 연결되는 것으로 가정합니다. 자세한 내용은 [방법: 데이터베이스에 연결할](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md)합니다.  
  
### <a name="to-insert-a-row-into-the-database"></a>데이터베이스에 행을 삽입하려면  
  
1. 전송할 행 데이터가 있는 새 개체를 만듭니다.  
  
2. 새 개체를 추가 합니다 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] `Table` 데이터베이스에서 대상 테이블에 연결 된 컬렉션입니다.  
  
3. 데이터베이스에 변경 내용을 전송합니다.  
  
## <a name="example"></a>예제  
 다음 코드 예제에서는 `Order` 형식의 새 개체를 만들어 적절한 값을 채웁니다. 그런 다음 새 개체를 `Order` 컬렉션에 추가합니다. 마지막으로 변경 내용을 `Orders` 테이블의 새 행으로 데이터베이스에 전송합니다.  
  
 [!code-csharp[System.Data.Linq.Table#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.table/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.Table#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.table/vb/module1.vb#1)]  
  
## <a name="see-also"></a>참고자료

- [방법: 변경 내용 충돌 관리](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
- [DataContext 메서드(O/R 디자이너)](/visualstudio/data-tools/datacontext-methods-o-r-designer)
- [방법: 저장 프로시저를 할당하여 업데이트, 삽입 및 삭제 수행(O/R 디자이너)](/visualstudio/data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer)
- [데이터 변경 및 변경 내용 전송](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
