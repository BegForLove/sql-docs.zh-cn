---
title: updateDate 方法 （int，java.sql.Date） |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerResultSet.updateDate (int, java.sql.Date)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: c5fb1292-a5cf-4cdd-8c4a-d1679944a6d0
author: MightyPen
ms.author: genemi
manager: jroth
ms.openlocfilehash: 13a8ed675e63d19d3c21dddf54751073593ae156
ms.sourcegitcommit: 3026c22b7fba19059a769ea5f367c4f51efaf286
ms.translationtype: MTE75
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2019
ms.locfileid: "66804258"
---
# <a name="updatedate-method-int-javasqldate"></a>updateDate 方法 (int, java.sql.Date)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  根据给定的列索引使用日期值更新指定的列。  
  
## <a name="syntax"></a>语法  
  
```  
  
public void updateDate(int index,  
                       java.sql.Date x)  
```  
  
#### <a name="parameters"></a>Parameters  
 索引   
  
 指示列索引的 int  。  
  
 *x*  
  
 日期值。  
  
## <a name="exceptions"></a>异常  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Remarks  
 此 updateDate 方法是由 java.sql.ResultSet 接口中的 updateDate 方法指定的。  
  
## <a name="see-also"></a>另请参阅  
 [updateDate 方法&#40;SQLServerResultSet&#41;](../../../connect/jdbc/reference/updatedate-method-sqlserverresultset.md)   
 [SQLServerResultSet 成员](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet 类](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
