---
title: "COS (Transact SQL) |Microsoft 文档"
ms.custom: 
ms.date: 07/24/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- COS
- COS_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- cosine
- COS function
ms.assetid: c9fa8ae1-3373-4f3e-9b97-fa05077c1040
caps.latest.revision: 21
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: f095bcaf0ad264ef3423221c907f35d9e3290690
ms.contentlocale: zh-cn
ms.lasthandoff: 09/01/2017

---
# <a name="cos-transact-sql"></a>COS (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all_md](../../includes/tsql-appliesto-ss2008-all-md.md)]

一个数学函数，返回指定表达式中以弧度表示的指定角的三角余弦。
  
![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "主题链接图标") [TRANSACT-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)
  
## <a name="syntax"></a>语法  
  
```sql
COS ( float_expression )  
```  
  
## <a name="arguments"></a>参数  
*float_expression*  
是[表达式](../../t-sql/language-elements/expressions-transact-sql.md)类型的**float**。
  
## <a name="return-types"></a>返回类型
**float**
  
## <a name="examples"></a>示例  
以下示例将返回指定角度的 COS 值。
  
```sql
DECLARE @angle float;  
SET @angle = 14.78;  
SELECT 'The COS of the angle is: ' + CONVERT(varchar,COS(@angle));  
GO  
```  
  
[!INCLUDE[ssResult](../../includes/ssresult-md.md)]
  
```sql
The COS of the angle is: -0.599465                        
  
(1 row(s) affected)  
```  

## <a name="examples"></a>示例
  
[!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)]和[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  


以下示例将返回指定角度的 COS 值。
  
```sql
SELECT COS(14.76) AS cosCalc1, COS(-0.1472738) AS cosCalc2;   
```  
  
[!INCLUDE[ssResult](../../includes/ssresult-md.md)]
  
`cosCalc1  cosCalc2`
  
`--------  --------`
  
`-0.58     0.99`
  
## <a name="see-also"></a>另请参阅
[数学函数 &#40;Transact SQL &#41;](../../t-sql/functions/mathematical-functions-transact-sql.md)
  
  


