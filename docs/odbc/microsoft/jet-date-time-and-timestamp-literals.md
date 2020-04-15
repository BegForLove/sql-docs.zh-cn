---
title: Jet：日期、时间和时间戳文本 |微软文档
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- literals [ODBC], SQL grammar
- SQL grammar [ODBC], literals
- date literals [ODBC]
- timestamp literals [ODBC]
- time literals [ODBC]
ms.assetid: 37db1ae1-ca4e-4cd8-9b47-7f1a38e7fcad
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 372b7c1dab1ad8ff000fb88729c3b02e05d4a21c
ms.sourcegitcommit: ce94c2ad7a50945481172782c270b5b0206e61de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "81299928"
---
# <a name="jet-date-time-and-timestamp-literals"></a>Jet：日期、时间和时间戳文本
为了达到最大的互操作性，应用程序应使用转义子句语法以 ODBC 规范格式传递日期文本：  
  
-   对于日期文本，{d'*值*"，其中*值*e 以"yyyy-mm-dd"的形式  
  
-   对于时间文本，{t'*值*"，其中*值*e 以"hh：mm：ss"的形式  
  
 对于时间戳文本 [ts '*值*']，其中*值*e 以形式"yyyy-mm-dd hh：mm：ss_.f...]"。
