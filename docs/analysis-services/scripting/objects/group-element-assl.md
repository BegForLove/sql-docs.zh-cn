---
title: "组元素 (ASSL) |Microsoft 文档"
ms.custom: 
ms.date: 03/03/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: 
ms.topic: reference
apiname:
- Group Element
apilocation:
- http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to:
- SQL Server 2016 Preview
f1_keywords:
- GROUP
helpviewer_keywords:
- Group element
ms.assetid: 7df4ba90-b39f-4d8a-8db1-b73639a522a6
caps.latest.revision: 34
author: Minewiskan
ms.author: owend
manager: erikre
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 2e7c61ecf3f826a048445a39ef6407982e35cfe6
ms.contentlocale: zh-cn
ms.lasthandoff: 09/01/2017

---
# <a name="group-element-assl"></a>Group 元素 (ASSL)
  定义一组绑定到某个属性的成员。  
  
## <a name="syntax"></a>语法  
  
```xml  
  
<Groups>  
   <Group>  
      <Name>...</Name>  
      <Members>...</Members>  
   </Group>  
<Groups/>  
```  
  
## <a name="element-characteristics"></a>元素特征  
  
|特征|说明|  
|--------------------|-----------------|  
|数据类型和长度|无|  
|默认值|无|  
|基数|1-n：可多次出现的必需元素。|  
  
## <a name="element-relationships"></a>元素关系  
  
|关系|元素|  
|------------------|-------------|  
|父元素|[组](../../../analysis-services/scripting/collections/groups-element-assl.md)|  
|子元素|[Members](../../../analysis-services/scripting/collections/members-element-assl.md)、[Name](../../../analysis-services/scripting/properties/name-element-assl.md)|  
  
## <a name="remarks"></a>注释  
 分析管理对象 (AMO) 对象模型中的相应元素是<xref:Microsoft.AnalysisServices.Group>。  
  
## <a name="see-also"></a>另请参阅  
 [UserDefinedGroupBinding 数据类型 &#40;ASSL &#41;](../../../analysis-services/scripting/data-type/userdefinedgroupbinding-data-type-assl.md)   
 [对象 &#40;ASSL &#41;](../../../analysis-services/scripting/objects/objects-assl.md)  
  
  

