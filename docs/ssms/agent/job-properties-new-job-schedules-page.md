---
title: 作业属性 - 新建作业（“计划”页）
ms.custom: seo-lt-2019
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: sql-tools
ms.technology: ssms
ms.topic: conceptual
f1_keywords:
- sql13.ag.job.schedules.f1
ms.assetid: 0b03585b-a510-484d-8a63-9b32459def9c
author: markingmyname
ms.author: maghan
ms.manager: jroth
ms.reviewer: ''
monikerRange: = azuresqldb-mi-current || >= sql-server-2016 || = sqlallproducts-allversions
ms.openlocfilehash: b8cb5f6fafa2ef48b3aea31e916480e712f477af
ms.sourcegitcommit: ff82f3260ff79ed860a7a58f54ff7f0594851e6b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2020
ms.locfileid: "75242260"
---
# <a name="job-properties---new-job-schedules-page"></a>作业属性 - 新建作业（“计划”页）
[!INCLUDE[appliesto-ss-asdbmi-xxxx-xxx-md](../../includes/appliesto-ss-asdbmi-xxxx-xxx-md.md)]

> [!IMPORTANT]  
> [Azure SQL 数据库托管实例](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance)目前支持大多数但并非所有 SQL Server 代理功能。 有关详细信息，请参阅 [Azure SQL 数据库托管实例与 SQL Server 之间的 T-SQL 差异](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent)。

使用此页可以查看和组织 [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 代理作业的计划。  
  
## <a name="options"></a>选项  
**计划列表**  
列出此作业的计划。  
  
**新建**  
创建新计划。 在创建计划后，该计划将被添加到作业。  
  
**选取**  
从现有计划中选择计划。 因为作业和计划必须具有相同的所有者，所以此选项将仅允许您从自己拥有的计划中选取计划。  
  
**编辑**  
编辑选定的计划以更改作业计划属性。  
  
**删除**  
从作业中删除选定的计划。 如果没有其他作业使用该计划，将从数据库中删除该计划。  
  
## <a name="see-also"></a>另请参阅  
[执行作业](../../ssms/agent/implement-jobs.md)  
  
