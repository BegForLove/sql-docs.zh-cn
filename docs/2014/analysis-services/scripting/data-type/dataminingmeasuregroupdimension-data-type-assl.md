---
title: DataMiningMeasureGroupDimension 数据类型 (ASSL) |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.topic: reference
api_name:
- DataMiningMeasureGroupDimension Data Type
api_location:
- http://schemas.microsoft.com/analysisservices/2003/engine
topic_type:
- apiref
f1_keywords:
- DataMiningMeasureGroupDimension
helpviewer_keywords:
- DataMiningMeasureGroupDimension data type
ms.assetid: 56d5c2ec-7e03-4dc7-a668-c8d598d59e55
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 9f92fb25375c3741b06ad873ac5f9facd6585570
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2018
ms.locfileid: "48171827"
---
# <a name="dataminingmeasuregroupdimension-data-type-assl"></a>DataMiningMeasureGroupDimension 数据类型 (ASSL)
  定义一个派生数据类型，该类型表示某个度量值组和数据挖掘维度之间的关系。  
  
## <a name="syntax"></a>语法  
  
```xml  
  
<DataMiningMeasureGroupDimension>  
   <!-- The following elements extend MeasureGroupDimension -->  
      <CaseCubeDimensionID>...</CaseCubeDimensionID>  
</DataMiningMeasureGroupDimension>  
```  
  
## <a name="data-type-characteristics"></a>数据类型特征  
  
|特征|Description|  
|--------------------|-----------------|  
|基本数据类型|[MeasureGroupDimension](dimension-data-type-assl.md)|  
|派生数据类型|None|  
  
## <a name="data-type-relationships"></a>数据类型关系  
  
|关系|元素|  
|------------------|-------------|  
|父元素|None|  
|子元素|[CaseCubeDimensionID](../properties/id-element-assl.md)|  
|派生元素|请参阅[维度](../objects/dimension-element-assl.md)([维度](../collections/dimensions-element-assl.md)的集合[MeasureGroup](../objects/group-element-assl.md))|  
  
## <a name="remarks"></a>备注  
 在 Analysis Management Objects (AMO) 对象模型中的相应元素是<xref:Microsoft.AnalysisServices.DataMiningMeasureGroupDimension>。  
  
## <a name="see-also"></a>请参阅  
 [Analysis Services 脚本语言 XML 数据类型&#40;ASSL&#41;](analysis-services-scripting-language-xml-data-types-assl.md)  
  
  
