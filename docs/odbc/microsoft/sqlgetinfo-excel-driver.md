---
title: SQLGetInfo (Excel Driver) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- Excel driver [ODBC], SQLGetInfo
- SQLGetInfo function [ODBC], Excel Driver
ms.assetid: fed4aea2-6d3d-4199-a5db-3d033eb63927
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: a2524c51f1b4b9297b6e3483a27fd78e6c1836e9
ms.sourcegitcommit: 3026c22b7fba19059a769ea5f367c4f51efaf286
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2019
ms.locfileid: "63301987"
---
# <a name="sqlgetinfo-excel-driver"></a>SQLGetInfo（Excel 驱动程序）
> [!NOTE]  
>  本主题提供了特定于 Excel 驱动程序的信息。 有关此函数的常规信息，请参阅下的相应主题[ODBC API 参考](../../odbc/reference/syntax/odbc-api-reference.md)。  
  
 **SQLGetInfo**支持 SQL_FILE_USAGE 信息类型。 返回的值是一个 16 位整数，指示如何驱动程序直接处理数据源中的文件：  
  
-   SQL_FILE_NOT_SUPPORTED-驱动程序不是单个层驱动程序。  
  
-   SQL_FILE_TABLE-单层驱动程序将视为表中的数据源的文件。  
  
-   SQL_FILE_QUALIFIER-单层驱动程序将视为一个限定符的数据源中的文件。  
  
 ODBC 驱动程序返回 SQL_FILE_TABLE 根据 Exceldriver 由于每个文件是一个表。  
  
## <a name="sqldbmsver"></a>SQL_DBMS_VER  
  
|ISAM|Version|版本号的格式|  
|----------|-------------|-------------------------------|  
|Microsoft Excel|3.0|03.00.0000|  
||4.0|04.00.0000|  
||5.0/7.0|05.00.0000|  
||97/2000|08.00.0000|  
  
## <a name="sqlfileusage"></a>SQL_FILE_USAGE  
 SQL_FILE_TABLE (Excel 3.0/4.0)  
  
 SQL_FILE_CATALOG (Excel 5.0/7.0)  
  
## <a name="sqlmaxcharliterallen"></a>SQL_MAX_CHAR_LITERAL_LEN  
 255 (Excel 3.0/4.0/5.0/7.0)  
  
 65535 (Excel 97)  
  
## <a name="sqlmaxcolumnnamelen"></a>SQL_MAX_COLUMN_NAME_LEN  
 30 (Excel 3.0/4.0)  
  
 64 (Excel 5.0/7.0/97)  
  
## <a name="sqlmaxtablenamelen"></a>SQL_MAX_TABLE_NAME_LEN  
 12 (Excel 3.0/4.0)  
  
 31 (Excel 5.0/7.0/97)  
  
## <a name="sqlcatalognameseparator"></a>SQL_CATALOG_NAME_SEPARATOR  
 "\\" (Excel 3.0/4.0)  
  
 "."(Excel 5.0/7.0/97)  
  
## <a name="sqlcatalogterm"></a>SQL_CATALOG_TERM  
 "Directory"(Excel 3.0/4.0)  
  
 "Workbook" (Excel 5.0/7.0/97)  
  
## <a name="sqlcatalogusage"></a>SQL_CATALOG_USAGE  
 SQL_QU_DML_STATEMENTS &#124; SQL_QU_TABLE_DEFINITION  
  
## <a name="sqltimedatefunctions"></a>SQL_TIMEDATE_FUNCTIONS  
 SQL_FN_TD_CURDATE &AMP;#124; SQL_FN_TD_CURTIME &AMP;#124; SQL_FN_TD_DAYOFMONTH &AMP;#124; SQL_FN_TD_DAYOFWEEK &AMP;#124; SQL_FN_TD_DAYOFYEAR &AMP;#124; SQL_FN_TD_HOUR &AMP;#124; SQL_FN_TD_MINUTE &AMP;#124; SQL_FN_TD_MONTH &AMP;#124; SQL_FN_TD_NOW&AMP;#124; SQL_FN_TD_SECOND &AMP;#124; SQL_FN_TD_WEEK &AMP;#124; SQL_FN_TD_YEAR
