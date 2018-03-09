---
title: "Dbmslpcn.dll 共享内存中的 ConnectionValidSharedMemory 函数 |Microsoft 文档"
ms.custom: 
ms.date: 03/07/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: 
ms.component: native-client|applications
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 6ae35826-7d75-4542-b686-5f79316b6157
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 705177dd5243c0eb7619bf9fda723087e8d846d4
ms.sourcegitcommit: a0aa5e611a0e6ebb74ac1e2f613e8916dc7a7617
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/24/2018
---
# <a name="connectionvalidsharedmemory-function-in-dbmslpcndll-shared-memory"></a>Dbmslpcn.dll 共享内存中的 ConnectionValidSharedMemory 函数
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../../includes/snac-deprecated.md)]

  该函数确定 SQL Server 共享内存是否已安装并处于活动状态。  
  
## <a name="syntax"></a>语法  
  
```cpp  
BOOL ConnectionValidSharedMemory(char * szServerName);  
```  
  
## <a name="parameters"></a>Parameters  
 *szServerName*  
  
-   类型： **char\***  
  
-   SQL server 的名称。  
  
## <a name="return-value"></a>返回值  
 类型： **BOOL**  
  
 如果不是有效的; 则返回 0否则返回非零值。  
  
  
