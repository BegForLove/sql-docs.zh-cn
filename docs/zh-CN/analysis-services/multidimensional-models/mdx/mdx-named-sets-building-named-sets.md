---
title: 生成的命名集的 MDX (MDX) |Microsoft 文档
ms.date: 05/02/2018
ms.prod: sql
ms.technology: analysis-services
ms.component: mdx
ms.topic: article
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 1890c1965299ba0f7318c7bfa9b47935e3b85fc8
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="mdx-named-sets---building-named-sets"></a>MDX 命名集的生成命名集
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]
  集表达式可能是较长且非常复杂的声明，因此很难理解。 或者，可能非常频繁地使用集表达式，以致于重复定义集成为一种负担。 为了使长而复杂的表达式或常用的表达式更易于使用，多维表达式 (MDX) 允许使用“命名集”表达式。  
  
 从根本上说，命名集就是指定了别名的集表达式。 命名集可包含能正常合并到集中的任何成员或函数。 由于 MDX 将命名集别名视为集表达式，因此您可以在任何能使用集表达式的位置使用命名集别名。  
  
 可以将命名集定义为具有下列上下文之一：  
  
-   **查询作用域** ：若要创建一个命名集，该命名集被定义为 MDX 查询的一部分并且其作用域因此被限制在该查询内，请使用 WITH 关键字。 然后，就可以在 MDX SELECT 语句中使用该命名集。 通过这种方法，更改用 WITH 关键字创建的命名集时就不会打乱 SELECT 语句。  
  
     有关如何使用 WITH 关键字创建命名集的详细信息，请参阅[创建查询作用域的命名集 (MDX)](../../../analysis-services/multidimensional-models/mdx/mdx-named-sets-creating-query-scoped-named-sets.md)。  
  
-   **会话作用域**：若要创建一个命名集，使其作用域比查询上下文更广（即，其作用域为 MDX 会话的生存期），请使用 CREATE SET 语句。 使用 CREATE SET 语句定义的命名集对该会话中的所有 MDX 查询均可用。 例如，CREATE SET 语句对于需要在多种查询中大量重用某个集的客户端应用程序会非常有用。  
  
     有关如何使用 CREATE SET 语句在会话中创建命名集的详细信息，请参阅[创建会话作用域的命名集 (MDX)](../../../analysis-services/multidimensional-models/mdx/mdx-named-sets-creating-session-scoped-named-sets.md)。  
  
## <a name="see-also"></a>另请参阅  
 [SELECT 语句 & #40;MDX & #41;](../../../mdx/mdx-data-manipulation-select.md)   
 [创建 SET 语句 & #40;MDX & #41;](../../../mdx/mdx-data-definition-create-set.md)   
 [MDX 查询基础知识 & #40;Analysis Services & #41;](../../../analysis-services/multidimensional-models/mdx/mdx-query-fundamentals-analysis-services.md)  
  
  