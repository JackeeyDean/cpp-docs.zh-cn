---
title: "Verifyinheritancehelper:: Verify 方法 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: implements/Microsoft::WRL::Details::VerifyInheritanceHelper::Verify
dev_langs: C++
helpviewer_keywords: Verify method
ms.assetid: 3360082b-81ad-4191-9ec3-b4372f7207d7
caps.latest.revision: "5"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ffc08fd7cd59d463d5a53ababf3acb6baef9e3ef
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="verifyinheritancehelperverify-method"></a>VerifyInheritanceHelper::Verify 方法
支持 WRL 基础结构，不应在代码中直接使用。  
  
## <a name="syntax"></a>语法  
  
```  
static void Verify();  
```  
  
## <a name="remarks"></a>备注  
 测试当前的模板参数指定的两个接口，并确定是否将一个接口派生自另。  
  
 如果一个接口不从其他派生，则会发出错误。  
  
## <a name="requirements"></a>惠?  
 **标头：** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## <a name="see-also"></a>请参阅  
 [VerifyInheritanceHelper 结构](../windows/verifyinheritancehelper-structure.md)   
 [Microsoft::WRL::Details 命名空间](../windows/microsoft-wrl-details-namespace.md)