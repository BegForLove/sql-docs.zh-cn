---
title: UpdateCells 元素 (XMLA) |Microsoft 文档
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: ''
ms.topic: reference
api_name:
- UpdateCells Element
api_location:
- http://schemas.microsoft.com/analysisservices/2003/engine
topic_type:
- apiref
f1_keywords:
- microsoft.xml.analysis.updatecells
- urn:schemas-microsoft-com:xml-analysis#UpdateCells
- http://schemas.microsoft.com/analysisservices/2003/engine#UpdateCells
helpviewer_keywords:
- UpdateCells command
ms.assetid: 18336a35-8a46-4532-9ee7-71828b2982af
caps.latest.revision: 12
author: mgblythe
ms.author: mblythe
manager: mblythe
ms.openlocfilehash: fd96a8652bb5537cfb4f4f116aa86450a34acbe3
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36128194"
---
# <a name="updatecells-element-xmla"></a>UpdateCells 元素 (XMLA)
  更新启用写操作的多维数据集中的单元。  
  
## <a name="syntax"></a>语法  
  
```xml  
  
<Command>  
   <UpdateCells>  
      <Cell>...</Cell>  
   </UpdateCells>  
</Command>  
```  
  
## <a name="element-characteristics"></a>元素特征  
  
|特征|Description|  
|--------------------|-----------------|  
|数据类型和长度|InclusionThresholdSetting|  
|默认值|InclusionThresholdSetting|  
|基数|0-n：可多次出现的可选元素。|  
  
## <a name="element-relationships"></a>元素关系  
  
|关系|元素|  
|------------------|-------------|  
|父元素|[Command](../xml-elements-properties/command-element-xmla.md)|  
|子元素|[单元格](../xml-elements-properties/cell-element-xmla.md)|  
  
## <a name="remarks"></a>Remarks  
 `UpdateCells` 命令更新支持单元回写操作的多维数据集中的单元。  
  
 有关更新单元的详细信息，请参阅[更新单元 (XMLA)](../../multidimensional-models-scripting-language-assl-xmla/updating-cells-xmla.md)。  
  
## <a name="see-also"></a>请参阅  
 [删除元素&#40;XMLA&#41;](drop-element-xmla.md)   
 [插入元素&#40;XMLA&#41;](insert-element-xmla.md)   
 [更新元素&#40;XMLA&#41;](update-element-xmla.md)   
 [命令&#40;XMLA&#41;](xml-elements-commands.md)  
  
  