---
title: 自动创建自联接 (Visual Database Tools) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dbe-cross-instance
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- automatic joins
- self-joins
- joins [SQL Server], self
ms.assetid: f9ec90e8-3aad-415c-a5c4-8dfa9540e37f
caps.latest.revision: 10
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: d541ce3229ee01c2fb213eafb1e8c7f55a4b984a
ms.sourcegitcommit: c18fadce27f330e1d4f36549414e5c84ba2f46c2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2018
ms.locfileid: "37196547"
---
# <a name="create-self-joins-automatically-visual-database-tools"></a>自动创建自联接 (Visual Database Tools)
  如果表在数据库中有自反关系，则可自动将其与自身联接。  
  
### <a name="to-create-a-self-join-automatically"></a>自动创建自联接  
  
1.  将要处理的表添加到 [“关系图”窗格](visual-database-tools.md) 中。  
  
2.  再次添加同一表，以便“关系图”窗格显示同一表两次。  
  
     [查询和视图设计器](query-and-view-designer-tools-visual-database-tools.md) 将通过为表名添加一个顺序号来为第二个实例分配别名。 此外，查询和视图设计器还会在表示该表参与查询的两种不同方式的两个矩形之间创建联接线。  
  
## <a name="see-also"></a>请参阅  
 [使用联接进行查询 (Visual Database Tools)](query-with-joins-visual-database-tools.md)  
  
  