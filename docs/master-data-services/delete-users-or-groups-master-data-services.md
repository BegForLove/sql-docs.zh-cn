---
title: 删除用户或组 (Master Data Services) | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: mds
ms.reviewer: ''
ms.technology: master-data-services
ms.topic: conceptual
helpviewer_keywords:
- deleting groups [Master Data Services]
- groups [Master Data Services], deleting
- users [Master Data Services], deleting
- deleting users [Master Data Services]
ms.assetid: 0bbf9d2c-b826-48bb-8aa9-9905db6e717f
author: lrtoyou1223
ms.author: lle
ms.openlocfilehash: 81b16bc5b2bc8f2158a82733fb96f5144b7d15f9
ms.sourcegitcommit: b2464064c0566590e486a3aafae6d67ce2645cef
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/15/2019
ms.locfileid: "67906269"
---
# <a name="delete-users-or-groups-master-data-services"></a>删除用户或组 (Master Data Services)

[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-winonly](../includes/appliesto-ss-xxxx-xxxx-xxx-md-winonly.md)]

  在您不再希望用户或组访问 [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)]时删除它们。  
  
 在删除用户和组时请注意以下行为：  
  
-   如果您删除的用户是有权访问 [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)]的组的成员，则在您从 Active Directory 或本地组中删除该用户之前，该用户仍能够访问 [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)] 。  
  
-   如果您删除某一组，则该组中有权访问 [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)] 的所有用户都将在您删除它们之前显示在 **“用户”** 列表中。  
  
-   对安全性所做的更改在 20 分钟之内不会传播到 MDS [!INCLUDE[ssMDSXLS](../includes/ssmdsxls-md.md)] 。  
  
## <a name="prerequisites"></a>先决条件  
 若要执行此过程：  
  
-   您必须有权访问 **“用户和组权限”** 功能区域。  
  
### <a name="to-delete-users-or-groups"></a>删除用户或组  
  
1.  在 [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)]中，单击 **“用户和组权限”** 。  
  
2.  若要删除某一用户，请保持在 **“用户”** 页上。 若要删除某一组，请从菜单栏中单击“管理组”  。  
  
3.  在网格中，选择你要删除的用户或组所对应的行。  
  
4.  单击 **“删除所选用户”** 或 **“删除所选组”** 。  
  
5.  在确认对话框中，单击 **“确定”** 。  
  
## <a name="see-also"></a>请参阅  
 [安全性 (Master Data Services)](../master-data-services/security-master-data-services.md)  
  
  
