---
title: setTrustManagerClass 方法 (SQLServerDataSource) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2018
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerDataSource.setTrustManagerClass
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: ''
author: MightyPen
ms.author: genemi
ms.openlocfilehash: 9d197589cb1b4702404ce8ba22200a7bde7e4da4
ms.sourcegitcommit: b78f7ab9281f570b87f96991ebd9a095812cc546
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2020
ms.locfileid: "67972264"
---
# <a name="settrustmanagerclass-method-sqlserverdatasource"></a>setTrustManagerClass 方法 (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  设置 TrustManagerClass 连接属性的 String 值。
  
## <a name="syntax"></a>语法  
  
```  
  
public void setTrustManagerClass(java.lang.String trustManagerClass)  
```  
  
#### <a name="parameters"></a>parameters  
 trustManagerClass   
  
 String  ，它包含自定义 javax.net.ssl.TrustManager 的完全限定类名。
  
## <a name="see-also"></a>另请参阅  
 [SQLServerDataSource 成员](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource 类](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
