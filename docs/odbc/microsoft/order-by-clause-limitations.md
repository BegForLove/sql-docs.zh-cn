---
title: ORDER BY 子句限制 |Microsoft 文档
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: drivers
ms.service: ''
ms.component: odbc
ms.reviewer: ''
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- ODBC SQL grammar, ORDER BY clause limitations
- ORDER BY clause limitations [ODBC]
ms.assetid: fd4ddc7c-9c7e-4a0c-a781-e5427dfb2e18
caps.latest.revision: 7
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 7eb96840ec20338b8d7739b2332d63bea25c765d
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="order-by-clause-limitations"></a>ORDER BY 子句限制
如果 SELECT 语句包含 GROUP BY 子句和 ORDER BY 子句，仅在结果集中的列或 GROUP BY 子句中的表达式可以包含 ORDER BY 子句。
