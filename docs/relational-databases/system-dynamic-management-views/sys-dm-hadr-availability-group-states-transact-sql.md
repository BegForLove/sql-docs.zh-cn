---
title: sys. dm_hadr_availability_group_states （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.dm_hadr_availability_group_states
- sys.dm_hadr_availability_group_states_TSQL
- dm_hadr_availability_group_states_TSQL
- dm_hadr_availability_group_states
dev_langs:
- TSQL
helpviewer_keywords:
- Availability Groups [SQL Server], monitoring
- sys.dm_hadr_availability_group_states dynamic management view
ms.assetid: d18019dd-f8dc-4492-b035-b1a639369b65
author: CarlRabeler
ms.author: carlrab
ms.openlocfilehash: bace0824a7c8411e267186c3e9919ba2eb4be15c
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82811975"
---
# <a name="sysdm_hadr_availability_group_states-transact-sql"></a>sys.dm_hadr_availability_group_states (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  为在本地实例上拥有可用性副本的每个 Always On 可用性组返回一行 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 。 每行显示定义给定可用性组的运行状况的状态。  
  
> [!NOTE]  
>  若要获取的完整列表，请查询[sys.databases. availability_groups](../../relational-databases/system-catalog-views/sys-availability-groups-transact-sql.md)目录视图。  
  
|列名称|数据类型|说明|  
|-----------------|---------------|-----------------|  
|**group_id**|**uniqueidentifier**|可用性组的唯一标识符。|  
|**primary_replica**|**varchar（128**|正在承载当前主副本的服务器实例的名称。<br /><br /> NULL = 不是主副本或无法与 WSFC 故障转移群集通信。|  
|**primary_recovery_health**|**tinyint**|指示主副本的恢复状况，可为下列值之一：<br /><br /> 0 = 正在进行<br /><br /> 1 = 联机<br /><br /> Null<br /><br /> 在辅助副本上， **primary_recovery_health**列为 NULL。|  
|**primary_recovery_health_desc**|**nvarchar(60)**|**Primary_replica_health**的说明，请执行以下操作之一：<br /><br /> ONLINE_IN_PROGRESS<br /><br /> ONLINE<br /><br /> Null|  
|**secondary_recovery_health**|**tinyint**|指示辅助副本副本的恢复运行状况，其中之一如下：<br /><br /> 0 = 正在进行<br /><br /> 1 = 联机<br /><br /> Null<br /><br /> 在主副本上， **secondary_recovery_health**列是 NULL。|  
|**secondary_recovery_health_desc**|**nvarchar(60)**|**Secondary_recovery_health**的说明，请执行以下操作之一：<br /><br /> ONLINE_IN_PROGRESS<br /><br /> ONLINE<br /><br /> Null|  
|**synchronization_health**|**tinyint**|反映可用性组中所有可用性副本的**synchronization_health**汇总。 下面是可能的值及其说明。<br /><br /> 0：不正常。 所有可用性副本都没有正常**synchronization_health** （2 = 正常）。<br /><br /> 1：部分运行正常。 某些（但并非全部）可用性副本的同步运行状况是正常的。<br /><br /> 2：正常。 每个可用性副本的同步运行状况都是正常的。<br /><br /> 有关副本同步运行状况的信息，请参阅 dm_hadr_availability_replica_states sys.databases 中的**synchronization_health**列[&#40;transact-sql&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-hadr-availability-replica-states-transact-sql.md)。|  
|**synchronization_health_desc**|**nvarchar(60)**|**Synchronization_health**的说明，请执行以下操作之一：<br /><br /> NOT_HEALTHY<br /><br /> PARTIALLY_HEALTHY<br /><br /> HEALTHY|  
  
## <a name="security"></a>安全性  
  
### <a name="permissions"></a>权限  
 要求具有服务器的 VIEW SERVER STATE 权限。  
  
## <a name="see-also"></a>另请参阅  
 [&#40;Transact-sql 监视可用性组&#41;](../../database-engine/availability-groups/windows/monitor-availability-groups-transact-sql.md)   
 [Always On 可用性组 &#40;SQL Server&#41;](../../database-engine/availability-groups/windows/always-on-availability-groups-sql-server.md)   
 [AlwaysOn 可用性组动态管理视图和函数 (Transact-SQL)](../../relational-databases/system-dynamic-management-views/always-on-availability-groups-dynamic-management-views-functions.md)  
  
  
