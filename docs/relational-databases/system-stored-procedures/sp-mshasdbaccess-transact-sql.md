---
title: sp_MShasdbaccess (TRANSACT-SQL) |Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sp_MShasdbaccess
- sp_MShasdbaccess_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sp_MShasdbaccess
ms.assetid: a9a23b90-2c60-4460-80a7-d7e14cc5a6a8
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 8bd1974d8fe99569a402f761a7446891cf3136b4
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2018
ms.locfileid: "47779255"
---
# <a name="spmshasdbaccess-transact-sql"></a>sp_MShasdbaccess (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  列出用户有权限访问的所有数据库的名称和所有者。  
  
 ![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "主题链接图标") [TRANSACT-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>语法  
  
```  
  
sp_MShasdbaccess      
```  
  
## <a name="return-code-values"></a>返回代码值  
 0（成功）或 1（失败）  
  
## <a name="permissions"></a>Permissions  
 执行权限授予**公共**角色。  
  
## <a name="see-also"></a>请参阅  
 [sys.sysdatabases (Transact-SQL)](../../relational-databases/system-compatibility-views/sys-sysdatabases-transact-sql.md)  
  
  
