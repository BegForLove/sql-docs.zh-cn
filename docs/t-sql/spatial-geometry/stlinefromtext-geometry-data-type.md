---
title: STLineFromText（geometry 数据类型）| Microsoft Docs
ms.custom: ''
ms.date: 10/11/2019
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
f1_keywords:
- STLineFromText (geometry Data Type)
- STLineFromText_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- STLineFromText (geometry Data Type)
ms.assetid: 430508ad-207b-4dee-a4d1-4ddf25e6b4a9
author: MladjoA
ms.author: mlandzic
ms.openlocfilehash: a0a912e4ab228617537e9c28e9a5cecc4a0278fe
ms.sourcegitcommit: 58158eda0aa0d7f87f9d958ae349a14c0ba8a209
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/30/2020
ms.locfileid: "72278137"
---
# <a name="stlinefromtext-geometry-data-type"></a>STLineFromText（geometry 数据类型）
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

从开放地理空间信息联盟 (OGC) 熟知文本 (WKT) 表示形式返回 geometry 实例，增加了该实例传递的任何 Z（标高）和 M（度量）值  。
  
## <a name="syntax"></a>语法  
  
```  
  
STLineFromText ( 'linestring_tagged_text' , SRID )  
```  
  
## <a name="arguments"></a>参数  
 linestring_tagged_text   
 希望返回的 geometryLineString 实例的 WKT 表示形式  。 linestring_tagged_text 是一个 nvarchar(max) 表达式   。  
  
 SRID   
 一个 int 表达式，表示希望返回的 geometryLineString 实例的空间引用 ID (SRID)   。  
  
## <a name="return-types"></a>返回类型  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 返回类型：geometry   
  
 CLR 返回类型：**SqlGeometry**  
  
 OGC 类型：**LineString**  
  
## <a name="remarks"></a>备注  
如果输入的格式不正确，此方法将引发 FormatException  。 不支持 SQL 规范版本 1.2.1 的开放地理空间信息联盟 (OGC) 简单功能中的三维和测量几何图形 WKT 表示法。 请查看 Z（标高）和 M（度量）值的支持表示形式的示例。
  
## <a name="examples"></a>示例  
 下面的示例使用 `STLineFromText()` 创建 `geometry` 实例。

### <a name="example-1-two-dimension-geometry-wkt"></a>示例 1：二维几何图形 WKT
```  
DECLARE @g geometry;  
SET @g = geometry::STLineFromText('LINESTRING (100 100, 200 200)', 0);  
SELECT @g.ToString();  
```  
  
### <a name="example-2-three-dimension-geometry-wkt"></a>示例 2：三维几何图形 WKT
```  
DECLARE @g geometry;  
SET @g = geometry::STLineFromText('LINESTRING (100 100 100, 200 200 200)', 0);  
SELECT @g.ToString();  
``` 

### <a name="example-3-two-dimension-measured-geometry-wkt"></a>示例 3：二维测量几何图形 WKT
```  
DECLARE @g geometry;  
SET @g = geometry::STLineFromText('LINESTRING (100 100 NULL 100, 200 200 NULL 200)', 0);  
SELECT @g.ToString();  
``` 

### <a name="example-4-three-dimension-measured-geometry-wkt"></a>示例 4：三维测量几何图形 WKT
```  
DECLARE @g geometry;  
SET @g = geometry::STLineFromText('LINESTRING (100 100 100 100, 200 200 200 200)', 0);  
SELECT @g.ToString();  
``` 
## <a name="see-also"></a>另请参阅  
 [OGC 静态几何图形方法](../../t-sql/spatial-geometry/ogc-static-geometry-methods.md)  
  
  

