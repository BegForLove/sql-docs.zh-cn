---
title: 列元素 (ASSL) |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.topic: reference
api_name:
- Column Element
api_location:
- http://schemas.microsoft.com/analysisservices/2003/engine
topic_type:
- apiref
f1_keywords:
- Column
helpviewer_keywords:
- Column element
ms.assetid: 10dc6d5e-c690-4415-adbb-eaeebaa29cb4
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 314e5077f4212e2095d822e0e00d5028ca127a1b
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2018
ms.locfileid: "48218777"
---
# <a name="column-element-assl"></a>Column 元素 (ASSL)
  描述与父元素关联的列集合中的一列。  
  
## <a name="syntax"></a>语法  
  
```xml  
  
<Columns>  
   <Column xsi:type="MeasureBinding">...</Column> <!-- parent of collection: DrillThroughAction -->  
   <!-- or -->  
   <Column xsi:type="CubeAttributeBinding">...</Column> <!-- parent of collection: DrillThroughAction -->  
   <!-- or -->  
   <Column xsi:type="EventColumn">...</Column> <!-- parent of collection: Event -->  
   <!-- or -->  
   <Column xsi:type="MiningModelColumn">...</Column> <!-- parent of collection: MiningModel or MiningModelColumn -->  
   <!-- or -->  
   <Column xsi:type="MiningStructureColumn">...</Column> <!-- parent of collection: MiningStructure or TableMiningStructureColumn -->  
</Columns>  
```  
  
## <a name="element-characteristics"></a>元素特征  
  
|特征|Description|  
|--------------------|-----------------|  
|数据类型和长度||  
|默认值|None|  
|基数||  
  
|祖先或父级|数据类型|  
|------------------------|---------------|  
|[DrillThroughAction](../data-type/binding-data-type-assl.md)， [CubeAttributeBinding](../data-type/attributebinding-data-type-assl.md)|  
|[事件](../data-type/eventcolumn-data-type-assl.md)|  
|[MiningModel](miningmodel-element-assl.md)， [MiningModelColumn](../data-type/miningmodelcolumn-data-type-assl.md)|  
|[MiningStructure](miningstructure-element-assl.md)， [TableMiningStructureColumn](../data-type/miningstructurecolumn-data-type-assl.md)|  
  
|祖先或父级|基数|  
|------------------------|-----------------|  
|[事件](event-element-assl.md)|1-n：可多次出现的必需元素。|  
|其他|0-1：可出现一次且仅出现一次的可选元素。|  
  
## <a name="element-relationships"></a>元素关系  
  
|关系|元素|  
|------------------|-------------|  
|父元素|[列](../collections/columns-element-assl.md)|  
|子元素|None|  
  
## <a name="see-also"></a>请参阅  
 [对象&#40;ASSL&#41;](objects-assl.md)  
  
  
