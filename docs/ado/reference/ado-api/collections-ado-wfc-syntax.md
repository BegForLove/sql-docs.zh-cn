---
title: 集合（ADO-WFC 语法） |Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
helpviewer_keywords:
- syntax indexes [ADO], ADO/WFC
- collections [ADO], ADO/WFC syntax
- ADO/WFC syntax index [ADO]
ms.assetid: 073f9a0e-c755-42dd-9f71-4647d68e331a
author: MightyPen
ms.author: genemi
ms.openlocfilehash: b26c78f514ef6786f642c534b2621d0c81c71e51
ms.sourcegitcommit: b87d36c46b39af8b929ad94ec707dee8800950f5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2020
ms.locfileid: "67919906"
---
# <a name="collections-ado---wfc-syntax"></a>集合（ADO - WFC 语法）
**包 .com. 数据**  
  
## <a name="parameters"></a>parameters  
  
### <a name="methods"></a>方法  
  
```  
public void append(com.ms.wfc.data.Parameter param)  
public void delete(int n)  
public void delete(String s)  
public void refresh()  
public Parameter getItem(int n)  
public Parameter getItem(String s)  
```  
  
### <a name="properties"></a>属性  
  
```  
public int getCount()  
```  
  
## <a name="fields"></a>字段  
  
### <a name="methods"></a>方法  
  
```  
public void append(String name, int type)  
public void append(String name, int type, int definedSize)  
public void append(String name, int type, int definedSize, int attrib)  
public void delete(int n)  
public void delete(String s)  
public void refresh()  
public com.ms.wfc.data.Field getItem(int n)  
public com.ms.wfc.data.Field getItem(String s)  
```  
  
### <a name="properties"></a>属性  
  
```  
public int getCount()  
```  
  
## <a name="errors"></a>错误  
  
### <a name="methods"></a>方法  
  
```  
public void clear()  
public void refresh()  
public com.ms.wfc.data.Error getItem(int n)  
public com.ms.wfc.data.Error getItem(String s)  
```  
  
### <a name="properties"></a>属性  
  
```  
public int getCount()  
```  
  
## <a name="see-also"></a>另请参阅  
 [Errors 集合（ADO）](../../../ado/reference/ado-api/errors-collection-ado.md)   
 [Fields 集合（ADO）](../../../ado/reference/ado-api/fields-collection-ado.md)   
 [参数集合 (ADO)](../../../ado/reference/ado-api/parameters-collection-ado.md)
