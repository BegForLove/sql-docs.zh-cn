---
title: sys.pdw_column_distribution_properties (Transact SQL) |Microsoft 文档
ms.custom: ''
ms.date: 03/03/2017
ms.prod: ''
ms.prod_service: sql-data-warehouse, pdw
ms.service: sql-data-warehouse
ms.component: system-catalog-views
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
dev_langs:
- TSQL
ms.assetid: 46b74f99-2e22-4dbd-872a-533fce0e239c
caps.latest.revision: 5
author: barbkess
ms.author: barbkess
manager: craigg
monikerRange: '>= aps-pdw-2016 || = azure-sqldw-latest || = sqlallproducts-allversions'
ms.openlocfilehash: e9b6e5b498a04e9f02a86194bd1d76ac35b5b471
ms.sourcegitcommit: f1caaa156db2b16e817e0a3884394e7b30fb642f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="syspdwcolumndistributionproperties-transact-sql"></a>sys.pdw_column_distribution_properties (TRANSACT-SQL)
[!INCLUDE[tsql-appliesto-xxxxxx-xxxx-asdw-pdw-md](../../includes/tsql-appliesto-xxxxxx-xxxx-asdw-pdw-md.md)]

  包含列的分发信息。  
  
|列名|数据类型|Description|范围|  
|-----------------|---------------|-----------------|-----------|  
|**object_id**|**int**|该列所属的对象 ID。||  
|**column_id**|**int**|列的 ID。||  
|**distribution_ordinal**|**tinyint**|序号 （基于 1 的） 中分发组。|0 = 不分布列。 1 =[!INCLUDE[ssSDW](../../includes/sssdw-md.md)]使用此列来分配父表。|  
  
## <a name="see-also"></a>另请参阅  
 [SQL 数据仓库和并行数据仓库目录视图](../../relational-databases/system-catalog-views/sql-data-warehouse-and-parallel-data-warehouse-catalog-views.md)  
  
  
