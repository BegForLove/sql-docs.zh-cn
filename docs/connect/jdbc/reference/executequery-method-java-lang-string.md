---
title: executeQuery 方法 (java.lang.String) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerPreparedStatement.executeQuery (java.lang.String)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 610205c2-6bcd-426c-ad6f-9682551efdec
author: MightyPen
ms.author: genemi
ms.openlocfilehash: 38e5a31ccaf493a8800f0e15abd1c21424db07c7
ms.sourcegitcommit: ff82f3260ff79ed860a7a58f54ff7f0594851e6b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2020
ms.locfileid: "67954810"
---
# <a name="executequery-method-javalangstring"></a>executeQuery 方法 (java.lang.String)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  运行给定的 SQL 语句并返回单一的 [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md) 对象。  
  
## <a name="syntax"></a>语法  
  
```  
  
public final java.sql.ResultSet executeQuery(java.lang.String sql)  
```  
  
#### <a name="parameters"></a>parameters  
 *sql*  
  
 包含 SQL 语句的 String  。  
  
## <a name="return-value"></a>返回值  
 SQLServerResultSet 对象。  
  
## <a name="exceptions"></a>例外  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>备注  
 此 executeQuery 方法是由 java.sql.Statement 接口中的 executeQuery 方法指定的。  
  
 此方法替代 [SQLServerStatement](../../../connect/jdbc/reference/executequery-method-sqlserverstatement.md) 类中找到的 [executeQuery](../../../connect/jdbc/reference/sqlserverstatement-class.md) 方法。  
  
 调用此方法将导致异常，因为在创建 SQLServerPreparedStatement 对象时指定了该对象的 SQL 语句。  
  
 如果给定的 SQL 语句没有生成单一的 [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverexception-class.md) 对象，则会引发 [SQLServerException](../../../connect/jdbc/reference/sqlserverresultset-class.md)。  
  
## <a name="see-also"></a>另请参阅  
 [executeQuery 方法 &#40;SQLServerPreparedStatement&#41;](../../../connect/jdbc/reference/executequery-method-sqlserverpreparedstatement.md)   
 [SQLServerPreparedStatement 成员](../../../connect/jdbc/reference/sqlserverpreparedstatement-members.md)   
 [SQLServerPreparedStatement 类](../../../connect/jdbc/reference/sqlserverpreparedstatement-class.md)  
  
  
