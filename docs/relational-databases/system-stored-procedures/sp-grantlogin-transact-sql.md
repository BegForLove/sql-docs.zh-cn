---
title: sp_grantlogin （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sp_grantlogin_TSQL
- sp_grantlogin
dev_langs:
- TSQL
helpviewer_keywords:
- sp_grantlogin
ms.assetid: 0c873d99-c3bf-4eb1-948b-a46cb235ccd4
ms.author: vanto
author: VanMSFT
ms.openlocfilehash: a32826266a9e844b01b455116e18ae821f71e9c5
ms.sourcegitcommit: e042272a38fb646df05152c676e5cbeae3f9cd13
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2020
ms.locfileid: "68055316"
---
# <a name="sp_grantlogin-transact-sql"></a>sp_grantlogin (Transact-SQL)

[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  创建 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 登录名。  
  
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureAvoid](../../includes/ssnotedepfutureavoid-md.md)]请改用[CREATE LOGIN](../../t-sql/statements/create-login-transact-sql.md) 。  
  
 ![主题链接图标](../../database-engine/configure-windows/media/topic-link.gif "“主题链接”图标") [Transact-SQL 语法约定](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>语法  
  
```  
sp_grantlogin [@loginame=] 'login'  
```  
  
## <a name="arguments"></a>参数  
`[ @loginame = ] 'login'`Windows 用户或组的名称。 Windows 用户或组必须使用*域*\\*用户*的 windows 域名进行限定;例如， **London\Joeb**。 *login*的**sysname**为，无默认值。  
  
## <a name="return-code-values"></a>返回代码值  
 0（成功）或 1（失败）  
  
## <a name="remarks"></a>备注  
 **sp_grantlogin**调用创建登录名，后者支持其他选项。 有关创建 SQL Server 登录名的信息，请参阅[CREATE LOGIN &#40;transact-sql&#41;](../../t-sql/statements/create-login-transact-sql.md)  
  
 不能在用户定义的事务中执行**sp_grantlogin** 。  
  
## <a name="permissions"></a>权限  
 要求对服务器拥有 ALTER ANY LOGIN 权限。  
  
## <a name="examples"></a>示例  
 下面的示例使用`CREATE LOGIN`创建 Windows 用户[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] `Corporate\BobJ.`的登录名，这是首选方法。  
  
```sql
CREATE LOGIN [Corporate\BobJ] FROM WINDOWS;  
GO  
```  
  
## <a name="see-also"></a>另请参阅  
 [安全存储过程 &#40;Transact-sql&#41;](../../relational-databases/system-stored-procedures/security-stored-procedures-transact-sql.md)   
 [CREATE LOGIN &#40;Transact-sql&#41;](../../t-sql/statements/create-login-transact-sql.md)   
 [系统存储过程 (Transact-SQL)](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
