---
title: sysdbmaintplan_history （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sysdbmaintplan_history_TSQL
- sysdbmaintplan_history
dev_langs:
- TSQL
helpviewer_keywords:
- sysdbmaintplan_history system table
ms.assetid: 02d36f08-ac93-4463-bb59-284c5cd6ed04
author: CarlRabeler
ms.author: carlrab
ms.openlocfilehash: 088dbf0fb51edddedd37fdd176becd413fc229ee
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82820969"
---
# <a name="sysdbmaintplan_history-transact-sql"></a>sysdbmaintplan_history (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  该表存储在**msdb**数据库中。  
  
 [!INCLUDE[ssNoteDepNextAvoid](../../includes/ssnotedepnextavoid-md.md)]  
  
  
|列名称|数据类型|说明|  
|-----------------|---------------|-----------------|  
|**sequence_id**|**int**|数据库维护计划执行的历史记录序列。|  
|**plan_id**|**uniqueidentifier**|数据库维护计划 ID。|  
|**plan_name**|**sysname**|数据库维护计划名称。|  
|**database_name**|**sysname**|与数据库维护计划关联的数据库的名称。|  
|server_name |**sysname**|系统名称。|  
|**activity**|**nvarchar(128)**|数据库维护计划执行的活动（例如备份事务日志等）。|  
|**成功**|**bit**|**0** = 成功**1** = 失败|  
|**end_time**|**datetime**|完成操作的时间。|  
|**duration**|**int**|完成数据库维护计划操作所需的时间。|  
|**start_time**|**datetime**|操作开始的时间。|  
|error_number |**int**|失败时报告的错误号。|  
|**message**|**nvarchar(512)**|**Sqlmaint**生成的消息。|  
  
  
