---
title: "错误 C1202 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C1202
dev_langs: C++
helpviewer_keywords: C1202
ms.assetid: c859adb8-17a7-4fa1-a1f3-5820b7bf3849
caps.latest.revision: "11"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 38613d819dab182b6ea0b5922ed087c17b6992c5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="fatal-error-c1202"></a>错误 C1202
递归类型或函数依赖项上下文太复杂  
  
 模板定义为递归，或者超出复杂性限制。  
  
## <a name="example"></a>示例  
 下面的示例生成 C1202。  
  
```  
// C1202.cpp  
// processor: x86 IPF  
template<int n>   
class Factorial : public Factorial<n-1>  {   // C1202  
public:  
   operator int () {   
      return Factorial <n-1>::operator int () * n;   
   }  
};  
Factorial<7> facSeven;  
```  
  
## <a name="example"></a>示例  
 可能的解决方法。  
  
```  
// C1202b.cpp  
// compile with: /c  
template<int n>   
class Factorial : public Factorial<n-1> {  
public:  
   operator int () {   
      return Factorial <n-1>::operator int () * n;   
   }  
};  
  
template <>  
class Factorial<0> {  
public:  
   operator int () {   
      return 1;   
   }  
};  
  
Factorial<7> facSeven;  
```