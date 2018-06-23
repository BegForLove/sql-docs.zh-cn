---
title: SQLExecDirect |Microsoft 文档
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
- docset-sql-devref
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- SQLExecDirect function
ms.assetid: e7c2a5b5-83f4-4c72-9aca-7b9fb4748b11
caps.latest.revision: 13
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 7c51b1330f862dab23e028892945dce32f42d0e7
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36137976"
---
# <a name="sqlexecdirect"></a>SQLExecDirect
  如果语句属性： SQL_SOPT_SS_PARAM_FOCUS 是不为 0，SQLExecDirect 将返回 SQL_ERROR，并生成 SQLSTATE 的诊断记录 = HY024 和消息"无效的属性值： SQL_SOPT_SS_PARAM_FOCUS （必须在执行时的零）"。 : SQL_SOPT_SS_PARAM_FOCUS 有关的详细信息，请参阅[SQLSetStmtAttr](sqlsetstmtattr.md)。  
  
 有关表值参数的详细信息，请参阅[表值参数&#40;ODBC&#41;](../native-client-odbc-table-valued-parameters/table-valued-parameters-odbc.md)。  
  
## <a name="see-also"></a>请参阅  
 [SQLExecDirect](http://go.microsoft.com/fwlink/?LinkId=80709)   
 [ODBC API 实现细节](odbc-api-implementation-details.md)  
  
  