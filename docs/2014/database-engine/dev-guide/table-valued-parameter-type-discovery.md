---
title: 表值参数类型发现 | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: database-engine
ms.topic: reference
helpviewer_keywords:
- table-valued parameters, type discovery
ms.assetid: f55818c2-ebb5-4cf6-8c0c-0da41f592560
author: mashamsft
ms.author: mathoma
manager: craigg
ms.openlocfilehash: cf3f7b4d6754902ac38172ffa0e8fc392599d307
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2020
ms.locfileid: "62780316"
---
# <a name="table-valued-parameter-type-discovery"></a>表值参数类型发现
  使用者（即使用[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client OLE DB 提供程序的客户端应用程序）可以发现每个命令参数的类型（如果命令文本已提供给 OLE DB 提供程序）。 了解表值参数的类型之后，使用者可以发现表值参数各列的元数据信息。  
  
 对于多数参数类型，ICommandWithParameters::GetParameterInfo 都支持过程参数的类型信息。 从开始[!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)]，由于引入了用户定义的类型和`xml`数据类型，GetParameterInfo 方法不足以实现此目的，因为不能通过 ICommandWithParameters 提供用户定义的类型信息（名称、架构和目录）。 因此，定义了一个新接口 ISSCommandWithParameters 来提供扩展类型信息。  
  
 对于表值参数，同样使用 ISSCommandWithParameters 接口发现详细信息。 在准备好命令对象之后，客户端调用 ISSCommandWithParameters::GetParameterInfo。 对于表值参数，访问接口将 DBPARAMINFO 结构的 wType 成员设置为 DBTYPE_TABLE**。 DBPARAMINFO 结构的 ulParamSize 字段的值为 ~0**。  
  
 使用者随后使用 ISSCommandWithParameters::GetParameterProperties 请求获取附加属性（表值参数类型目录名称、表值参数类型架构名称、表值参数类型名称、列排序和默认列）。  
  
 了解类型名称之后，要检索各个列信息，使用者必须调用 IOpenRowset::OpenRowsetor ，或者通过将表值参数类型名称指定为表名来获取 DBSCHEMA_TABLE_TYPE_COLUMNS 行集。  
  
## <a name="see-also"></a>另请参阅  
 [表值参数 &#40;OLE DB&#41;](../../relational-databases/native-client-ole-db-table-valued-parameters/table-valued-parameters-ole-db.md)   
 [使用表值参数 (OLE DB)](../../relational-databases/native-client-ole-db-how-to/use-table-valued-parameters-ole-db.md)  
  
  
