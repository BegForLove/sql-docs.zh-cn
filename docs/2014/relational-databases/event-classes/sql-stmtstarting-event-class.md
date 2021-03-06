---
title: SQL:StmtStarting 事件类 | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: supportability
ms.topic: conceptual
topic_type:
- apiref
helpviewer_keywords:
- SQL:StmtStarting event class
ms.assetid: ae97386c-9dbf-456d-bcbc-391931775fa3
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 95a2e4a2bc7caeaae04ac8aab245ccf7edbb6af7
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2020
ms.locfileid: "63061279"
---
# <a name="sqlstmtstarting-event-class"></a>SQL:StmtStarting 事件类
  SQL:StmtStarting 事件类指示 [!INCLUDE[tsql](../../includes/tsql-md.md)] 语句已启动。  
  
## <a name="sqlstmtstarting-event-class-data-columns"></a>SQL:StmtStarting 事件类的数据列  
  
|数据列名称|数据类型|说明|列 ID|可筛选|  
|----------------------|---------------|-----------------|---------------|----------------|  
|ApplicationName|`nvarchar`|客户端应用程序的名称，该客户端应用程序创建了指向 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]实例的连接。 此列由应用程序传递的值填充，而不是由所显示的程序名填充。|10|是|  
|ClientProcessID|`int`|主机为运行该客户端应用程序的进程分配的 ID。 如果客户端提供了客户端进程 ID，则填充此数据列。|9|是|  
|DatabaseID|`int`|由 USE *database* 语句指定的数据库的 ID；如果未对给定实例发出 USE *database* 语句，则为默认数据库的 ID。 [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] 如果在跟踪中捕获 ServerName 数据列而且服务器可用，则将显示数据库名。 可使用 DB_ID 函数来确定数据库的值。|3|是|  
|DatabaseName|`nvarchar`|正在其中运行用户语句的数据库的名称。|35|是|  
|EventClass|`int`|事件类型 = 40。|27|否|  
|EventSequence|`int`|给定事件在请求中的顺序。|51|否|  
|GroupID|`int`|在其中激发 SQL 跟踪事件的工作负荷组的 ID。|66|是|  
|HostName|`nvarchar`|正在运行客户端的计算机的名称。 如果客户端提供了主机名，则填充此数据列。 若要确定主机名，请使用 HOST_NAME 函数。|8|是|  
|IntegerData2|`int`|正在执行的语句的终止偏移量（字节）。|55|是|  
|IsSystem|`int`|指示事件是发生在系统进程中还是发生在用户进程中。 1 = 系统，0 = 用户。|60|是|  
|LineNumber|`int`|正在执行的语句的行号。|5|是|  
|LoginName|`nvarchar`|用户的登录名（ [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 安全登录名或 [!INCLUDE[msCoName](../../includes/msconame-md.md)] Windows 登录凭据，格式为“DOMAIN\username”）。|11|是|  
|LoginSid|`image`|登录用户的安全标识号 (SID)。 您可以在 sys.server_principals 目录视图中找到此信息。 服务器中的每个登录名都具有唯一的 SID。|41|是|  
|NestLevel|`int`|如果曾在存储过程中运行 SQL 语句，则为存储过程的嵌套级别。|29|是|  
|NTDomainName|`nvarchar`|用户所属的 Windows 域。|7|是|  
|NTUserName|`nvarchar`|Windows 用户名。|6|是|  
|偏移量|`int`|存储过程或批查询中的语句的起始偏移量。|61|是|  
|RequestID|`int`|包含该语句的请求的 ID。|49|是|  
|ServerName|`nvarchar`|所跟踪的 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 实例的名称。|26|否|  
|SessionLoginName|`nvarchar`|发起会话的用户的登录名。 例如，如果您使用 Login1 连接到 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ，再以 Login2 的身份执行语句，则 SessionLoginName 将显示 Login1，而 LoginName 将显示 Login2。 此列将同时显示 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 登录名和 Windows 登录名。|64|是|  
|SPID|`int`|发生该事件的会话的 ID。|12|是|  
|StartTime|`datetime`|该事件（如果存在）的启动时间。|14|是|  
|State|`int`|指示在重新编译后是否执行语句。<br /><br /> 1 = 已重新编译|30|是|  
|TextData|`ntext`|将要执行的语句文本。|1|是|  
|TransactionID|`bigint`|该语句在事务中运行时的事务 ID。|4|是|  
|XactSequence|`bigint`|用于说明当前事务的标记。|50|是|  
  
## <a name="see-also"></a>另请参阅  
 [扩展事件](../extended-events/extended-events.md)   
 [sp_trace_setevent (Transact-SQL)](/sql/relational-databases/system-stored-procedures/sp-trace-setevent-transact-sql)  
  
  
