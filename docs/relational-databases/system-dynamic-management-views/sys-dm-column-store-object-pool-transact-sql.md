---
title: sys. dm_column_store_object_pool （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/17/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
dev_langs:
- TSQL
ms.assetid: a8a58ca7-0a7d-4786-bfd9-e8894bd345dd
author: CarlRabeler
ms.author: carlrab
monikerRange: =azuresqldb-current||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: c6bd55fb4bf466352a3aac861844669e70b762a1
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82824682"
---
# <a name="sysdm_column_store_object_pool-transact-sql"></a>sys. dm_column_store_object_pool （Transact-sql）
[!INCLUDE[tsql-appliesto-ss2016-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md)]

 返回列存储索引对象的不同类型的对象内存池用法的计数。  
  
|列名称|数据类型|说明|  
|-----------------|---------------|-----------------|  
|`database_id`|`int`|数据库 ID。 这在 SQL Server 数据库或 Azure SQL 数据库服务器的实例中是唯一的。 |  
|`object_id`|`int`|对象的 ID。 对象是 object_types 之一。 | 
|`index_id`|`int`|columnstore 索引的 ID。|  
|`partition_number`|`bigint`|索引或堆中从 1 开始的分区号。 每个表或视图至少具有一个分区。| 
|`column_id`|`int`|列存储列的 ID。 对于 DELETE_BITMAP，此值为 NULL。| 
|`row_group_id`|`int`|行组的 ID。|
|`object_type`|`smallint`|1 = COLUMN_SEGMENT<br /><br /> 2 = COLUMN_SEGMENT_PRIMARY_DICTIONARY<br /><br /> 3 = COLUMN_SEGMENT_SECONDARY_DICTIONARY<br /><br /> 4 = COLUMN_SEGMENT_BULKINSERT_DICTIONARY<br /><br /> 5 = COLUMN_SEGMENT_DELETE_BITMAP|  
|`object_type_desc`|`nvarchar(60)`|COLUMN_SEGMENT-列段。 `object_id`是段 ID。 段将一个行组中的所有值存储在一个行组中。 例如，如果表有10列，则每个行组有10个列段。 <br /><br /> COLUMN_SEGMENT_PRIMARY_DICTIONARY-一个全局字典，其中包含表中所有列段的查找信息。<br /><br /> COLUMN_SEGMENT_SECONDARY_DICTIONARY-与一个列关联的本地字典。<br /><br /> COLUMN_SEGMENT_BULKINSERT_DICTIONARY-全局字典的其他表示形式。 这提供了值的反向查找 dictionary_id。 用于在元组移动器或大容量加载过程中创建压缩段。<br /><br /> COLUMN_SEGMENT_DELETE_BITMAP-跟踪段删除的位图。 每个分区都有一个删除位图。|  
|`access_count`|`int`|对此对象的读或写访问次数。|  
|`memory_used_in_bytes`|`bigint`|对象池中此对象使用的内存。|  
|`object_load_time`|`datetime`|Object_id 进入对象池时的时钟时间。|  
  
## <a name="permissions"></a>权限  

在上 [!INCLUDE[ssNoVersion_md](../../includes/ssnoversion-md.md)] ，需要 `VIEW SERVER STATE` 权限。   
在 [!INCLUDE[ssSDS_md](../../includes/sssds-md.md)] 高级层上，需要具有 `VIEW DATABASE STATE` 数据库中的权限。 在 [!INCLUDE[ssSDS_md](../../includes/sssds-md.md)] 标准层和基本层上，需要**服务器管理员**或**Azure Active Directory 管理员**帐户。   
 
## <a name="see-also"></a>另请参阅  
  
 [与索引相关的动态管理视图和函数 &#40;Transact-sql&#41;](../../relational-databases/system-dynamic-management-views/index-related-dynamic-management-views-and-functions-transact-sql.md)   
 [sys.dm_db_index_physical_stats (Transact-SQL)](../../relational-databases/system-dynamic-management-views/sys-dm-db-index-physical-stats-transact-sql.md)   
 [sys. dm_db_index_operational_stats &#40;Transact-sql&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-db-index-operational-stats-transact-sql.md)   
 [sys. 索引 &#40;Transact-sql&#41;](../../relational-databases/system-catalog-views/sys-indexes-transact-sql.md)   
 [sys.databases &#40;Transact-sql&#41;](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md)   
 [监视和优化性能](../../relational-databases/performance/monitor-and-tune-for-performance.md)  
  
  
