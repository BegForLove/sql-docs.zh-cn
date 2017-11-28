---
title: "BACKUP SERVICE MASTER KEY (TRANSACT-SQL) |Microsoft 文档"
ms.custom: 
ms.date: 03/03/2017
ms.prod: sql-non-specified
ms.prod_service: sql-database
ms.service: 
ms.component: t-sql|statements
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- BACKUP SERVICE MASTER KEY
- DUMP_SERVICE_MASTER_KEY_TSQL
- DUMP SERVICE MASTER KEY
- BACKUP_SERVICE_MASTER_KEY_TSQL
dev_langs: TSQL
helpviewer_keywords:
- backing up service master keys [SQL Server]
- BACKUP SERVICE MASTER KEY statement
- cryptography [SQL Server], Service Master Key
- exporting Service Master Keys
- encryption [SQL Server], Service Master Key
- service master key [SQL Server], exporting
ms.assetid: f8356683-6680-4f1c-9eaf-5c29a9a9020d
caps.latest.revision: "29"
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: 427b2a7c0faff9f00d37e3d85c79c5bd2c15a2f4
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="backup-service-master-key-transact-sql"></a>BACKUP SERVICE MASTER KEY (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  导出服务主密钥。  
  
 ![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "主题链接图标") [TRANSACT-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>语法  
  
```  
  
BACKUP SERVICE MASTER KEY TO FILE = 'path_to_file'   
    ENCRYPTION BY PASSWORD = 'password'  
```  
  
## <a name="arguments"></a>参数  
 文件**=***path_to_file*  
 指定要将服务主密钥导出到的文件的完整路径（包括文件名）。 此路径可以是本地路径，也可以是网络位置的 UNC 路径。  
  
 密码**=***密码*  
 用于对备份文件中的服务主密钥进行加密的密码。 此密码应通过复杂性检查。 有关详细信息，请参阅 [Password Policy](../../relational-databases/security/password-policy.md)。  
  
## <a name="remarks"></a>注释  
 应当对服务主密钥进行备份，并将其存储在另外一个单独的安全位置。 创建该备份应该是首先在服务器上执行的管理操作之一。  
  
## <a name="permissions"></a>Permissions  
 需要对服务器的 CONTROL SERVER 权限。  
  
## <a name="examples"></a>示例  
 下面的示例将服务主密钥备份到一个文件中。  
  
```  
BACKUP SERVICE MASTER KEY TO FILE = 'c:\temp_backups\keys\service_master_key' ENCRYPTION BY PASSWORD = '3dH85Hhk003GHk2597gheij4';  
```  
  
## <a name="see-also"></a>另请参阅  
 [ALTER SERVICE MASTER KEY &#40;Transact SQL &#41;](../../t-sql/statements/alter-service-master-key-transact-sql.md)   
 [RESTORE SERVICE MASTER KEY (Transact-SQL)](../../t-sql/statements/restore-service-master-key-transact-sql.md)  
  
  
