---
title: sys. database_scoped_credentials （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/27/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse
ms.reviewer: ''
ms.technology: system-objects
ms.topic: conceptual
f1_keywords:
- sys.database_scoped_credentials
- sys.database_scoped_credentials_TSQL
- database_scoped_credentials
- database_scoped_credentials_TSQL
helpviewer_keywords:
- sys.database_scoped_credentials catalog view
ms.assetid: 68e8aa6b-bcdc-42aa-93d8-d498f724c188
author: VanMSFT
ms.author: vanto
monikerRange: =azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: 03687ea50b04c96aa4dbafab9d02d2bbc33a14b3
ms.sourcegitcommit: e042272a38fb646df05152c676e5cbeae3f9cd13
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2020
ms.locfileid: "68079424"
---
# <a name="sysdatabase_scoped_credentials-transact-sql"></a>sys. database_scoped_credentials （Transact-sql）
[!INCLUDE[tsql-appliesto-ss2016-asdb-asdw-xxx-md](../../includes/tsql-appliesto-ss2016-asdb-asdw-xxx-md.md)]

  为数据库中的每个数据库作用域凭据返回一行。  
  
|列名称|数据类型|说明|  
|-----------------|---------------|-----------------|  
|name|**sysname**|数据库作用域凭据的名称。 在数据库中是唯一的。|  
|credential_id|**int**|数据库作用域凭据的 ID。 在数据库中是唯一的。|  
|principal_id|**int**|拥有密钥的数据库主体的 ID。|  
|credential_identity|**nvarchar(4000)**|要使用的标识的名称。 这通常是一个 Windows 用户。 它不必是唯一的。|  
|create_date|**datetime**|创建数据库作用域凭据的时间。|  
|modify_date|**datetime**|上次修改数据库作用域凭据的时间。|  
|target_type|**nvarchar （100）**|数据库作用域凭据的类型。 返回`NULL`数据库范围的凭据。|  
|target_id|**int**|将数据库范围凭据映射到的对象的 ID。 对于数据库范围的凭据，返回0|  
  
## <a name="permissions"></a>权限  
 需要对数据库拥有 `CONTROL` 权限。  
  
## <a name="see-also"></a>另请参阅  
 [凭据 &#40;数据库引擎&#41;](../../relational-databases/security/authentication-access/credentials-database-engine.md)   
 [&#40;Transact-sql&#41;创建数据库作用域凭据](../../t-sql/statements/create-database-scoped-credential-transact-sql.md)   
 [更改数据库作用域凭据 &#40;Transact-sql&#41;](../../t-sql/statements/alter-database-scoped-credential-transact-sql.md)   
 [&#40;Transact-sql&#41;删除数据库范围的凭据](../../t-sql/statements/drop-database-scoped-credential-transact-sql.md)   
 [&#40;Transact-sql&#41;创建凭据](../../t-sql/statements/create-credential-transact-sql.md)   
 [sys.credentials (Transact-SQL)](../../relational-databases/system-catalog-views/sys-credentials-transact-sql.md)  
  
  
