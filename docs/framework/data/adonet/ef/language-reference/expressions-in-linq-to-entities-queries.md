---
title: LINQ to Entities 쿼리의 식
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d70b502f-6a15-4120-b4fe-500b173ad9cc
ms.openlocfilehash: 234b3059f9109c23b8ecae4da37e15f7f094fbd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62034192"
---
# <a name="expressions-in-linq-to-entities-queries"></a>LINQ to Entities 쿼리의 식
식은 단일 값, 개체, 메서드, 네임스페이스 등으로 계산될 수 있는 코드의 일부입니다. 식에는 리터럴 값, 메서드 호출, 연산자와 해당 피연산자, 단순한 이름 등이 포함될 수 있습니다. 단순한 이름이란 변수, 형식 멤버, 메서드 매개 변수, 네임스페이스 또는 형식의 이름일 수 있습니다. 식은 다른 식을 매개 변수로 사용하는 연산자를 사용할 수 있으며 다른 메서드 호출을 매개 변수로 가지는 메서드 호출을 사용할 수도 있습니다. 따라서 식은 단순한 형태에서 매우 복잡한 형태까지 다양합니다.  
  
 [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] 쿼리에서 식은 <xref:System.Linq.Expressions> 네임스페이스 내의 형식에 허용되는 모든 항목을 포함할 수 있습니다(람다 식 포함). [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] 쿼리에 사용할 수 있는 식은 [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)]를 쿼리하는 데 사용할 수 있는 식의 상위 집합입니다.  [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)]에 대한 쿼리의 일부를 구성하는 식은 `ObjectQuery<T>` 및 기본 데이터 원본에서 지원되는 연산으로 한정됩니다.  
  
 다음 예제에서 `Where` 절의 비교는 식입니다.  
  
 [!code-csharp[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#whereexpression)]
 [!code-vb[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#whereexpression)]  
  
> [!NOTE]
>  C# `unchecked` 등과 같은 특정 언어 구문은 [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)]에서 의미가 없습니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [상수 식](../../../../../../docs/framework/data/adonet/ef/language-reference/constant-expressions.md)  
  
 [식 비교](../../../../../../docs/framework/data/adonet/ef/language-reference/comparison-expressions.md)  
  
 [null 비교](../../../../../../docs/framework/data/adonet/ef/language-reference/null-comparisons.md)  
  
 [초기화 식](../../../../../../docs/framework/data/adonet/ef/language-reference/initialization-expressions.md)  
  
 [관계, 탐색 속성 및 외래 키](/ef/ef6/fundamentals/relationships)  
  
## <a name="see-also"></a>참고자료

- [ADO.NET Entity Framework](../../../../../../docs/framework/data/adonet/ef/index.md)
