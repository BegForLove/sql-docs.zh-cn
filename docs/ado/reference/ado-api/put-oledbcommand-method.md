---
title: put_OLEDBCommand 方法 |Microsoft 文档
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- put_OLEDBCommand method [ADO]
ms.assetid: ca6a5804-bf5c-4afc-99db-22904bc0b33d
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 5de6710cc300312478d5f734334a1c29faf44920
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35280846"
---
# <a name="putoledbcommand-method"></a>put_OLEDBCommand 方法
此方法不执行任何操作并始终返回，则为 S_OK。  
  
## <a name="syntax"></a>语法  
  
```  
  
HRESULT put_OLEDBCommand(  
      IUnknown *pOLEDBCommand  
);  
```  
  
#### <a name="parameters"></a>Parameters  
 *pOLEDBCommand*  
 [in]指向 OLE DB 命令对象的指针。  
  
## <a name="applies-to"></a>适用范围  
 [IADOCommandConstruction](https://msdn.microsoft.com/library/windows/desktop/aa965677.aspx)
