---
title: 配置专用数据刷新或仅限查询的处理（PowerPivot for SharePoint） |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: analysis-services
ms.topic: conceptual
ms.assetid: 5e027605-1086-4941-bb01-f315df8f829b
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: eaf62d2bbe6e6becc21bbf5e870c9fe442c96f74
ms.sourcegitcommit: 6fd8c1914de4c7ac24900fe388ecc7883c740077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2020
ms.locfileid: "66087513"
---
# <a name="configure-dedicated-data-refresh-or-query-only-processing-powerpivot-for-sharepoint"></a>配置专用数据刷新或仅限查询的处理 (PowerPivot for SharePoint)
  在 SharePoint 集成模式下，可以将 Analysis Services 服务器实例配置为支持特定类型的处理请求，如数据刷新或仅限查询的处理。 默认情况下，支持这两种类型的负载请求。 您可以关闭任一类型，以创建专用查询引擎或数据刷新服务器。  
  
 **[!INCLUDE[applies](../includes/applies-md.md)]** SharePoint 2010  
  
> [!NOTE]  
>  在此版本中，没有相应的配置设置可用来将内存或 CPU 使用率限制为数据刷新作业或按需查询。 [!INCLUDE[ssGeminiSrv](../includes/ssgeminisrv-md.md)]实例将使用所有可用资源来运行它正在管理的查询和数据刷新作业。  
  
 本主题包含以下各节：  
  
 [配置处理模式](#config)  
  
 [更改可并行运行的数据刷新作业的数目](#change)  
  
##  <a name="configure-a-processing-mode"></a><a name="config"></a>配置处理模式  
  
1.  在管理中心的 "系统设置" 中，单击 "**管理服务器上的服务**"。  
  
2.  在本页顶部的“服务器”中，单击下箭头，然后单击 **“更改服务器”**。  
  
3.  选择具有您要配置的 Analysis Services 服务器实例的 SharePoint 服务器。  
  
4.  单击 **SQL Server Analysis Services**。  
  
5.  在“服务实例使用情况”中，执行以下操作之一：  
  
    1.  清除 "**启用加载只读数据库**" 复选框，以关闭在用户打开包含 PowerPivot 数据的工作簿时进行的按需查询处理。  
  
    2.  清除 "启用为**刷新加载数据库**" 复选框，关闭计划的数据刷新。  
  
    > [!NOTE]  
    >  关闭数据刷新并不会从 SharePoint 站点中删除数据刷新选项。 拥有 PowerPivot 工作簿的用户仍可以创建数据刷新计划，但该服务器上不会发生数据刷新。  
  
6.  对于数据刷新操作，您还可以选择更改并发刷新作业数目。 如果服务器配置为仅进行数据刷新或如果服务器上有其他处理器，则建议增加并发作业数目。 如果您要释放系统资源以进行更多的按需查询，则可以减少并发作业数目。  
  
7.  保存所做更改。 在发生处理事件之前，服务器将不验证您的条目。 如果您输入的并发作业数目无效，则在处理下一个请求时，系统将检测到并记录此错误。  
  
##  <a name="change-the-number-of-data-refresh-jobs-that-can-run-in-parallel"></a><a name="change"></a>更改可并行运行的数据刷新作业数  
 数据刷新作业是一项计划的任务，它添加到由 PowerPivot 服务应用程序维护和监视的处理队列中。 作业由 PowerPivot 工作簿中一个或多个数据源的计划信息组成。 将为每个定义的计划创建一个单独的作业。 如果工作簿所有者为所有数据源定义了一个计划，则将只为整个数据刷新操作创建一个作业。 如果工作簿所有者为外部数据源创建单独的计划，则将创建和运行多个作业，以完成该工作簿的完全数据刷新。  
  
 如果系统有能力支持额外负载，则可以增加可同时运行的数据刷新作业数目。  
  
|设置|有效值|说明|  
|-------------|------------------|-----------------|  
|默认值|基于 RAM 进行计算。|默认值基于可用内存量除以 4 GB 后的结果。 默认值由公式计算得出，以便可以根据系统的容量调整设置。<br /><br /> 注意：根据实际 PowerPivot 数据源的大采样的 RAM 使用情况，选择 4 gb 除数。 而不依据 PowerPivot 物理或逻辑体系结构。|  
|最大值|基于 CPU 数量进行计算。|您可以指定的最大并发作业数目基于计算机上的处理器数量。 例如，在 4 插槽四核计算机上，您可以并行运行的最大作业数目为 16。|  
  
#### <a name="increasing-the-default-value-to-a-higher-value"></a>提高默认值  
 下图显示 RAM 和 CPU 的不同组合，以及基于系统特性计算出的默认值和最大值。 请记住，可同时运行的数据刷新作业数的计算默认值是基于系统内存的，而计算的最大值是基于 CPU 的。 最后一列指示您是否可以增加并行数据刷新作业的最大数目。  
  
|实际 RAM（以 GB 为单位）|计算的默认值|CPU 实际数量|计算的最大值|是否增加并发作业数目？|  
|---------------------------------|------------------------------|------------------------|------------------------------|-------------------------------|  
|4|1|1|1|否。 默认值和最大值相同。|  
|4|1|4|4|是的。 您可以将并发作业数目增加到 2、3 或 4。|  
|8|2|4|4|是的。 您可以将并发作业数目增加到 3 或 4。|  
|16|4|4|4|否。 默认值和最大值相同。|  
|32|使用计算默认值的公式，默认值将是 8。 因为该默认值高于允许的最大值，所以，计算出的默认值在此情况下不使用。|4|4|否。 虽然 RAM 较大可能指示默认 8 个并发作业，但具有 4 个处理器的计算机最多仅支持 4 个并发作业。|  
|32|8|8|8|否。|  
|32|8|16|16|是的。|  
|64|16|16|16|否。|  
  
 因为无法提前知道多个作业是否能够同时成功运行，所以，您只应在分析了内存使用量随时间的变化趋势，并确定服务器内存通常处于利用不足状态时，才增加并发作业的数目。  
  
 每个数据刷新作业都具有不同的负载特征，具体取决于所刷新的数据源的数量和大小。 具有单个数据源且行数较少的工作簿与具有大量数据源和大量行集的工作簿相比，前者的处理负载要轻得多。  
  
## <a name="see-also"></a>另请参阅  
 [使用 SharePoint 2010 进行 PowerPivot 数据刷新](powerpivot-data-refresh-with-sharepoint-2010.md)  
  
  
