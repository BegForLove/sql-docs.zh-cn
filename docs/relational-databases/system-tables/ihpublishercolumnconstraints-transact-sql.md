---
title: IHpublishercolumnconstraints (Transact SQL) |Microsoft 文档
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: system-tables
ms.reviewer: ''
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: ''
ms.topic: language-reference
applies_to:
- SQL Server
f1_keywords:
- IHpublishercolumnconstraints
- IHpublishercolumnconstraints_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- IHpublishercolumnconstraints system table
ms.assetid: d7a41da6-e067-430a-8da2-3f6745b8a4f3
caps.latest.revision: 26
author: edmacauley
ms.author: edmaca
manager: craigg
ms.openlocfilehash: e4b764ec9638f207d504052598f6867a9123f945
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
ms.locfileid: "33000337"
---
# <a name="ihpublishercolumnconstraints-transact-sql"></a>IHpublishercolumnconstraints (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  **IHpublishercolumnconstraints**系统表映射列中的非 SQL Server 发布[IHpublishercolumns](../../relational-databases/system-tables/ihpublishercolumns-transact-sql.md)系统表中的约束[IHpublisherconstraints](../../relational-databases/system-tables/ihpublisherconstraints-transact-sql.md)系统表。 此表存储在分发数据库中。  
  
## <a name="definition"></a>定义  
  
|列名|数据类型|Description|  
|-----------------|---------------|-----------------|  
|**publishercolumn_id**|**int**|标识从列[IHpublishercolumns](../../relational-databases/system-tables/ihpublishercolumns-transact-sql.md)具有关联的约束。|  
|**publisherconstraint_id**|**int**|标识约束从[IHpublisherconstraints](../../relational-databases/system-tables/ihpublisherconstraints-transact-sql.md)与该列关联。|  
|**indid**|**int**|指示列在已发布表中的位置。|  
  
## <a name="see-also"></a>另请参阅  
 [异类数据库复制](../../relational-databases/replication/non-sql/heterogeneous-database-replication.md)   
 [复制表&#40;Transact SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [复制视图 (Transact-SQL)](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
