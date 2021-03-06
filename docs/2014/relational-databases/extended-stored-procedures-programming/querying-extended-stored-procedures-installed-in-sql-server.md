---
title: 查询在 SQL Server 中安装的扩展存储过程 |Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: ''
ms.topic: reference
helpviewer_keywords:
- extended stored procedures [SQL Server], querying
ms.assetid: e02348e6-dba6-438a-98b6-684244bb034d
author: rothja
ms.author: jroth
manager: craigg
ms.openlocfilehash: 9f62c0dea02ee4c6f9bccda0dfaf7e7932c1dab7
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/25/2020
ms.locfileid: "62511930"
---
# <a name="querying-extended-stored-procedures-installed-in-sql-server"></a>查询在 SQL Server 中安装的扩展存储过程
    
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureDontUse](../../includes/ssnotedepfuturedontuse-md.md)]请改用 CLR 集成。  
  
 经过[!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]身份验证的用户可以通过运行**sp_helpextendedproc**系统过程来显示当前定义的扩展存储过程和每个存储过程所属的 DLL 的名称。 例如，下面的示例返回**xp_hello**所属的 DLL：  
  
```  
sp_helpextendedproc 'xp_hello'  
```  
  
 如果在不指定扩展存储过程的情况下执行**sp_helpextendedproc** ，则将显示所有扩展存储过程及其 dll。  
  
> [!IMPORTANT]  
>  将仅为那些登录用户拥有或具有权限的扩展存储过程返回信息。 只有**sysadmin**固定服务器角色的成员和**db_owner**、 **db_securityadmin**和**db_ddladmin**固定数据库角色的成员才能查看所有扩展存储过程的信息。  
  
## <a name="see-also"></a>另请参阅  
 [sp_helpextendedproc &#40;Transact-sql&#41;](/sql/relational-databases/system-stored-procedures/sp-helpextendedproc-transact-sql)   
 [sp_addextendedproc &#40;Transact-sql&#41;](/sql/relational-databases/system-stored-procedures/sp-addextendedproc-transact-sql)   
 [sp_dropextendedproc (Transact-SQL)](/sql/relational-databases/system-stored-procedures/sp-dropextendedproc-transact-sql)  
  
  
