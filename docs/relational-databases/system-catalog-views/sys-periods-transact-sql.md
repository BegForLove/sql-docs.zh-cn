---
title: sys.periods (Transact SQL) |Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
dev_langs:
- TSQL
ms.assetid: 25e66ed3-2270-4c5c-9f5a-2c0f165a57ca
author: stevestein
ms.author: sstein
ms.openlocfilehash: eea7709c67eab0dc9fe1890135f9ae03225cdff2
ms.sourcegitcommit: b2464064c0566590e486a3aafae6d67ce2645cef
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/15/2019
ms.locfileid: "68068096"
---
# <a name="sysperiods-transact-sql"></a>sys.periods (Transact SQL)
[!INCLUDE[tsql-appliesto-ss2016-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md)]

  返回为其定义任何时间每个表的行。  
  
|列标题|数据类型|描述|  
|-------------------|---------------|-----------------|  
|name|**sysname**|期间的名称|  
|period_type|**tinyint**|表示时间段的类型的数值：<br /><br /> 1 = 系统时间段|  
|period_type_desc|**nvarchar(60)**|列的类型的文本说明：<br /><br /> SYSTEM_TIME_PERIOD|  
|object_id|**int**|包含 period_type 列的表的 id|  
|start_column_id|**int**|定义时间段的下限的列的 id|  
|end_column_id|**int**|定义时间段上限的列的 id|  
  
## <a name="permissions"></a>权限  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] 有关详细信息，请参阅 [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md)。  
  
## <a name="see-also"></a>请参阅  
 [系统视图&#40;Transact SQL&#41;](https://msdn.microsoft.com/library/35a6161d-7f43-4e00-bcd3-3091f2015e90)   
 [对象目录视图 (Transact-SQL)](../../relational-databases/system-catalog-views/object-catalog-views-transact-sql.md)   
 [目录视图 (Transact-SQL)](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)   
 [sys.all_columns &#40;TRANSACT-SQL&#41;](../../relational-databases/system-catalog-views/sys-all-columns-transact-sql.md)   
 [sys.system_columns &#40;TRANSACT-SQL&#41;](../../relational-databases/system-catalog-views/sys-system-columns-transact-sql.md)   
 [查询 SQL Server 系统目录常见问题](../../relational-databases/system-catalog-views/querying-the-sql-server-system-catalog-faq.md)   
 [临时表](../../relational-databases/tables/temporal-tables.md)  
  
  
