---
title: 使用 IRow::Open 和 ISequentialStream 提取 BLOB 数据 | Microsoft Docs
description: 使用 IRow::Open 和 ISequentialStream 提取 BLOB 数据
ms.custom: ''
ms.date: 06/14/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- fetching BLOB data
- Open method
- ISequentialStream interface
- BLOBs, fetching
author: pmasl
ms.author: pelopes
ms.openlocfilehash: 7af4888a77dc96145082f1378713f020b16f56a0
ms.sourcegitcommit: ff82f3260ff79ed860a7a58f54ff7f0594851e6b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2020
ms.locfileid: "68015377"
---
# <a name="fetching-blob-data-using-irowopen-and-isequentialstream"></a>使用 IRow::Open 和 ISequentialStream 提取 BLOB 数据
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  IRow::Open 只支持打开 DBGUID_STREAM 和 DBGUID_NULL 对象类型  。  
  
 以下函数使用 IRow::Open  和 ISequentialStream  提取大型数据。  
  
```  
void InitializeAndExecuteCommand()  
{  
    ULONG iidx;  
    WCHAR* wCmdString=OLESTR("SELECT * FROM MyTable");  
    // Do the initialization, create the session, and set command text.  
    hr = pICommandText->Execute(NULL, IID_IRow, NULL,   
                         &cNumRows,(IUnknown **)&pIRow)))  
    //Get 1 column at a time.  
    for(ULONG i=1; i <= NoOfColumns; i++)  
      GetSequentialColumn(pIRow, iidx);  
    // Do the clean up.  
}  
HRESULT GetSequentialColumn(IRow* pUnkRow, ULONG iCol)  
{  
    HRESULT hr = NOERROR;  
    ULONG cbRead = 0;  
    ULONG cbTotal = 0;  
    ULONG cColumns = 0;  
    ULONG cReads = 0;  
    ISequentialStream* pIStream = NULL;  
    WCHAR* pBuffer[kMaxBuff]; //50 chars read by ISequentialStream::Read()  
    DBCOLUMNINFO* prgInfo;  
    OLECHAR* pColNames;  
    IColumnsInfo* pIColumnsInfo;  
    DBID columnid;  
    DBCOLUMNACCESS column;  
  
    hr = pUnkRow->QueryInterface(IID_IColumnsInfo,   
                            (void**) &pIColumnsInfo);  
    hr = pIColumnsInfo->GetColumnInfo(&cColumns, &prgInfo, &pColNames);  
    // Get Column ID.  
    columnid = (prgInfo + (iCol - 1))->columnid;  
    // Get sequential stream object by calling IRow::Open.  
    hr = pUnkRow->Open(NULL, &columnid, DBGUID_STREAM, 0,   
                    IID_ISequentialStream,(LPUNKNOWN *)&pIStream);  
    ZeroMemory(pBuffer, kMaxBuff * sizeof(WCHAR));  
    // Read 50 chars at a time until no more data.  
    do  
    {  
        hr = pIStream->Read(pBuffer, kMaxBuff, &cbRead);  
        cbTotal = cbTotal + cbRead;  
        // Process the data.  
    } while(cbRead > 0);  
// Do the clean up.  
    return hr;  
}  
```  
  
 大型数据可使用 ISequentialStream  接口进行绑定或检索。 对于绑定列，状态标志指示是否通过设置 DBSTATUS_S_TRUNCATED 来截断数据。  
  
## <a name="see-also"></a>另请参阅  
 [使用 IRow 提取 BLOB 数据](../../oledb/ole-db-rowsets/fetching-a-single-row-with-irow.md)  
  
  
