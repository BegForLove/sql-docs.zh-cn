---
title: "ATAN (Transact SQL) |Microsoft 文档"
ms.custom: 
ms.date: 07/24/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: 
ms.component: t-sql|functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- ATAN_TSQL
- ATAN
dev_langs:
- TSQL
helpviewer_keywords:
- arctangent
- ATAN function
- tangent
ms.assetid: 6d3dd28e-4fa6-40ba-94cf-b33c0ff614ec
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: efb6cbe8dcc58d8989b8f8ce9b4deb6ce587dc83
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="atan-transact-sql"></a>ATAN (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

返回的角度以弧度表示，其正切为指定**float**表达式。 它也称为反正切函数。
  
![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "主题链接图标") [TRANSACT-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)
  
## <a name="syntax"></a>语法  
  
```sql
ATAN ( float_expression )  
```  
  
## <a name="arguments"></a>参数  
*float_expression*  
是[表达式](../../t-sql/language-elements/expressions-transact-sql.md)类型的**float**或可以隐式转换为的类型**float**。
  
## <a name="return-types"></a>返回类型
**float**
  
## <a name="examples"></a>示例  
下面的示例将**float**表达式并返回指定角度的反正切。
  
```sql
SELECT 'The ATAN of -45.01 is: ' + CONVERT(varchar, ATAN(-45.01))  
SELECT 'The ATAN of -181.01 is: ' + CONVERT(varchar, ATAN(-181.01))  
SELECT 'The ATAN of 0 is: ' + CONVERT(varchar, ATAN(0))  
SELECT 'The ATAN of 0.1472738 is: ' + CONVERT(varchar, ATAN(0.1472738))  
SELECT 'The ATAN of 197.1099392 is: ' + CONVERT(varchar, ATAN(197.1099392))  
GO  
```  
  
[!INCLUDE[ssResult](../../includes/ssresult-md.md)]
  
```sql
  
-------------------------------   
The ATAN of -45.01 is: -1.54858                         
  
(1 row(s) affected)  
  
--------------------------------   
The ATAN of -181.01 is: -1.56527                         
  
(1 row(s) affected)  
  
--------------------------------   
The ATAN of 0 is: 0                                
  
(1 row(s) affected)  
  
----------------------------------   
The ATAN of 0.1472738 is: 0.146223                         
  
(1 row(s) affected)  
  
-----------------------------------   
The ATAN of 197.1099392 is: 1.56572                          
  
(1 row(s) affected)  
```  
  
## <a name="examples-includesssdwfullincludessssdwfull-mdmd-and-includesspdwincludessspdw-mdmd"></a>示例：[!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)]和[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  
下面的示例将**float**表达式并返回指定角度的反正切值。
  
```sql
SELECT ATAN(45.87) AS atanCalc1,  
    ATAN(-181.01) AS atanCalc2,  
    ATAN(0) AS atanCalc3,  
    ATAN(0.1472738) AS atanCalc4,  
    ATAN(197.1099392) AS atanCalc5;  
```  
  
[!INCLUDE[ssResult](../../includes/ssresult-md.md)]
  
```
atanCalc1  atanCalc2  atanCalc3  atanCalc4  atanCalc5
---------  ---------  ---------  ---------  ---------
1.55       -1.57       0.00       0.15       1.57
```
  
## <a name="see-also"></a>另请参阅
[上限 &#40;Transact SQL &#41;](../../t-sql/functions/ceiling-transact-sql.md)  
[数学函数 &#40;Transact SQL &#41;](../../t-sql/functions/mathematical-functions-transact-sql.md)
  
  

