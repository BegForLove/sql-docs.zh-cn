---
title: PreConnect:Starting 事件类 | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: supportability
ms.topic: conceptual
topic_type:
- apiref
helpviewer_keywords:
- PreConnect:Starting Event Class
ms.assetid: d43ed0ad-3dbd-42e0-9cef-8320b8d87497
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 0986e654430a47cc494bf1646c222b4888fc105b
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2020
ms.locfileid: "63033509"
---
# <a name="preconnectstarting-event-class"></a>PreConnect:Starting 事件类
  PreConnect:Starting事件类指示 LOGON 触发器或资源调控器分类器函数开始执行的时间。  
  
## <a name="preconnectstarting-event-class-data-columns"></a>PreConnect:Starting 事件类数据列  
  
|数据列名称|数据类型|说明|列 ID|可筛选|  
|----------------------|---------------|-----------------|---------------|----------------|  
|EventClass|`int`|215|27|否|  
|SPID|`int`|激发此事件的服务器进程的 ID。|12|是|  
|EventSubClass|`int`|1 表示用户定义的分类器函数。|21|是|  
|StartTime|`datetime`|用户定义的分类器函数开始时间。|14|是|  
|ObjectID|`int`|用户定义的分类器对象的 ID。|22|是|  
|ObjectName|`nvarchar(256)`|用户定义的分类器函数的两部分名称。 例如，dbo.classifier。|34|是|  
  
## <a name="see-also"></a>另请参阅  
 [扩展事件](../extended-events/extended-events.md)   
 [PreConnect： Completed 事件类](preconnect-completed-event-class.md)   
 [资源调控器](../resource-governor/resource-governor.md)  
  
  
