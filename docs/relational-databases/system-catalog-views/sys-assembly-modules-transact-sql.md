---
title: sys. assembly_modules （Transact-sql） |Microsoft Docs
ms.custom: ''
ms.date: 03/15/2017
ms.prod: sql
ms.prod_service: database-engine, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.assembly_modules
- sys.assembly_modules_TSQL
- assembly_modules
- assembly_modules_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.assembly_modules catalog view
ms.assetid: 5f9e644e-8065-49a2-b53d-db7df98f70d8
author: CarlRabeler
ms.author: carlrab
monikerRange: '>=aps-pdw-2016||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 967626693c52cc31bacddf88735224f3e191e6a6
ms.sourcegitcommit: 4d3896882c5930248a6e441937c50e8e027d29fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "82829173"
---
# <a name="sysassembly_modules-transact-sql"></a>sys.assembly_modules (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-asdw-pdw-md](../../includes/tsql-appliesto-ss2008-xxxx-asdw-pdw-md.md)]

  为公共语言运行时 (CLR) 程序集所定义的每个函数、过程或触发器返回一行。 此目录视图将 CLR 存储过程、CLR 触发器或 CLR 函数映射到其基础实现。 类型为 TA、AF、PC、FS 和 FT 的对象具有相关联的程序集模块。 若要查找对象和程序集之间的关联，可以将此目录视图联接到其他目录视图。 例如，当您创建 CLR 存储过程时，该存储过程由**sys.databases**中的一行 **、sys.databases 中的一行（继承**自**sys.databases**）和一个在**sys. assembly_modules**中。 存储过程本身由**sys.databases**和**sys.databases**中的元数据表示。 在**sys. assembly_modules**中找到对过程的基础 CLR 实现的引用。  
  
|列名称|数据类型|说明|  
|-----------------|---------------|-----------------|  
|**object_id**|**int**|SQL 对象的对象标识号。 在数据库中是唯一的。|  
|**assembly_id**|**int**|创建此模块所基于的程序集的 ID。|  
|**assembly_class**|**sysname**|定义此模块的程序集中的类名。|  
|**assembly_method**|**sysname**|定义此模块的**assembly_class**中的方法的名称。<br /><br /> 对于聚合函数 (AF)，该参数的值为 NULL。|  
|**null_on_null_input**|**bit**|将模块声明为针对任意 NULL 输入生成 NULL 输出。|  
|**execute_as_principal_id**|**int**|在其中执行上下文的数据库主体的 ID，该 ID 由 CLR 函数、存储过程或触发器的 EXECUTE AS 子句指定。<br /><br /> NULL = EXECUTE AS CALLER。 这是默认设置。<br /><br /> 指定数据库主体的 ID = 作为自身执行，作为*USER_NAME*执行，或作为*login_name*执行。<br /><br /> -2 = EXECUTE AS OWNER。|  
  
## <a name="permissions"></a>权限  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] 有关详细信息，请参阅 [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md)。  
  
## <a name="see-also"></a>另请参阅  
 [&#40;Transact-sql&#41;的对象目录视图](../../relational-databases/system-catalog-views/object-catalog-views-transact-sql.md)   
 [目录视图 (Transact-SQL)](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)  
  
  
