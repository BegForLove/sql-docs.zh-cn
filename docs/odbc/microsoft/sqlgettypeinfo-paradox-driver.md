---
title: SQLGetTypeInfo（悖论驱动程序） |微软文档
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLGetTypeInfo function [ODBC], Paradox Driver
- Paradox driver [ODBC], SQLGetTypeInfo
ms.assetid: e65063c7-ba9e-4cf0-ac13-4bb5bd2937db
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 693441c088865be85b18106a4c769a9f3f676f13
ms.sourcegitcommit: ce94c2ad7a50945481172782c270b5b0206e61de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "81295097"
---
# <a name="sqlgettypeinfo-paradox-driver"></a>SQLGetTypeInfo（Paradox 驱动程序）
> [!NOTE]  
>  本主题提供特定于悖论驱动程序的信息。 有关此功能的一般信息，请参阅[ODBC API 参考](../../odbc/reference/syntax/odbc-api-reference.md)下的相应主题。  
  
 **SQLGetTypeInfo**生成的表中返回的类型（TYPE_NAME）的名称将是数据源最常用的名称。  
  
 SQL_ALL_EXCEPT_LIKE将在字节、计数器、双、单、长和短数据类型的 SEARCHABLE 列中返回。 （可以通过使用 ODBC 规范转换函数将值转换为字符，然后执行比较来实现 LIKE 功能。
