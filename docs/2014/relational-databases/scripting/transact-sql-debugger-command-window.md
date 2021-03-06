---
title: “命令”窗口
ms.custom: seo-lt-2019
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: database-engine
ms.topic: conceptual
helpviewer_keywords:
- Command Window [Transact-SQL]
ms.assetid: e567ebf9-0793-451b-92c7-26193a02d9da
author: rothja
ms.author: jroth
manager: craigg
ms.openlocfilehash: a7f8e72831e333323621279a0403e95e6a134860
ms.sourcegitcommit: b72c9fc9436c44c6a21fd96223c73bf94706c06b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/01/2020
ms.locfileid: "82718417"
---
# <a name="command-window"></a>“命令”窗口
  使用“命令窗口”  可以对“[!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)] 查询编辑器”窗口中当前所调试的代码运行命令，例如调试和编辑命令。 只有在调试模式下才可以使用 **“命令窗口”** 。 [!INCLUDE[tsql](../../includes/tsql-md.md)] 调试器支持许多在 [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]“命令”  窗口中支持的命令。 有关详细信息，请参阅 [Visual Studio“命令”窗口](https://go.microsoft.com/fwlink/?LinkId=112007)。  
  
## <a name="task-list"></a>任务列表  
 **访问“命令”窗口**  
  
-   在 **“调试”** 菜单中，单击 **“启动调试”** 。  
  
 **打印变量的值**  
  
-   在“命令窗口”  中，键入 **Debug.Print \<VariableName>** ，然后按 Enter 键。  
  
 **列出有关当前线程的信息**  
  
-   在**命令**中，键入 `Debug.ListThread` ，然后按 enter。  
  
 **将变量添加到“快速监视”窗口**  
  
-   在“命令窗口”  中，键入 **Debug.QuickWatch \<VariableName>** ，然后按 Enter 键。  
  
## <a name="see-also"></a>另请参阅  
 [Transact-SQL 调试器](transact-sql-debugger.md)  
