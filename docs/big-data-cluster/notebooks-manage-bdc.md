---
title: 管理：Azure Data Studio 笔记本
titleSuffix: SQL Server Big Data Clusters
description: 使用 Azure Data Studio 中的笔记本管理大数据群集和排除其故障。
author: yualan
ms.author: alanyu
ms.reviewer: mikeray
ms.metadata: seo-lt-2019
ms.date: 03/30/2020
ms.topic: conceptual
ms.prod: sql
ms.technology: big-data-cluster
ms.openlocfilehash: 28ba612c1932dd511ee0cd99a2aa97dd127d63f7
ms.sourcegitcommit: 1124b91a3b1a3d30424ae0fec04cfaa4b1f361b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2020
ms.locfileid: "80531330"
---
# <a name="manage-sql-server-big-data-clusters-with-azure-data-studio-notebooks"></a>使用 Azure Data Studio 笔记本管理 SQL Server 大数据群集

[!INCLUDE[tsql-appliesto-ssver15-xxxx-xxxx-xxx](../includes/tsql-appliesto-ssver15-xxxx-xxxx-xxx.md)]

[!INCLUDE[sql-server-2019](../includes/sssqlv15-md.md)] 为包含笔记本的 Azure Data Studio 提供扩展。 笔记本提供可在 Azure Data Studio 中用于管理 SQL Server 2019 大数据群集的文档和代码。

[笔记本](../azure-data-studio/notebooks-guidance.md)最初作为开放源代码项目实现，现已并入 [Azure Data Studio](https://docs.microsoft.com/sql/azure-data-studio/download)。 可以在文本单元格中使用 markdown 作为文本，并使用其中一个可用核心在代码单元格中编写代码。

可以使用笔记本为 [!INCLUDE[sql-server-2019](../includes/sssqlv15-md.md)] 部署大数据群集。

除了笔记本之外，还可以查看一组称为 Jupyter Book 的笔记本。 Jupyter Book 提供用于帮助浏览笔记本集合的目录，这样，无论是想对 SQL Server 进行故障排除还是查看群集状态，都可以轻松找到所需的笔记本。

## <a name="prerequisites"></a>先决条件

若要打开一个笔记本，需要满足以下先决条件：

* 已安装 [Azure Data Studio 预览体验内部版本](https://aka.ms/azuredatastudio-rc)的最新版本
* 已在 Azure Data Studio 中安装 [!INCLUDE[sql-server-2019](../includes/sssqlv15-md.md)] 扩展

除了上述先决条件，若要部署 SQL Server 2019 大数据群集，还需要：

* [azdata](deploy-install-azdata.md)
* [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-binary-using-native-package-management)
* [Azure CLI](/cli/azure/install-azure-cli)

## <a name="access-troubleshooting-notebooks"></a>访问故障排除笔记本

可通过三种方法访问故障排除笔记本。

### <a name="command-palette"></a>命令面板

1. 选择“查看” > “命令面板”   。

2. 输入“Jupyter Books：  SQL Server 2019 指南”。

Jupyter Books 视图窗口随即打开，其中显示有包含与 SQL Server 大数据群集相关的故障排除笔记本的 Jupyter Book。

### <a name="sql-master-dashboard"></a>SQL 主仪表板

1. 安装 Azure Data Studio 预览体验内部版本后，连接到 SQL Server 大数据群集实例。

2. 连接到实例后，在“连接”下右键单击相应服务器名称，然后选择“管理”   。

3. 在仪表板上，选择“SQL Server 大数据群集”  。 选择“SQL Server 2019 指南”，打开包含所需笔记本的 Jupyter Book  。
    ![仪表板中的 Jupyter 笔记本](media/manage-notebooks/jupyter-book-button.png)

4. 选择需要完成的任务的笔记本。

### <a name="controller-dashboard"></a>控制器仪表板

1. 在“连接”视图中，展开“SQL Server 大数据群集”   。

2. 添加控制器终结点详细信息。

3. 连接到控制器后，右键单击终结点，然后选择“管理”  。

4. 在仪表板加载后，选择“故障排除”以打开 Jupyter Book 故障排除指南  。

## <a name="use-troubleshooting-notebooks"></a>使用故障排除笔记本

1. 在 Jupyter Book 目录中找到所需的故障排除指南。

2. 笔记本已经过优化，因此只需选择“运行单元”  。 此操作将单独运行笔记本中的每个单元，直到笔记本运行完成。

3. 如果发现错误，Jupyter Book 将建议一个可运行以修复错误的笔记本。 按照建议的步骤操作，然后再次运行该笔记本。

## <a name="change-the-big-data-cluster"></a>更改大数据群集

更改笔记本的 SQL Server 大数据群集：

1. 单击笔记本工具栏中的“附加到”菜单  。

   ![单击笔记本工具栏中的“附加到”菜单](./media/notebooks-how-to-manage/select-attach-to-1.png)

2. 单击“附加到”菜单中的服务器  。

   ![选择“附加到”菜单中的服务器](./media/notebooks-how-to-manage/select-attach-to-2.png)

## <a name="next-steps"></a>后续步骤

有关 Azure Data Studio 中的笔记本的详细信息，请参阅[如何在 SQL Server 中使用笔记本](../azure-data-studio/notebooks-guidance.md)。
