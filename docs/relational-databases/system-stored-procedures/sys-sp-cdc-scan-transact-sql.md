---
title: sys. sp_cdc_scan （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.sp_cdc_scan_TSQL
- sp_cdc_scan
- sys.sp_cdc_scan
- sp_cdc_scan_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sp_cdc_scan
ms.assetid: 46e4294c-97b8-47d6-9ed9-b436a9929353
author: CarlRabeler
ms.author: carlrab
ms.openlocfilehash: 84e404ffb9459abc3f0ab2a7a1604d3f4c5609a8
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82827411"
---
# <a name="syssp_cdc_scan-transact-sql"></a>sys.sp_cdc_scan (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  执行变更数据捕获日志扫描操作。  
  
 ![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "“主题链接”图标") [Transact-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>语法  
  
```  
  
sys.sp_cdc_scan [ [ @maxtrans = ] max_trans ]   
     [ , [ @maxscans = ] max_scans ]   
     [ , [ @continuous = ] continuous ]   
     [ , [ @pollinginterval = ] polling_interval ]   
```  
  
## <a name="arguments"></a>参数  
`[ @maxtrans = ] max_trans`每个扫描循环中要处理的最大事务数。 *max_trans*的**整数为 int** ，默认值为500。  
  
`[ @maxscans = ] max_scans`为了从日志中提取所有行而要执行的扫描周期的最大数目。 *max_scans*的**整数为 int** ，默认值为10。  
  
`[ @continuous = ] continuous`指示存储过程应在执行单个扫描循环（0）之后结束，还是在 reexecuting 扫描周期（1）之前，通过*polling_interval*指定的时间暂停。 *连续*为**tinyint** ，默认值为0。  
  
`[ @pollinginterval = ] polling_interval`日志扫描循环之间的秒数。 *polling_interval*为**bigint** ，默认值为0。  
  
## <a name="return-code-values"></a>返回代码值  
 **0** （成功）或**1** （失败）  
  
## <a name="result-sets"></a>结果集  
 无  
  
## <a name="remarks"></a>备注  
 如果变更数据捕获正在使用 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 代理捕获作业，则 sys.sp_MScdc_capture_job 将内部调用 sys.sp_cdc_scan。 如果变更数据捕获日志扫描操作已经处于活动状态，或数据库启用了事务复制，则无法显式执行此过程。 此存储过程应当由需要自定义自动配置的捕获作业的行为的管理员使用。  
  
## <a name="permissions"></a>权限  
 要求具有 db_owner 固定数据库角色中的成员资格。  
  
## <a name="see-also"></a>另请参阅  
 [cdc_jobs &#40;Transact-sql&#41;](../../relational-databases/system-tables/dbo-cdc-jobs-transact-sql.md)  
  
  
