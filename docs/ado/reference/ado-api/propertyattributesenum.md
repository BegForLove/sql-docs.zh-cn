---
title: PropertyAttributesEnum | Microsoft Docs
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: ado
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
f1_keywords:
- PropertyAttributesEnum
helpviewer_keywords:
- PropertyAttributesEnum enumeration [ADO]
ms.assetid: 96a01955-a6b4-4cbf-9c73-52bcd1e9fb25
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 57c232c27dc538cbbdc8203855a27ee2ff56b7f8
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/09/2018
---
# <a name="propertyattributesenum"></a>PropertyAttributesEnum
指定的属性[属性](../../../ado/reference/ado-api/property-object-ado.md)对象。  
  
|常量|“值”|Description|  
|--------------|-----------|-----------------|  
|**adPropNotSupported**|0|指示提供程序不支持该属性。|  
|**adPropRequired**|1|指示数据源初始化之前，用户必须指定此属性的值。|  
|**adPropOptional**|2|指示用户不必指定此属性的值之前初始化的数据源。|  
|**adPropRead**|512|指示用户可以读取该属性。|  
|**adPropWrite**|1024|指示用户可以设置此属性。|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC 等效项  
 Package: **com.ms.wfc.data**  
  
|常量|  
|--------------|  
|AdoEnums.PropertyAttributes.NOTSUPPORTED|  
|AdoEnums.PropertyAttributes.REQUIRED|  
|AdoEnums.PropertyAttributes.OPTIONAL|  
|AdoEnums.PropertyAttributes.READ|  
|AdoEnums.PropertyAttributes.WRITE|  
  
## <a name="applies-to"></a>适用范围  
 [Attributes 属性 (ADO)](../../../ado/reference/ado-api/attributes-property-ado.md)
