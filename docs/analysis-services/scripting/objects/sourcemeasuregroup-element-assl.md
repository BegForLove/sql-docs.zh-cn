---
title: "SourceMeasureGroup 元素 (ASSL) |Microsoft 文档"
ms.custom: 
ms.date: 03/06/2017
ms.prod: sql-non-specified
ms.prod_service: analysis-services
ms.service: 
ms.component: scripting
ms.reviewer: 
ms.suite: sql
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: 
ms.topic: reference
apiname: SourceMeasureGroup Element
apilocation: http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to: SQL Server 2016 Preview
f1_keywords: SourceMeasureGroup
helpviewer_keywords: SourceMeasureGroup element
ms.assetid: aaa7cc0b-162a-4c31-ab03-a90f81eeca00
caps.latest.revision: "35"
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 30cea4a156acf4af8c715b6fdf96cf0d92eca2c7
ms.sourcegitcommit: 44cd5c651488b5296fb679f6d43f50d068339a27
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2017
---
# <a name="sourcemeasuregroup-element-assl"></a>SourceMeasureGroup 元素 (ASSL)
  标识用作挖掘结构列的数据源的度量值组。  
  
## <a name="syntax"></a>语法  
  
```xml  
  
<MiningStructureColumn xsi:type="TableMiningStructureColumn">  
   ...  
   <SourceMeasureGroup xsi:type="MeasureGroupBinding">...</SourceMeasureGroup>  
   ...  
</MiningStructureColumn>  
```  
  
## <a name="element-characteristics"></a>元素特征  
  
|特征|说明|  
|--------------------|-----------------|  
|数据类型和长度|[MeasureGroupBinding](../../../analysis-services/scripting/data-type/measuregroupbinding-data-type-assl.md)|  
|默认值|无|  
|基数|0-1：可出现一次且仅出现一次的可选元素。|  
  
## <a name="element-relationships"></a>元素关系  
  
|关系|元素|  
|------------------|-------------|  
|父元素|[MiningStructureColumn](../../../analysis-services/scripting/data-type/miningstructurecolumn-data-type-assl.md)类型的[TableMiningStructureColumn](../../../analysis-services/scripting/data-type/tableminingstructurecolumn-data-type-assl.md)|  
|子元素|无|  
  
## <a name="remarks"></a>注释  
 有关详细信息**绑定**类型，包括表的 Analysis Services 脚本语言 (ASSL) 对象**绑定**类型和继承层次结构的**绑定**类型，请参阅[绑定数据类型 &#40;ASSL &#41;](../../../analysis-services/scripting/data-type/binding-data-type-assl.md).  
  
 ASSL 中数据绑定的概述，请参阅[数据源和绑定 &#40;SSAS 多维 &#41;](../../../analysis-services/multidimensional-models/data-sources-and-bindings-ssas-multidimensional.md).  
  
 对应的父级的元素**SourceMeasureGroup**分析管理对象 (AMO) 对象模型中是<xref:Microsoft.AnalysisServices.MiningStructureColumn>和<xref:Microsoft.AnalysisServices.TableMiningStructureColumn>。  
  
## <a name="see-also"></a>另请参阅  
 [对象 &#40;ASSL &#41;](../../../analysis-services/scripting/objects/objects-assl.md)  
  
  
