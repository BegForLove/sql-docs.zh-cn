---
title: setSavepoint 方法 (java.lang.String) |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerConnection.setSavepoint (java.lang.String)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 1cf15ec4-d9d9-4ab3-bfee-2ea43ff609a6
author: MightyPen
ms.author: genemi
manager: jroth
ms.openlocfilehash: 41d9cf40028efb2fac732ec7f6da4a3be39095af
ms.sourcegitcommit: 3026c22b7fba19059a769ea5f367c4f51efaf286
ms.translationtype: MTE75
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2019
ms.locfileid: "66796809"
---
# <a name="setsavepoint-method-javalangstring"></a>setSavepoint 方法 (java.lang.String)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  在当前事务中创建具有给定名称的保存点，然后返回表示此保存点的新 [SQLServerSavepoint](../../../connect/jdbc/reference/sqlserversavepoint-class.md) 对象。  
  
## <a name="syntax"></a>语法  
  
```  
  
public java.sql.Savepoint setSavepoint(java.lang.String sName)  
```  
  
#### <a name="parameters"></a>Parameters  
 sName   
  
 包含保存点名称的 String  值。  
  
## <a name="return-value"></a>返回值  
 一个保存点的对象。  
  
## <a name="exceptions"></a>异常  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Remarks  
 此 setSavePoint 方法由 java.sql.Connection 接口中的 setSavePoint 方法指定。  
  
 [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] 会自动转义 sName  参数。  
  
## <a name="see-also"></a>另请参阅  
 [setSavepoint 方法 &#40;SQLServerConnection&#41;](../../../connect/jdbc/reference/setsavepoint-method-sqlserverconnection.md)   
 [SQLServerConnection 成员](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [SQLServerConnection 类](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
