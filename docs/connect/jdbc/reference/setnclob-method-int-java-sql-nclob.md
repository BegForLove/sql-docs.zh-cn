---
title: setNClob 方法 (int, java.sql.NClob) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: 48c8aa2a-4185-4837-b592-830e60f8ca0b
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 4c8fcb66b008c5290000b7038796359496f545d3
ms.sourcegitcommit: fe5c45a492e19a320a1a36b037704bf132dffd51
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2020
ms.locfileid: "80900998"
---
# <a name="setnclob-method-int-javasqlnclob"></a>setNClob 方法 (int, java.sql.NClob)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  将指定参数设置为指定 NClob 对象。  
  
## <a name="syntax"></a>语法  
  
```  
  
public final void setNClob(int parameterIndex,  
              java.sql.NClob value)  
```  
  
#### <a name="parameters"></a>parameters  
 parameterIndex   
  
 指示参数索引的 int  。  
  
 *value*  
  
 指示参数值的 NClob 对象。  
  
## <a name="exceptions"></a>例外  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>备注  
 此 setNClob 方法是由 java.sql.PreparedStatement 接口中的 setNClob 方法指定的。  
  
## <a name="see-also"></a>另请参阅  
 [setNClob 方法 &#40;SQLServerPreparedStatement&#41;](../../../connect/jdbc/reference/setnclob-method-sqlserverpreparedstatement.md)   
 [SQLServerPreparedStatement 成员](../../../connect/jdbc/reference/sqlserverpreparedstatement-members.md)  
  
  
