---
title: PDOStatement::debugDumpParams |Microsoft 文档
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: drivers
ms.service: ''
ms.component: php
ms.reviewer: ''
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: cf156d65-d933-4235-b89a-18e172d61c15
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: d09d11b9343b2adc8df132182b51156d066c99bf
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="pdostatementdebugdumpparams"></a>PDOStatement::debugDumpParams
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

显示已准备的语句。  
  
## <a name="syntax"></a>语法  
  
```  
  
bool PDOStatement::debugDumpParams();  
```  
  
## <a name="remarks"></a>注释  
已在 [!INCLUDE[ssDriverPHP](../../includes/ssdriverphp_md.md)]的版本 2.0 中添加了对 PDO 的支持。  
  
## <a name="example"></a>示例  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$param = "Owner";  
  
$stmt = $conn->prepare("select * from Person.ContactType where name = :param");  
$stmt->execute(array($param));  
$stmt->debugDumpParams();  
  
echo "\n\n";  
  
$stmt = $conn->prepare("select * from Person.ContactType where name = ?");  
$stmt->execute(array($param));  
$stmt->debugDumpParams();  
?>  
```  
  
## <a name="see-also"></a>另请参阅  
[PDOStatement 类](../../connect/php/pdostatement-class.md)

[PDO](http://php.net/manual/book.pdo.php)  
  
