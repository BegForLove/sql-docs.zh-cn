---
title: 过程删除方法示例 (VB) |Microsoft 文档
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
dev_langs:
- VB
helpviewer_keywords:
- Delete method [ADOX], Visual Basic example
ms.assetid: 94f1ac93-e778-4a40-a85e-94bce5316ac7
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: e3ff286753b12fa5e648d5d43bf8bb4c360a441a
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35286686"
---
# <a name="procedures-delete-method-example-vb"></a>过程删除方法示例 (VB)
下面的代码演示如何通过删除过程[删除](../../../ado/reference/adox-api/delete-method-adox-collections.md)方法[过程](../../../ado/reference/adox-api/procedures-collection-adox.md)集合。  
  
```  
' BeginDeleteProcedureVB  
Sub Main()  
    On Error GoTo DeleteProcedureError  
  
    Dim cat As New ADOX.Catalog  
  
    ' Open the catalog.  
    cat.ActiveConnection = _  
        "Provider='Microsoft.Jet.OLEDB.4.0';" & _  
        "Data Source='Northwind.mdb';"  
  
    ' Delete the procedure.  
    cat.Procedures.Delete "CustomerById"  
  
    'Clean up.  
    Set cat.ActiveConnection = Nothing  
    Set cat = Nothing  
    Exit Sub  
  
DeleteProcedureError:  
    Set cat = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
' EndDeleteProcedureVB  
```  
  
## <a name="see-also"></a>请参阅  
 [ActiveConnection 属性 (ADOX)](../../../ado/reference/adox-api/activeconnection-property-adox.md)   
 [目录对象 (ADOX)](../../../ado/reference/adox-api/catalog-object-adox.md)   
 [Delete 方法 （ADOX 集合）](../../../ado/reference/adox-api/delete-method-adox-collections.md)   
 [过程对象 (ADOX)](../../../ado/reference/adox-api/procedure-object-adox.md)   
 [过程集合 (ADOX)](../../../ado/reference/adox-api/procedures-collection-adox.md)
