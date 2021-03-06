---
title: 查询选项结果（文本页） |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: database-engine
ms.topic: conceptual
f1_keywords:
- sql12.swb.query.text.f1
ms.assetid: fd2fb409-58f9-4ede-8349-ce007126b68d
author: rothja
ms.author: jroth
manager: craigg
ms.openlocfilehash: c8b41a624335026c3c20bd0d7b1d037d1ec55d06
ms.sourcegitcommit: 4b5919e3ae5e252f8d6422e8e6fddac1319075a1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/09/2020
ms.locfileid: "83000567"
---
# <a name="query-options-results-text-page"></a>“查询选项”中的“结果”（“文本”页）
  使用此页可以指定以文本格式显示查询结果集的选项。 在选择 **“将结果保存到文件”** 时也会应用此页上的设置。  
  
 **输出格式**  
 默认情况下，将在通过用空格分隔结果而得到的列中显示输出。 您还可以使用逗号、制表符或空格来分隔列。 选中 **“自定义分隔符”** 复选框，可以在 **“自定义分隔符”** 框中指定其他分隔字符。  
  
 **“自定义分隔符”**  
 自行指定用于分隔列的字符。 只有在 **“输出格式”** 框中选中 **“自定义分隔符”** 复选框后，才可使用此选项。  
  
 **在结果集中包括列标题**  
 如果不希望每列都带有列标题，请清除此复选框。  
  
 **接收到结果时滚动**  
 选中此复选框将使得结果集的显示侧重于结尾处最近返回的记录。 清除此复选框，则使其侧重于接收到的前几行。  
  
 **右对齐数值**  
 选中此复选框可以将数值与列的右侧对齐。 这样，就可以更方便地查看具有固定小数位数的数值。  
  
 **在执行查询后放弃结果**  
 当屏幕显示接收到查询结果之后，通过放弃查询结果来释放内存。  
  
 **在单独选项卡中显示结果**  
 选中此复选框可在新文档窗口中显示结果集，而不是在查询文档窗口的底部显示。  
  
 **执行查询后切换到“结果”选项卡**  
 单击此项可将屏幕焦点自动设置到结果集。  
  
 **每列中显示的最大字符数**  
 此值默认为 256。 增大此值可显示更大的结果集，而不会将其截断。  
  
 **重置为默认值**  
 将此页上的所有值重置为原始默认值。  
  
## <a name="saving-a-text-result-set-with-headers"></a>使用标题保存文本结果集  
 若要将查询结果保存为带有标题的文本文件，请选中 **“在结果集中包括列标题”** 复选框，并选择一种带分隔符的输出格式。 现在，如果单击工具栏上的****“将结果保存到文件”，或者右键单击任何查询结果，再单击****“将结果另存为”，并键入一个文件名，然后单击****“保存”，报表文件将包含标题。  
  
  
