---
title: 打开具有特定查询字符串参数的移动报表 | Microsoft Docs
description: 对于具有参数和数据源的 Reporting Services 移动报表，可以在报表 URL 中使用查询参数，以使用指定值打开它。
ms.date: 10/25/2016
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.technology: mobile-reports
ms.topic: conceptual
ms.assetid: 4eeb3204-e207-4ac0-aff3-bfc4926e5754
author: maggiesMSFT
ms.author: maggies
ms.openlocfilehash: f953a8ee9371f3e8919d53f017f27a7e863a52ca
ms.sourcegitcommit: ff82f3260ff79ed860a7a58f54ff7f0594851e6b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2020
ms.locfileid: "79448391"
---
# <a name="open-a-mobile-report-with-specific-query-string-parameters--reporting-services"></a>打开具有特定查询字符串参数的移动报表 | Reporting Services
如果有带有参数的 [!INCLUDE[ssRSnoversion_md](../../includes/ssrsnoversion-md.md)] 移动报表和 [!INCLUDE[ssNoVersion_md](../../includes/ssnoversion-md.md)] 或 [!INCLUDE[ssASnoversion_md](../../includes/ssasnoversion-md.md)] 数据源，则可以在报表 URL 中包括查询字符串参数，以便根据已指定的值自动打开报表。 
1.  创建 [带参数的移动报表](../../reporting-services/mobile-reports/add-parameters-to-a-mobile-report-reporting-services.md)。

2. 在移动报表发布服务器中打开报表，并选择“数据”选项卡。 

2. 查找选项卡上表底部的数据集的名称和所需的字段名称。 
    
    ![mobile-report-publisher-parameter-data-view](../../reporting-services/mobile-reports/media/mobile-report-publisher-parameter-data-view.png)
    
2.  URL 的语法取决于数据源。 

     **对于 SQL Server Analysis Services 数据源**：生成具有以下格式的带查询字符串参数的 URL：

    `https://<servername>/reports/<report-folder-name>/<report-name>?<dataset-name>.<field-name>=<parameter-value>`

    例如：
    
    `https://sampleserver/reports/adventureworks-reports/adventureworks-load-on-demand?TimeChartLoD.category=Clothing` 
    
     **对于 SQL Server 数据源**：查询字符串参数几乎相同，区别在于字段名称前面有 \@ 符号：

    `https://<servername>/reports/<report-folder-name>/<report-name>?<dataset-name>.@<field-name>=<parameter-value>`

    例如：
    
      `https://sampleserver/reports/adventureworks-reports/adventureworks-load-on-demand?TimeChartLoD.@category=Clothing` 

    
3.  此 URL 会在服务器上打开报表，并且自动按你指定的参数值进行筛选。

    ![mobile-report-publisher-parameter-web-portal-view](../../reporting-services/mobile-reports/media/mobile-report-publisher-parameter-web-portal-view.png)

### <a name="see-also"></a>另请参阅

[将参数添加到移动报表](../../reporting-services/mobile-reports/add-parameters-to-a-mobile-report-reporting-services.md)

