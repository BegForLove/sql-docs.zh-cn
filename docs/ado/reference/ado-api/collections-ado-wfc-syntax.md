---
title: 集合 (ADO-WFC 语法) |Microsoft 文档
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
apitype: COM
helpviewer_keywords:
- syntax indexes [ADO], ADO/WFC
- collections [ADO], ADO/WFC syntax
- ADO/WFC syntax index [ADO]
ms.assetid: 073f9a0e-c755-42dd-9f71-4647d68e331a
caps.latest.revision: 10
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: cd7be8ac8341ca6386661b3408dc98c4bf800f5c
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35276516"
---
# <a name="collections-ado---wfc-syntax"></a>集合 (ADO-WFC 语法)
**包 com.ms.wfc.data**  
  
## <a name="parameters"></a>Parameters  
  
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
  
## <a name="see-also"></a>请参阅  
 [错误集合 (ADO)](../../../ado/reference/ado-api/errors-collection-ado.md)   
 [字段集合 (ADO)](../../../ado/reference/ado-api/fields-collection-ado.md)   
 [参数集合 (ADO)](../../../ado/reference/ado-api/parameters-collection-ado.md)
