---
title: "Crowset:: Crowset |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CRowset<TAccessor>::CRowset
- CRowset.CRowset
- ATL::CRowset::CRowset
- ATL::CRowset<TAccessor>::CRowset
- ATL.CRowset.CRowset
- CRowset
- CRowset<TAccessor>.CRowset
- CRowset::CRowset
- ATL.CRowset<TAccessor>.CRowset
dev_langs: C++
helpviewer_keywords: CRowset class, constructor
ms.assetid: 1c6f72e2-f4f4-48dc-957e-038ae8914ba7
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: bd028b432ec2a59c775509dbd3821292330d9ea1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="crowsetcrowset"></a>CRowset::CRowset
创建一个新`CRowset`对象并 （可选） 将其与关联[IRowset](https://msdn.microsoft.com/en-us/library/ms720986.aspx)作为参数提供的接口。  
  
## <a name="syntax"></a>语法  
  
```  
  
      CRowset( );   
CRowset(  
   IRowset* pRowset   
);  
```  
  
#### <a name="parameters"></a>参数  
 `pRowset`  
 [in] 指向将与此类关联的 `IRowset` 接口的指针。  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [CRowset 类](../../data/oledb/crowset-class.md)