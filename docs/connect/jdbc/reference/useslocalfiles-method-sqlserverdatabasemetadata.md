---
title: usesLocalFiles 方法 (SQLServerDatabaseMetaData) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerDatabaseMetaData.usesLocalFiles
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 69afb3a9-ed56-4191-88b8-bc46c03b817b
author: MightyPen
ms.author: genemi
ms.openlocfilehash: a88b6645445b9b9a4c644444ad3996377436112f
ms.sourcegitcommit: b78f7ab9281f570b87f96991ebd9a095812cc546
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2020
ms.locfileid: "68001591"
---
# <a name="useslocalfiles-method-sqlserverdatabasemetadata"></a>usesLocalFiles 方法 (SQLServerDatabaseMetaData)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  检索此数据库是否将表存储在本地文件中。  
  
## <a name="syntax"></a>语法  
  
```  
  
public boolean usesLocalFiles()  
```  
  
## <a name="return-value"></a>返回值  
 如果数据库使用本地文件，则为 true  。 否则为 **false**。  
  
## <a name="exceptions"></a>例外  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>备注  
 此 usesLocalFiles 方法是由 java.sql.DatabaseMetaData 接口中的 usesLocalFiles 方法指定的。  
  
## <a name="see-also"></a>另请参阅  
 [SQLServerDatabaseMetaData 方法](../../../connect/jdbc/reference/sqlserverdatabasemetadata-methods.md)   
 [SQLServerDatabaseMetaData 成员](../../../connect/jdbc/reference/sqlserverdatabasemetadata-members.md)   
 [SQLServerDatabaseMetaData 类](../../../connect/jdbc/reference/sqlserverdatabasemetadata-class.md)  
  
  
