---
title: "\"存储设置\" 对话框（Analysis Services 多维数据） |Microsoft Docs"
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: analysis-services
ms.topic: conceptual
f1_keywords:
- sql12.asvs.cubeeditor.partitiondesigner.partitionstoragesettings.f1
- sql12.asvs.cubeeditor.cubebuilder.measuregroupstoragesettings.f1
ms.assetid: 80c41c71-226c-45fe-b9cf-af824b592fe1
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: ecd796d2fb2bc37c4c2ad6d9fac00ef4258ec038
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2020
ms.locfileid: "66068028"
---
# <a name="storage-settings-dialog-box-analysis-services---multidimensional-data"></a>“存储设置”对话框（Analysis Services - 多维数据）
  可以使用 **中的** “存储设置” [!INCLUDE[ssBIDevStudioFull](../includes/ssbidevstudiofull-md.md)] 对话框，为维度、多维数据集、度量值组或分区设置主动缓存、存储和通知设置。 在 **中可以通过执行以下操作之一显示** “存储设置” [!INCLUDE[ssBIDevStudioFull](../includes/ssbidevstudiofull-md.md)] 对话框：  
  
-   在的 "**属性**" 窗口中，单击维度、 `ProactiveCaching`多维数据集、度量值组或分区的属性值的省略号按钮（**...**） [!INCLUDE[ssBIDevStudioFull](../includes/ssbidevstudiofull-md.md)]。  
  
-   在 **多维数据集设计器** 的 **“分区”** 选项卡中展开某个度量值组，再单击 **“存储设置”**。  
  
-   在 **多维数据集设计器** 的 **“分区”** 选项卡中展开某个度量值组并在网格中选择该度量值组的分区，再单击 **“存储设置”**。  
  
-   在 **多维数据集设计器** 的 **“分区”** 选项卡中展开某个度量值组并在网格中选择该度量值组的分区，然后在 **多维数据集设计器** 的 **“分区”** 选项卡上的 **“工具栏”** 窗格中单击 **“存储设置”**。  
  
## <a name="options"></a>选项  
  
|术语|定义|值|  
|----------|----------------|------------|  
|**标准设置**|选择此选项可启用 **“标准设置滑块”** ，并使用存储模式和主动缓存功能的预定义设置。||  
|**“标准设置滑块”**|设置为以下预定义设置之一：<br /><br /> **实时 ROLAP**<br /><br /> 选择此设置可以使用以下的存储和主动缓存设置：|ROLAP 存储模式<br /><br /> 启用主动缓存<br /><br /> 放弃过时缓存，滞后期为 0 秒<br /><br /> 使对象立即联机|  
||**实时 HOLAP**<br /><br /> 选择此设置可以使用以下的存储和主动缓存设置：|HOLAP 存储模式<br /><br /> 启用主动缓存<br /><br /> 放弃过时缓存，滞后期为 0 秒<br /><br /> 当数据更改时更新缓存，静默间隔为 0 秒，没有静默覆盖间隔<br /><br /> 使对象立即联机|  
||**低滞后时间 MOLAP**<br /><br /> 选择此设置可以使用以下的存储和主动缓存设置：|MOLAP 存储模式<br /><br /> 启用主动缓存<br /><br /> 放弃过时缓存，滞后期为 30 分钟。<br /><br /> 当数据更改时更新缓存，静默间隔为 10 秒，静默覆盖间隔为 10 分钟<br /><br /> 使对象立即联机|  
||**中等滞后时间 MOLAP**<br /><br /> 选择此设置可以使用以下的存储和主动缓存设置：|MOLAP 存储模式<br /><br /> 启用主动缓存<br /><br /> 放弃过时缓存，滞后期为 4 小时。<br /><br /> 当数据更改时更新缓存，静默间隔为 10 秒，静默覆盖间隔为 10 分钟<br /><br /> 使对象立即联机|  
||**自动 MOLAP**<br /><br /> 选择此设置可以使用以下的存储和主动缓存设置：|MOLAP 存储模式<br /><br /> 启用主动缓存<br /><br /> 当数据更改时更新缓存，静默间隔为 0 秒，没有静默覆盖间隔|  
||**预定的 MOLAP**<br /><br /> 选择此设置可以使用以下的存储和主动缓存设置：|MOLAP 存储模式<br /><br /> 启用主动缓存<br /><br /> 定期更新缓存，重新生成间隔为 1 天|  
||**MOLAP**<br /><br /> 选择此设置可以使用以下的存储和主动缓存设置：|MOLAP 存储模式|  
|**自定义设置**|选择此项可以显式地设置存储模式、主动缓存和通知选项。||  
|**选项**|单击此项可显示 **“存储选项”** 对话框，以显式地设置存储模式、主动缓存和通知选项。 有关****“存储选项”对话框的详细信息，请参阅[“存储选项”对话框（Analysis Services - 多维数据）](storage-options-dialog-box-analysis-services-multidimensional-data.md)。||  
  
## <a name="see-also"></a>另请参阅  
 [&#40;多维数据的 Analysis Services 设计器和对话框&#41;](analysis-services-designers-and-dialog-boxes-multidimensional-data.md)   
 [主动缓存 &#40;分区&#41;](multidimensional-models-olap-logical-cube-objects/partitions-proactive-caching.md)   
 [多维数据集存储 &#40;Analysis Services 多维数据&#41;](multidimensional-models-olap-logical-cube-objects/cube-storage-analysis-services-multidimensional-data.md)  
  
  
