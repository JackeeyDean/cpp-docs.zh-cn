---
title: '&lt;stdexcept&gt; |Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: <stdexcept>
dev_langs: C++
helpviewer_keywords: stdexcept header
ms.assetid: 495c10b1-1e60-4514-9f8f-7fda11a2f522
caps.latest.revision: "19"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: b67e1bdd9377c81965dd212836e0f224ff618788
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ltstdexceptgt"></a>&lt;stdexcept&gt;
定义用于报告异常的多个标准类。 这些类构成派生自 [exception](../standard-library/exception-class.md) 类的所有派生层次结构，并包括两种常规类型的异常：逻辑错误和运行时错误。 逻辑错误因程序员错误而引起。 它们派生自基类 logic_error，并且包括：  
  
-   `domain_error`  
  
-   `invalid_argument`  
  
-   `length_error`  
  
-   `out_of_range`  
  
 出现运行时错误是因库函数或运行时系统出错引起。 它们派生自基类 runtime_error，并且包括：  
  
-   `overflow_error`  
  
-   `range_error`  
  
-   `underflow_error`  
  
### <a name="classes"></a>类  
  
|||  
|-|-|  
|[domain_error 类](../standard-library/domain-error-class.md)|此类用作引发报告域错误的所有异常的基类。|  
|[invalid_argument 类](../standard-library/invalid-argument-class.md)|此类用作引发报告无效自变量的所有异常的基类。|  
|[length_error 类](../standard-library/length-error-class.md)|此类用作引发报告尝试生成对象太长而难以指定的所有异常的基类。|  
|[logic_error 类](../standard-library/logic-error-class.md)|此类用作引发报告执行程序前大概可检测的错误（例如，违反逻辑前提条件）的所有异常的基类。|  
|[out_of_range 类](../standard-library/out-of-range-class.md)|此类用作引发报告无效自变量的所有异常的基类。|  
|[overflow_error 类](../standard-library/overflow-error-class.md)|此类用作引发报告算数溢出的所有异常的基类。|  
|[range_error 类](../standard-library/range-error-class.md)|此类用作引发报告范围错误的所有异常的基类。|  
|[runtime_error 类](../standard-library/runtime-error-class.md)|此类用作引发报告仅在执行程序时大概可检测的错误的所有异常的基类。|  
|[underflow_error 类](../standard-library/underflow-error-class.md)|此类用作引发报告算数下溢的所有异常的基类。|  
  
## <a name="see-also"></a>请参阅  
 [头文件引用](../standard-library/cpp-standard-library-header-files.md)   
 [C++ 标准库中的线程安全](../standard-library/thread-safety-in-the-cpp-standard-library.md)

