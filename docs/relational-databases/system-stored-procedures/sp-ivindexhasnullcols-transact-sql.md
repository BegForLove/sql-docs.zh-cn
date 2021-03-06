---
title: sp_ivindexhasnullcols （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- sp_ivindexhasnullcols
- sp_ivindexhasnullcols_TSQL
helpviewer_keywords:
- sp_ivindexhasnullcols
ms.assetid: ed2cde63-37e1-43cf-b6ba-3b6114a0f797
author: CarlRabeler
ms.author: carlrab
ms.openlocfilehash: 6f83837e6676cfd99f2403b4bfecd301915d263a
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82834375"
---
# <a name="sp_ivindexhasnullcols-transact-sql"></a>sp_ivindexhasnullcols (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  验证索引视图的聚集索引是否唯一，而且当索引视图将要用于创建事务发布时其聚集索引不包含任何可能为 Null 的列。 此存储过程在发布服务器上对发布数据库执行。  
  
 ![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "“主题链接”图标") [Transact-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>语法  
  
```  
  
sp_ivindexhasnullcols [ @viewname = ] 'view_name'  
        , [ @fhasnullcols= ] field_has_null_columns OUTPUT  
```  
  
## <a name="arguments"></a>参数  
`[ @viewname = ] 'view_name'`要验证的视图的名称。 *view_name* **sysname**，无默认值。  
  
`[ @fhasnullcols = ] field_has_null_columns OUTPUT`指示视图索引是否具有允许 NULL 值的列的标志。 *view_name* **sysname**，无默认值。 如果视图索引包含允许 NULL 的列，则返回值**1** 。 如果视图不包含允许 NULL 的列，则返回值**0** 。  
  
> [!NOTE]  
>  如果存储过程本身返回的返回代码为**1**，则表示存储过程执行失败，则此值为**0** ，应忽略此值。  
  
## <a name="return-code-values"></a>返回代码值  
 **0** （成功）或**1** （失败）  
  
## <a name="remarks"></a>备注  
 **sp_ivindexhasnullcols**由事务复制使用。  
  
 默认情况下，发布中的索引视图项目创建为订阅服务器上的表。 但是，当索引列允许 NULL 值时，索引视图创建为订阅服务器上的索引视图而不是表。 通过执行此存储过程，可以警告用户当前索引视图中是否存在此问题。  
  
## <a name="permissions"></a>权限  
 只有**sysadmin**固定服务器角色的成员或**db_owner**固定数据库角色的成员才能执行**sp_ivindexhasnullcols**。  
  
## <a name="see-also"></a>另请参阅  
 [系统存储过程 (Transact-SQL)](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
