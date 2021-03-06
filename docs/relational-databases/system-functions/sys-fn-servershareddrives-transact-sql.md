---
title: sys. fn_servershareddrives （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- fn_servershareddrives
- fn_servershareddrives_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- fn_servershareddrives function
- shared drives [SQL Server]
- names [SQL Server], shared drives
- sys.fn_serversharedrives function
ms.assetid: ff01eff7-8cb6-460c-ba7a-6a52bda6d471
author: rothja
ms.author: jroth
ms.openlocfilehash: 71858ee3c57af8d94bdf4ef4addad720655942f4
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2020
ms.locfileid: "68122552"
---
# <a name="sysfn_servershareddrives-transact-sql"></a>sys.fn_servershareddrives (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  返回群集服务器使用的共享驱动器的名称。  
  
> [!IMPORTANT]  
>  包含此 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 系统函数是为了向后兼容。 建议改用[&#40;transact-sql&#41;的 dm_io_cluster_valid_path_names](../../relational-databases/system-dynamic-management-views/sys-dm-io-cluster-valid-path-names-transact-sql.md) 。  
  
 ![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "“主题链接”图标") [Transact-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>语法  
  
```  
  
fn_servershareddrives()  
```  
  
## <a name="tables-returned"></a>返回的表  
 如果当前服务器是群集服务器， **fn_servershareddrives**将返回共享驱动器的驱动器名称。  
  
 如果当前服务器实例不是群集服务器， **fn_servershareddrives**将返回空的行集。  
  
## <a name="remarks"></a>备注  
 `fn_servershareddrives` 返回此群集服务器使用的共享驱动器的列表。 这些共享驱动器属于与[!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]资源相同的群集组。 此外，[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 资源与这些驱动器相关。  
  
 此函数在标识用户可用的驱动器时十分有用。  
  
## <a name="permissions"></a>权限  
 用户必须对 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 实例拥有 VIEW SERVER STATE 权限。  
  
## <a name="examples"></a>示例  
 下面的示例使用 `fn_servershareddrives` 对群集服务器实例进行查询：  
  
```  
SELECT * FROM fn_servershareddrives();  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
 DriveName  
  
 -------\-  
  
 m  
  
 n  
  
## <a name="see-also"></a>另请参阅  
 [sys. dm_io_cluster_valid_path_names &#40;Transact-sql&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-io-cluster-valid-path-names-transact-sql.md)   
 [sys. dm_io_cluster_shared_drives &#40;Transact-sql&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-io-cluster-shared-drives-transact-sql.md)   
 [sys. fn_virtualservernodes &#40;Transact-sql&#41;](../../relational-databases/system-functions/sys-fn-virtualservernodes-transact-sql.md)  
  
  
