---
title: "C++ 标准库中的函数对象 | Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- functors
- C++ Standard Library, functors
- C++ Standard Library, function objects
- function objects
ms.assetid: 85f8a735-2c7b-4f10-9c4d-95c666ec4192
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 2ba5024590a0682f8d65c7d21ca2cb15d2f481b7
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="function-objects-in-the-c-standard-library"></a>C++ 标准库中的函数对象
*函数对象*（也称 *函子*）是实现 operator() 的任何类型。 此运算符被称为 *调用运算符* （有时称为 *应用程序运算符*）。 C++ 标准库主要使用函数对象作为容器和算法内的排序条件。  
  
 相对于直接函数调用，函数对象有两个优势。 第一个是函数对象可包含状态。 第二个是函数对象是一个类型，因此可用作模板参数。  
  
## <a name="creating-a-function-object"></a>创建函数对象  
 若要创建函数对象，请创建一个类型并实现 operator()，例如：  
  
```
class Functor  
{  
public:  
    int operator()(int a, int b)  
    {  
        return a < b;  
    }  
};  
```

 `main` 函数的最后一行显示了函数对象的调用方式。 此调用看起来像是对函数的调用，但实际上它调用的是函子类型的 operator()。 调用函数对象和函数之间的相似性在于生成术语函数对象的方式。  
  
## <a name="function-objects-and-containers"></a>函数对象和容器  
 C++ 标准库包含 [\<functional>](../standard-library/functional.md) 头文件中的多个函数对象。 这些函数对象的一个用途是用作容器的排序条件。 例如， `set` 容器声明如下：  
  
```  
template <class Key,  
    class Traits=less<Key>,  
    class Allocator=allocator<Key>>  
class set  
```  
  
 第二个模板函数是函数对象 `less`。 如果传递来的第一个参数小于所传递的第二个参数，则此函数对象返回 `true` 。 因为某些容器对其元素进行排序，所以容器需要一种方法来比较两个元素，而通过使用函数对象实现了这一点。 你可以创建函数对象并在容器的模板列表中指定它，从而定义你自己的排序条件。  
  
## <a name="function-objects-and-algorithms"></a>函数对象和算法  
 函数对象的另一个用法是在算法中。 例如， `remove_if` 算法声明如下：  
  
```  
template <class ForwardIterator, class Predicate>  
ForwardIterator remove_if(
    ForwardIterator first,  
    ForwardIterator last,  
    Predicate pred);
```  
  
 `remove_if` 的最后一个参数是返回布尔值（一个 *谓词*）的函数对象。 如果函数对象的结果是 `true`，则从迭代器 `first` 和 `last` 正在访问的容器中删除元素。 你可以使用在 `pred` 参数的 [\<functional>](../standard-library/functional.md) 标头中声明的任何函数对象，也可以自行创建。  
  
## <a name="see-also"></a>请参阅  
 [C++ 标准库参考](../standard-library/cpp-standard-library-reference.md)

