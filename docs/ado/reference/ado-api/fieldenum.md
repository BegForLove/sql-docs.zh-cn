---
title: FieldEnum |Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- FieldEnum
helpviewer_keywords:
- FieldEnum enumeration [ADO]
ms.assetid: be4eda13-d4e4-4d6b-bb0d-3310b0a96fc2
author: rothja
ms.author: jroth
ms.openlocfilehash: 24d69ac1406363458c8dbd3168e6d25309cfa2c4
ms.sourcegitcommit: 6037fb1f1a5ddd933017029eda5f5c281939100c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "82762568"
---
# <a name="fieldenum"></a>FieldEnum
指定[记录](../../../ado/reference/ado-api/record-object-ado.md)对象的[fields](../../../ado/reference/ado-api/fields-collection-ado.md)集合中引用的特殊字段。  
  
## <a name="remarks"></a>备注  
 这些常量提供了访问与**记录**关联的特殊字段的 "快捷方式"。 从 "**字段**" 集合中检索[字段](../../../ado/reference/ado-api/field-object.md)对象，然后获取其内容和**字段**对象的[Value](../../../ado/reference/ado-api/value-property-ado.md)属性。  
  
|返回的常量|值|说明|  
|--------------|-----------|-----------------|  
|**adDefaultStream**|-1|引用包含与**记录**关联的默认[流](../../../ado/reference/ado-api/stream-object-ado.md)对象的字段。|  
|**adRecordURL**|-2|引用包含当前**记录**的绝对 URL 字符串的字段。|
