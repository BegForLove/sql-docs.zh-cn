---
title: Avg 函数（报表生成器和 SSRS）| Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: reporting-services-native
ms.topic: conceptual
ms.assetid: f1276c4c-bb44-44c0-a1bf-386a0c340003
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.openlocfilehash: 74bb1b6e8178f104c3987cedba1986c599e6d42b
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2020
ms.locfileid: "66105321"
---
# <a name="avg-function-report-builder-and-ssrs"></a>Avg 函数（报表生成器和 SSRS）
  返回在给定作用域中计算的、由表达式指定的所有非 Null 数值的平均值。  
  
> [!NOTE]  
>  [!INCLUDE[ssRBRDDup](../../includes/ssrbrddup-md.md)]  
  
## <a name="syntax"></a>语法  
  
```  
  
Avg(expression, scope, recursive)  
```  
  
#### <a name="parameters"></a>parameters  
 *expression*  
 (`Float`) 要对其执行聚合的表达式。  
  
 *作用域*  
 (`String`) 可选。 包含要对其应用聚合函数的报表项的数据集、组或数据区域的名称。 如果未指定 *scope* ，则使用当前作用域。  
  
 *递归*  
 (**Enumerated Type**) 可选。 `Simple`（默认值）或 `RdlRecursive`。 指定是否以递归方式执行聚合。  
  
## <a name="return-type"></a>返回类型  
 对于十进制表达式，返回 `Decimal`；对于所有其他类型的表达式，返回 `Double`。  
  
## <a name="remarks"></a>备注  
 表达式中指定的数据集必须具有相同的数据类型。 若要将具有多个数值数据类型的数据转换为同一数据类型，请使用类似 `CInt`、`CDbl` 或 `CDec` 的转换函数。 有关详细信息，请参阅 [Type Conversion Functions](https://go.microsoft.com/fwlink/?LinkId=96142)（类型转换函数）。  
  
 *scope* 的值必须是字符串常量，不能是表达式。 对于外部聚合或未指定其他聚合的聚合， *scope* 必须引用当前作用域或包含作用域。 对于聚合的聚合，嵌套聚合可以指定子作用域。  
  
 *Expression* 可以包含对嵌套聚合函数的调用，但具有以下例外和条件：  
  
-   嵌套聚合的*Scope* 必须与外部聚合的作用域相同，或者包含在外部聚合的作用域中。 对于表达式中的所有非重复作用域，一个作用域必须相对所有其他作用域处于子关系中。  
  
-   嵌套聚合的*Scope* 不能为数据集的名称。  
  
-   *表达式*不能包含`First`、 `Last`、 `Previous`或`RunningValue`函数。  
  
-   *Expression* 不得包含用于指定 *recursive*的嵌套聚合。  
  
 有关详细信息，请参阅[聚合函数引用（报表生成器和 SSRS）](report-builder-functions-aggregate-functions-reference.md)和[总计、聚合和内置集合的表达式作用域（报表生成器和 SSRS）](expression-scope-for-totals-aggregates-and-built-in-collections.md)。  
  
 有关递归聚合的详细信息，请参阅[创建递归层次结构组（报表生成器和 SSRS）](creating-recursive-hierarchy-groups-report-builder-and-ssrs.md)。  
  
## <a name="example"></a>示例  
 下面的两个代码示例提供了名为 `Cost` 的数据集所包含的 `Inventory`字段中所有值的平均值。  
  
```  
=Avg(Fields!Cost.Value, "Inventory")   
  OR    
=Avg (CDbl(Fields!Cost.Value), "Inventory")  
```  
  
## <a name="see-also"></a>另请参阅  
 [在报表中使用表达式（报表生成器和 SSRS）](expression-uses-in-reports-report-builder-and-ssrs.md)   
 [表达式示例（报表生成器和 SSRS）](expression-examples-report-builder-and-ssrs.md)   
 [表达式中的数据类型（报表生成器和 SSRS）](expressions-report-builder-and-ssrs.md)   
 [总计、聚合和内置集合的表达式作用域（报表生成器和 SSRS）](expression-scope-for-totals-aggregates-and-built-in-collections.md)  
  
  
