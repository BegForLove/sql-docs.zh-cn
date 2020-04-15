---
title: SQLFreeStmt |微软文档
ms.custom: ''
ms.date: 11/23/2015
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: native-client
ms.topic: reference
apitype: DLLExport
helpviewer_keywords:
- SQLFreeStmt function
ms.assetid: d9666d0b-3446-480e-bf1a-10b01213e411
author: markingmyname
ms.author: maghan
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 3eb86f9b7b1076fa3a01135b5780637ee9857f90
ms.sourcegitcommit: ce94c2ad7a50945481172782c270b5b0206e61de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "81298446"
---
# <a name="sqlfreestmt"></a>SQLFreeStmt
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]

  一般   
      在 ODBC 3.0 及更高版本中不建议使用**SQLFreeStmt。** 但是，如果应用程序需要重用语句，您仍应使用**SQLFreeStmt**与**SQL_RESET_PARAMS**和**SQL_UNBIND**选项）。 您也可以使用[SQLCloseCursor、SQLBind](../../relational-databases/native-client-odbc-api/sqlclosecursor.md)[参数](../../relational-databases/native-client-odbc-api/sqlbindparameter.md)[、SQLBindCol、SQLSetDescfield](../../relational-databases/native-client-odbc-api/sqlbindcol.md)和[SQLFreeHandle](../../relational-databases/native-client-odbc-api/sqlfreehandle.md)来替换或复制**SQLFreeStmt 的功能**，并应改用它们。 [SQLSetDescField](../../relational-databases/native-client-odbc-api/sqlsetdescfield.md)  
  
 通常，重用语句比删除语句和分配新语句更有效。 但是，在某些情况下，如重用语句，仍必须使用 SQLFreeStmt。  
  
## <a name="see-also"></a>另请参阅  
 [SQLFreeStmt 函数](https://go.microsoft.com/fwlink/?LinkId=59346)   
 [ODBC API 实现细节](../../relational-databases/native-client-odbc-api/odbc-api-implementation-details.md)  
  
  
