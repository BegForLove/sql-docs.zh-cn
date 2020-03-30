---
title: updateShort 方法 (int, short) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerResultSet.updateShort (int, short)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 155b9189-cb97-4264-b42c-bbda1c7d624f
author: MightyPen
ms.author: genemi
ms.openlocfilehash: 9e146aacff54a934687b57d6b971e02c14d38e0a
ms.sourcegitcommit: ff82f3260ff79ed860a7a58f54ff7f0594851e6b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2020
ms.locfileid: "67998325"
---
# <a name="updateshort-method-int-short"></a>updateShort 方法 (int, short)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  根据给定的列索引使用 short  值更新指定的列。  
  
## <a name="syntax"></a>语法  
  
```  
  
public void updateShort(int index,  
                        short x)  
```  
  
#### <a name="parameters"></a>parameters  
 索引   
  
 指示列索引的 int  。  
  
 *x*  
  
 short  值。  
  
## <a name="exceptions"></a>例外  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>备注  
 此 updateShort 方法是由 java.sql.ResultSet 接口中的 updateShort 方法指定的。  
  
## <a name="see-also"></a>另请参阅  
 [updateShort 方法 (SQLServerResultSet)](../../../connect/jdbc/reference/updateshort-method-sqlserverresultset.md)   
 [SQLServerResultSet 成员](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet 类](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
