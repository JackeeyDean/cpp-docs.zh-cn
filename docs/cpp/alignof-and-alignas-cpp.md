---
title: "alignof 和 alignas （c + +） |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
ms.assetid: 1d18aa8a-9621-4fb5-86e5-4cc86d5187f4
caps.latest.revision: "2"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 8a506a3c44c3304e786c41a2eb049939d317778e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="alignof-and-alignas-c"></a>alignof 和 alignas (C++)
`alignas` 类型说明符是用于指定变量和用户定义类型的自定义对齐方式的一种可移植的 C++ 标准方法。 `alignof` 运算符也是一种获取指定类型或变量的对齐方式的标准可移植的方法。  
  
## <a name="example"></a>示例  
 你可以在类（struck 或 union）或者单个成员上使用 `alignas`。 遇到多个 `alignas` 说明符时，编译器将选择最严格的说明符（即具有最大值的说明符）。  
  
```cpp  
// alignas_alignof.cpp
// compile with: cl /EHsc alignas_alignof.cpp
#include <iostream>

struct alignas(16) Bar  
{      
    int i;       // 4 bytes  
    int n;      // 4 bytes  
    alignas(4) char arr[3];  
    short s;          // 2 bytes  
};  

int main()
{  
    std::cout << alignof(Bar) << std::endl; // output: 16  
}  
```  
  
## <a name="see-also"></a>请参阅  
 [对齐方式](../cpp/alignment-cpp-declarations.md)