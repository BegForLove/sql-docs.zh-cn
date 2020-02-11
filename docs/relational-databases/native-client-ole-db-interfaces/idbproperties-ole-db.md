---
title: IDBProperties （OLE DB） |Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: native-client
ms.topic: reference
ms.assetid: 2e5a4fd8-5164-495a-9986-3477aef8d8a5
author: MightyPen
ms.author: genemi
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 9a4249033987eb9f808b1f9e837418b3ade82f0c
ms.sourcegitcommit: b87d36c46b39af8b929ad94ec707dee8800950f5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2020
ms.locfileid: "73789430"
---
# <a name="idbproperties-ole-db"></a>IDBProperties (OLE DB)
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]

  OLE DB 标准规范允许提供程序为 DBPROPINFO::vValues 指定 VT_EMPTY****。 但是， [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]在调用**IDBProperties：： GetPropertyInfo**和**DBPROPSET_ROWSETALL**检索行集属性时，Native Client OLE DB 始终返回 VT_EMPTY。  
  
## <a name="see-also"></a>另请参阅  
 [接口 &#40;OLE DB&#41;](https://msdn.microsoft.com/library/34c33364-8538-45db-ae41-5654481cda93)  
  
  
