---
title: "Cdbpropidset:: Setguid |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CDBPropIDSet.SetGUID
- ATL::CDBPropIDSet::SetGUID
- SetGUID
- ATL.CDBPropIDSet.SetGUID
- CDBPropIDSet::SetGUID
dev_langs: C++
helpviewer_keywords: SetGUID method
ms.assetid: 8dd0f3bf-1490-4d53-9063-322b8d821bbe
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: aa70e704cd8e132404442ef390ea5582155a76e2
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="cdbpropidsetsetguid"></a>CDBPropIDSet::SetGUID
设置中的 GUID 字段**DBPROPIDSET**结构。  
  
## <a name="syntax"></a>语法  
  
```  
  
      void SetGUID(   
   const GUID& guid    
) throw( );  
```  
  
#### <a name="parameters"></a>参数  
 `guid`  
 [in]用于设置 GUID **guidPropertySet**字段[DBPROPIDSET](https://msdn.microsoft.com/en-us/library/ms717981.aspx)结构。  
  
## <a name="remarks"></a>备注  
 可以通过设置此字段[构造函数](../../data/oledb/cdbpropidset-cdbpropidset.md)以及。 如果您对此类使用默认构造函数，则调用此函数。  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [CDBPropIDSet 类](../../data/oledb/cdbpropidset-class.md)