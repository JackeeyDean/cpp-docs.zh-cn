---
title: "is_move_constructible 类 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: type_traits/std::is_move_constructible
dev_langs: C++
helpviewer_keywords: is_move_constructible
ms.assetid: becdf076-7419-488d-a335-78adf2478b9b
caps.latest.revision: "12"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 0c0ca88d938bca629dff15718d8057bd91b96886
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ismoveconstructible-class"></a>is_move_constructible 类
测试类型是否具有移动构造函数。  
  
## <a name="syntax"></a>语法  
  
```
template <class T>  
struct is_move_constructible;
```  
  
#### <a name="parameters"></a>参数  
 T  
 要计算的类型  
  
## <a name="remarks"></a>备注  
 如果类型 `T` 可通过使用移动操作构造，则类型谓词的计算结果为 true。 此谓词等效于 `is_constructible<T, T&&>`。  
  
## <a name="requirements"></a>惠?  
 **标头：**\<type_traits>  
  
 **命名空间：** std  
  
## <a name="see-also"></a>请参阅  
 [<type_traits>](../standard-library/type-traits.md)



