---
title: sp_dbmmonitorhelpmonitoring （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sp_dbmmonitorhelpmonitoring
- sp_dbmmonitorhelpmonitoring_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sp_dbmmonitorhelpmonitoring
- database mirroring [SQL Server], monitoring
ms.assetid: a085cf87-269f-454a-a146-21f80a113b72
author: CarlRabeler
ms.author: carlrab
ms.openlocfilehash: b16c77357795ed3c7e11454016663befcf4ae329
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82826157"
---
# <a name="sp_dbmmonitorhelpmonitoring-transact-sql"></a>sp_dbmmonitorhelpmonitoring (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  返回当前更新持续时间。  
  
 ![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "“主题链接”图标") [Transact-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>语法  
  
```  
  
sp_dbmmonitorhelpmonitoring   
```  
  
## <a name="arguments"></a>参数  
 无  
  
## <a name="return-code-values"></a>返回代码值  
 无  
  
## <a name="result-sets"></a>结果集  
 返回当前更新周期，即数据库镜像状态表的更新间隔分钟数。 此值范围是从 1 到 120 分钟。  
  
## <a name="permissions"></a>权限  
 要求具有 **sysadmin** 固定服务器角色的成员身份。  
  
## <a name="examples"></a>示例  
 以下示例返回当前更新周期。  
  
```  
EXEC sp_dbmmonitorhelpmonitoring;  
```  
  
## <a name="see-also"></a>另请参阅  
 [监视数据库镜像 &#40;SQL Server&#41;](../../database-engine/database-mirroring/monitoring-database-mirroring-sql-server.md)   
 [sp_dbmmonitorresults (Transact-SQL)](../../relational-databases/system-stored-procedures/sp-dbmmonitorresults-transact-sql.md)  
  
  
