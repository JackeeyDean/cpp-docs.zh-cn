---
title: "编译器警告 （等级 4） C4458 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4458
dev_langs: C++
helpviewer_keywords: C4458
ms.assetid: 7bdaa1b1-0caf-4d68-98c4-6bdd441c23fb
caps.latest.revision: "0"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 5dc5e3e49a8581fda9ecf83df2a96056bec38d7b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-4-c4458"></a>编译器警告 （等级 4） C4458
  
> 声明*标识符*隐藏类成员
  
声明*标识符*在本地作用域中隐藏具有相同名称的声明*标识符*类范围内。 此警告，告知你引用到*标识符*此作用域中解析为本地声明的版本中，不是类成员版本，可能会也可能不是你的意图。 若要解决此问题，我们建议你提供类成员名称不会发生冲突的本地变量名称。  
    
## <a name="example"></a>示例
  
下面的示例生成 C4458，因为参数`x`和本地变量`y`中`member_fn`类中具有相同名称的数据成员。 若要解决此问题，请使用不同的参数和局部变量名称。  
  
```cpp  
// C4458_hide.cpp
// compile with: cl /W4 /c C4458_hide.cpp

struct S {
    int x;
    float y;
    void member_fn(long x) {   // C4458
        double y;  // C4458
        y = x;  
        // To fix this issue, change the parameter name x
        // and local name y to something that does not 
        // conflict with the data member names.
    }
} s;
```  
