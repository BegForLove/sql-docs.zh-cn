---
title: "状态转换检查 |Microsoft 文档"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- diagnostic information [ODBC], driver manager error checking
- state transition checks [ODBC]
- driver manager [ODBC], error checking
ms.assetid: 0706db7d-e125-4845-a13a-7fe4308f7360
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 9a6873114b5d15bdf9bfbac369dacaea712a0236
ms.contentlocale: zh-cn
ms.lasthandoff: 09/09/2017

---
# <a name="state-transition-checks"></a>状态转换检查
驱动程序管理器检查环境、 连接或语句的状态适用于被调用函数。 例如，连接必须为一个已分配状态时**SQLConnect**称为; 语句必须是中的已准备状态时**SQLExecute**调用。 驱动程序管理器返回 SQL_ERROR 状态转换错误。

