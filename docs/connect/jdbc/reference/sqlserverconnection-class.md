---
title: SQLServerConnection 类 | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: 937292a6-1525-423e-a2b2-a18fd34c2893
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 6248e126806b15592bbc3d6c458045ca7d9db042
ms.sourcegitcommit: fe5c45a492e19a320a1a36b037704bf132dffd51
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2020
ms.locfileid: "80920680"
---
# <a name="sqlserverconnection-class"></a>SQLServerConnection 类
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  表示连接到 [!INCLUDE[msCoName](../../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] 数据库的 JDBC 连接。  
  
 **包：** com.microsoft.sqlserver.jdbc  
  
 **实现：** [ISQLServerConnection](../../../connect/jdbc/reference/isqlserverconnection-interface.md)、java.io.Serializable  
  
## <a name="syntax"></a>语法  
  
```  
  
public class SQLServerConnection  
```  
  
## <a name="remarks"></a>备注  
 SQLServerConnection 支持 JDBC 连接池，并且可以是物理 JDBC 连接或逻辑 JDBC 连接。 SQLServerConnection 可管理通过它创建的所有语句的事务控制，并且可参与通过 XAResource 适配器管理的 XA 分布式事务。  
  
 SQLServerConnection 管理准备的语句句柄池。 预定义语句仅准备一次，但通常使用不同的语句参数数据值运行多次。 预定义语句还可跨多个关闭的逻辑（入池）连接进行维护。  
  
> [!NOTE]  
>  SQLServerConnection 不是线程安全的。 但是，可以在并发线程中同时处理基于单个连接创建的多个语句。  
  
 此类支持取消包装 SQLServerConnection 类、java.sql.connection 接口和 ISQLServerConnection 接口。 有关详细信息，请参阅[包装器和接口](../../../connect/jdbc/wrappers-and-interfaces.md)。  
  
## <a name="see-also"></a>另请参阅  
 [SQLServerConnection 成员](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [JDBC 驱动程序 API 参考](../../../connect/jdbc/reference/jdbc-driver-api-reference.md)  
  
  
