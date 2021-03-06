---
title: "CAccessorBase 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CAccessorBase
dev_langs: C++
helpviewer_keywords: CAccessorBase class
ms.assetid: 389b65be-11ca-4ae0-9290-60c621c4982b
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 9b7c12430c4e7a6872afd46e72e93a29a3189333
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="caccessorbase-class"></a>CAccessorBase 类
从此类派生，OLE DB 模板中的所有访问器。 `CAccessorBase`允许一个行集来管理多个访问器。 它还提供用于参数和输出列的绑定。  
  
## <a name="syntax"></a>语法  
  
```  
// Replace with syntax  
```  
  
## <a name="members"></a>成员  
  
### <a name="methods"></a>方法  
  
|||  
|-|-|  
|[关闭](../../data/oledb/caccessorbase-close.md)|关闭访问器。|  
|[GetHAccessor](../../data/oledb/caccessorbase-gethaccessor.md)|检索访问器句柄。|  
|[GetNumAccessors](../../data/oledb/caccessorbase-getnumaccessors.md)|检索访问器类创建的数目。|  
|[IsAutoAccessor](../../data/oledb/caccessorbase-isautoaccessor.md)|测试指定的访问器是否为自动访问器。|  
|[ReleaseAccessors](../../data/oledb/caccessorbase-releaseaccessors.md)|释放在访问器。|  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [OLE DB 使用者模板](../../data/oledb/ole-db-consumer-templates-cpp.md)   
 [OLE DB 使用者模板参考](../../data/oledb/ole-db-consumer-templates-reference.md)