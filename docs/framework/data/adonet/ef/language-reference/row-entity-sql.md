---
title: ROW(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 06da96e8-55d7-486c-991a-4e514d837ff9
ms.openlocfilehash: 676080a6cc4208ea1a4d72b85a4a55e01fafe638
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64641456"
---
# <a name="row-entity-sql"></a>ROW(Entity SQL)
값 하나 이상을 기반으로 하여 구조적으로 형식화된 익명 레코드를 생성합니다.  
  
## <a name="syntax"></a>구문  
  
```  
ROW ( expression [ AS alias ] [,...] )  
```  
  
## <a name="arguments"></a>인수  
 `expression`  
 행 형식에서 생성되는 값을 반환하는 모든 유효한 쿼리 식입니다.  
  
 `alias`  
 행 형식에서 지정된 값의 별칭을 지정합니다. 별칭이 제공되지 않은 경우 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 에서는 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 별칭 생성 규칙에 따라 별칭을 생성합니다.  
  
## <a name="return-value"></a>반환 값  
 행 형식입니다.  
  
## <a name="remarks"></a>설명  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 의 행 생성자를 사용하여 값 하나 이상을 기반으로 구조적으로 형식화된 익명 레코드를 생성합니다. 행 생성자의 결과 형식은 필드 형식이 행 생성에 사용된 값의 형식과 동일한 행 형식입니다. 예를 들어, 다음 식은 형식 `Record(a int, b string, c int)`의 값을 생성합니다.  
  
```  
ROW(1 AS a, "abc" AS b, a+34 AS c)  
```  
  
 행 생성자에서 식의 별칭을 제공하지 않으면 Entity Framework에서 별칭을 생성합니다. 자세한 내용은 [식별자](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md) 항목의 "별칭 지정 규칙" 단원을 참조하세요.  
  
 행 생성자에서 식에 별칭을 지정하는 데 다음 규칙이 적용됩니다.  
  
- 행 생성자의 식은 동일한 생성자 내의 다른 별칭을 참조할 수 없습니다.  
  
- 동일한 행 생성자 내의 서로 다른 두 식은 별칭이 같을 수 없습니다.  
  
 쿼리 생성자에 대 한 자세한 내용은 참조 하세요. [형식 생성](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md)합니다.  
  
## <a name="example"></a>예제  
 다음 Entity SQL 쿼리에서는 ROW 연산자를 사용하여 구조적으로 형식화된 익명 레코드를 생성합니다. 쿼리는 AdventureWorks Sales 모델을 기반으로 합니다. 이 쿼리를 컴파일하고 실행하려면 다음 단계를 수행하세요.  
  
1. 절차에 따라 [방법: StructuralType 결과 반환 하는 쿼리 실행](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)합니다.  
  
2. 다음 쿼리를 `ExecuteStructuralTypeQuery` 메서드에 인수로 전달합니다.  
  
 [!code-csharp[DP EntityServices Concepts 2#ROW](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#row)]  
  
## <a name="see-also"></a>참고자료

- [형식 생성](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md)
- [엔터티 SQL 참조](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [형식 정의](../../../../../../docs/framework/data/adonet/ef/language-reference/type-definitions-entity-sql.md)
