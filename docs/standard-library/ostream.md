---
title: '&lt;ostream&gt; | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- <ostream>
- ostream/std::<ostream>
- std::<ostream>
dev_langs: C++
helpviewer_keywords: ostream header
ms.assetid: 90c3b6fb-57cd-4ae7-99b8-8512f24a67d2
caps.latest.revision: "20"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: d4805086fb3d63d16f5f9ce6bf3b9e900b436569
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ltostreamgt"></a>&lt;ostream&gt;
定义模板类 [basic_ostream](../standard-library/basic-ostream-class.md)，此模板类可调解 iostreams 的插入。 此标头还定义了若干相关的操控程序。 （此标头通常包含在另一个 iostream 标头中。 很少会直接包含它。）  
  
## <a name="syntax"></a>语法  
  
```  
#include <ostream>  
  
```  
  
### <a name="typedefs"></a>Typedef  
  
|||  
|-|-|  
|[ostream](../standard-library/ostream-typedefs.md#ostream)|通过专用于 `char` 的 `basic_ostream` 和专用于 `char` 的 `char_traits` 创建类型。|  
|[wostream](../standard-library/ostream-typedefs.md#wostream)|通过专用于 `wchar_t` 的 `basic_ostream` 和专用于 `wchar_t` 的 `char_traits` 创建类型。|  
  
### <a name="manipulators"></a>操控器  
  
|||  
|-|-|  
|[endl](../standard-library/ostream-functions.md#endl)|终止行并刷新缓冲区。|  
|[ends](../standard-library/ostream-functions.md#ends)|终止字符串。|  
|[flush](../standard-library/ostream-functions.md#flush)|刷新缓冲区。|  
|[swap](../standard-library/ostream-functions.md#swap)|将 `basic_ostream` 对象参数左侧的值与 `basic_ostream` 对象参数右侧的值进行交换。|  
  
### <a name="operators"></a>运算符  
  
|||  
|-|-|  
|[operator<<](../standard-library/ostream-operators.md#op_lt_lt)|将各种类型写入流。|  
  
### <a name="classes"></a>类  
  
|||  
|-|-|  
|[basic_ostream](../standard-library/basic-ostream-class.md)|模板类描述控制元素和编码对象插入到流缓存区中的对象。|  
  
## <a name="see-also"></a>请参阅  
 [头文件引用](../standard-library/cpp-standard-library-header-files.md)   
 [C++ 标准库中的线程安全性](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [iostream 编程](../standard-library/iostream-programming.md)   
 [iostreams 约定](../standard-library/iostreams-conventions.md)



