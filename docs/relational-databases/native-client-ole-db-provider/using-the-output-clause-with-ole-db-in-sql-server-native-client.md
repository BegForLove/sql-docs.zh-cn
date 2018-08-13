---
title: 使用 SQL Server Native Client 中的 OLE DB 使用 OUTPUT 子句 |Microsoft Docs
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.suite: sql
ms.technology: native-client
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 53deeb99-c088-4fde-844b-b2d91d6de1eb
author: MightyPen
ms.author: genemi
manager: craigg
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017'
ms.openlocfilehash: 3decdc6727fd23d8e219b4edee5cc9290f8c5c9d
ms.sourcegitcommit: 4cd008a77f456b35204989bbdd31db352716bbe6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2018
ms.locfileid: "39563121"
---
# <a name="using-the-output-clause-with-ole-db-in-sql-server-native-client"></a>在 SQL Server Native Client 中对 OLE DB 使用 OUTPUT 子句
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../includes/snac-deprecated.md)]

  如果在 INSERT、UPDATE、DELETE 或 MERGE 命令中使用 OUTPUT 子句，则无法获得受影响的行数。 应用程序必须对 OUTPUT 子句所返回的行集中的行数进行计数。  
  
## <a name="see-also"></a>请参阅  
 [创建 SQL Server Native Client OLE DB 提供程序应用程序](../../relational-databases/native-client-ole-db-provider/creating-a-sql-server-native-client-ole-db-provider-application.md)  
  
  
