---
title: 제네릭 IEnumerable로 형식 변환
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 64774fb5-7447-4296-ad3b-8a94346f99a1
ms.openlocfilehash: d75c9b9123b52b3e241bea1bbd1d302c406715e8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62032710"
---
# <a name="convert-a-type-to-a-generic-ienumerable"></a>제네릭 IEnumerable로 형식 변환
<xref:System.Linq.Enumerable.AsEnumerable%2A>을 사용하여 제네릭 `IEnumerable`로 형식화된 인수를 반환합니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 기본 제네릭 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]를 사용하여 `Query`에서 쿼리를 SQL로 변환하여 해당 쿼리를 서버에서 실행합니다. 그러나 `where` 절에서는 SQL로 변환할 수 없는 사용자 정의 클라이언트측 메서드(`isValidProduct`)를 참조합니다.  
  
 이 솔루션에서는 <xref:System.Collections.Generic.IEnumerable%601>의 클라이언트측 제네릭 `where` 구현을 지정하여 제네릭 <xref:System.Linq.IQueryable%601>을 대체합니다. 이 작업은 <xref:System.Linq.Enumerable.AsEnumerable%2A> 연산자를 호출하여 수행합니다.  
  
 [!code-csharp[DLinqQueryExamples#46](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#46)]
 [!code-vb[DLinqQueryExamples#46](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#46)]  
  
## <a name="see-also"></a>참고자료

- [쿼리 예제](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
