---
title: 创建、 更改和删除表 |Microsoft 文档
ms.custom: ''
ms.date: 08/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.service: ''
ms.component: smo
ms.reviewer: ''
ms.suite: sql
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- tables [SMO]
ms.assetid: ff0bcfff-812f-4999-b0c7-736a97804c2b
caps.latest.revision: 48
author: stevestein
ms.author: sstein
manager: craigg
monikerRange: = azuresqldb-current || = azure-sqldw-latest || >= sql-server-2016 || = sqlallproducts-allversions
ms.openlocfilehash: 40f8a8ceead774cbb8966ddb2d97534c9357bbca
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="creating-altering-and-removing-tables"></a>创建、更改和删除表
[!INCLUDE[appliesto-ss-asdb-asdw-xxx-md](../../../includes/appliesto-ss-asdb-asdw-xxx-md.md)]
  在 [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] 管理对象 (SMO) 中，表通过 <xref:Microsoft.SqlServer.Management.Smo.Table> 对象来表示。 在 SMO 对象层次结构中，<xref:Microsoft.SqlServer.Management.Smo.Table> 对象位于 <xref:Microsoft.SqlServer.Management.Smo.Database> 对象的下方。  
  
## <a name="example"></a>示例  
 若要使用所提供的任何代码示例，您必须选择创建应用程序所需的编程环境、模板和语言。 有关详细信息，请参阅[创建 Visual C&#35; Visual Studio.NET 中的 SMO 项目](../../../relational-databases/server-management-objects-smo/how-to-create-a-visual-csharp-smo-project-in-visual-studio-net.md)。  
  
## <a name="creating-altering-and-removing-a-table-in-visual-basic"></a>在 Visual Basic 中创建、更改和删除表  
 此代码示例创建了一个包含若干具有不同类型和用途的列的表。 此代码还提供了有关以下内容的示例：如何创建标识字段、如何创建主键以及如何更改表属性。  
  
```VBNET
'Connect to the local, default instance of SQL Server.
Dim srv As Server
srv = New Server
'Reference the AdventureWorks2012 2008R2 database.
Dim db As Database
db = srv.Databases("AdventureWorks2012")
'Define a Table object variable by supplying the parent database and table name in the constructor. 
Dim tb As Table
tb = New Table(db, "Test_Table")
'Add various columns to the table.
Dim col1 As Column
col1 = New Column(tb, "Name", DataType.NChar(50))
col1.Collation = "Latin1_General_CI_AS"
col1.Nullable = True
tb.Columns.Add(col1)
Dim col2 As Column
col2 = New Column(tb, "ID", DataType.Int)
col2.Identity = True
col2.IdentitySeed = 1
col2.IdentityIncrement = 1
tb.Columns.Add(col2)
Dim col3 As Column
col3 = New Column(tb, "Value", DataType.Real)
tb.Columns.Add(col3)
Dim col4 As Column
col4 = New Column(tb, "Date", DataType.DateTime)
col4.Nullable = False
tb.Columns.Add(col4)
'Create the table on the instance of SQL Server.
tb.Create()
'Add another column.
Dim col5 As Column
col5 = New Column(tb, "ExpiryDate", DataType.DateTime)
col5.Nullable = False
tb.Columns.Add(col5)
'Run the Alter method to make the change on the instance of SQL Server.
tb.Alter()
'Remove the table from the database.

tb.Drop()
``` 
  
## <a name="creating-altering-and-removing-a-table-in-visual-c"></a>在 Visual C# 中创建、更改和删除表  
 此代码示例创建了一个包含若干具有不同类型和用途的列的表。 此代码还提供了有关以下内容的示例：如何创建标识字段、如何创建主键以及如何更改表属性。  
  
```csharp  
{  
            //Connect to the local, default instance of SQL Server.   
        Server srv;   
        srv = new Server();   
        //Reference the AdventureWorks2012 database.   
        Database db;   
        db = srv.Databases["AdventureWorks2012"];   
        //Define a Table object variable by supplying the parent database and table name in the constructor.   
        Table tb;   
        tb = new Table(db, "Test_Table");   
        //Add various columns to the table.   
        Column col1;   
        col1 = new Column(tb, "Name", DataType.NChar(50));   
        col1.Collation = "Latin1_General_CI_AS";   
        col1.Nullable = true;   
        tb.Columns.Add(col1);   
        Column col2;   
        col2 = new Column(tb, "ID", DataType.Int);   
        col2.Identity = true;   
        col2.IdentitySeed = 1;   
        col2.IdentityIncrement = 1;   
        tb.Columns.Add(col2);   
        Column col3;   
        col3 = new Column(tb, "Value", DataType.Real);   
        tb.Columns.Add(col3);   
        Column col4;   
        col4 = new Column(tb, "Date", DataType.DateTime);   
        col4.Nullable = false;   
        tb.Columns.Add(col4);   
        //Create the table on the instance of SQL Server.   
        tb.Create();   
        //Add another column.   
        Column col5;   
        col5 = new Column(tb, "ExpiryDate", DataType.DateTime);   
        col5.Nullable = false;   
        tb.Columns.Add(col5);   
        //Run the Alter method to make the change on the instance of SQL Server.   
        tb.Alter();   
        //Remove the table from the database.   
        tb.Drop();   
        }  
```  
  
## <a name="creating-altering-and-removing-a-table-in-powershell"></a>在 PowerShell 中创建、更改和删除表  
 此代码示例创建了一个包含若干具有不同类型和用途的列的表。 此代码还提供了有关以下内容的示例：如何创建标识字段、如何创建主键以及如何更改表属性。  
  
```powershell  
#Load the assembly containing the objects used in this example  
[reflection.assembly]::LoadWithPartialName("Microsoft.SqlServer.Types")  
  
# Set the path context to the local, default instance of SQL Server.  
CD \sql\localhost\default\Databases\  
  
#And the database object corresponding to AdventureWorks2012.  
$db = get-item AdventureWorks2012  
  
#Create a SMO Table  
$tb = New-Object -TypeName Microsoft.SqlServer.Management.SMO.Table -argumentlist $db, "Test_Table"  
  
#Add various columns to the table.   
$Type = [Microsoft.SqlServer.Management.SMO.DataType]::NChar(50)  
$col1 =  New-Object -TypeName Microsoft.SqlServer.Management.SMO.Column -argumentlist $tb,"Name", $Type  
$col1.Collation = "Latin1_General_CI_AS"  
$col1.Nullable = $true  
$tb.Columns.Add($col1)  
  
$Type = [Microsoft.SqlServer.Management.SMO.DataType]::Int  
$col2 =  New-Object -TypeName Microsoft.SqlServer.Management.SMO.Column -argumentlist $tb,"ID", $Type  
$col2.Identity = $true  
$col2.IdentitySeed = 1  
$col2.IdentityIncrement = 1  
$tb.Columns.Add($col2)   
  
$Type = [Microsoft.SqlServer.Management.SMO.DataType]::Real  
$col3 =  New-Object -TypeName Microsoft.SqlServer.Management.SMO.Column -argumentlist $tb,"Value", $Type  
$tb.Columns.Add($col3)   
  
$Type = [Microsoft.SqlServer.Management.SMO.DataType]::DateTime  
$col4 =  New-Object -TypeName Microsoft.SqlServer.Management.SMO.Column -argumentlist $tb,"Date", $Type  
$col4.Nullable = $false  
$tb.Columns.Add($col4)   
  
#Create the table  
$tb.Create()  
  
$Type = [Microsoft.SqlServer.Management.SMO.DataType]::DateTime  
$col5 =  New-Object -TypeName Microsoft.SqlServer.Management.SMO.Column -argumentlist $tb,"ExpiryDate", $Type  
$col5.Nullable = $false  
$tb.Columns.Add($col5)   
  
#Run the Alter method to make the change on the instance of SQL Server.   
$tb.Alter()  
  
#Remove the table from the database.   
$tb.Drop()  
  
```  
  
## <a name="see-also"></a>另请参阅  
 <xref:Microsoft.SqlServer.Management.Smo.Table>  
  
  
