---
title: MSrepl_backup_lsns （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- MSrepl_backup_lsns_TSQL
- MSrepl_backup_lsns
dev_langs:
- TSQL
helpviewer_keywords:
- MSrepl_backup_Isns system table
ms.assetid: de06c349-82a8-48c6-b602-b5d6938514f6
author: CarlRabeler
ms.author: carlrab
ms.openlocfilehash: 5b97f2f3a7ae169c446a298ae7f5d31b7c8b88ed
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82824805"
---
# <a name="msrepl_backup_lsns-transact-sql"></a>MSrepl_backup_lsns (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  **MSrepl_backup_lsns**表包含事务日志序列号（LSN），用于支持分发数据库的 "同步与备份" 选项。 此表存储在分发数据库中。  
  
|列名称|数据类型|说明|  
|-----------------|---------------|-----------------|  
|**publisher_database_id**|**int**|发布服务器数据库的 ID。|  
|**valid_xact_id**|**varbinary(16)**|发送到发布服务器用以标记日志截断点的事务 ID。 仅当分发数据库处于 "与备份同步" 模式时使用。 包含已备份分发数据库中最新复制事务的 ID。 它将被发送到发布服务器以标记日志读取器所做的日志截断点。|  
|**valid_xact_seqno**|**varbinary(16)**|发送到发布服务器用以标记日志截断点的事务序列号。 仅当分发数据库处于“sync with backup”模式时使用。 它是已备份分发数据库中最新复制事务的日志序列号。 它将被发送到发布服务器以标记日志读取器所做的日志截断点。|  
|**next_xact_id**|**varbinary(16)**|备份操作使用的临时日志序列号。|  
|**nextx_xact_seqno**|**varbinary(16)**|备份操作使用的临时日志序列号。|  
  
## <a name="see-also"></a>另请参阅  
 [Transact-sql&#41;&#40;复制表](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [复制视图 (Transact-SQL)](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
