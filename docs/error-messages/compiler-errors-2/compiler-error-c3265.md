---
title: "编译器错误 C3265 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3265
dev_langs: C++
helpviewer_keywords: C3265
ms.assetid: 10ab3e17-4a9f-4120-bab5-21473869b70f
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 39a80944a7ebb73a1339e140bf68c91fe17c0951
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3265"></a>编译器错误 C3265
不能声明托管托管中构造非托管的非托管构造  
  
在非托管上下文中，不能包含托管的对象。  
  
下面的示例重新产生 C3265:  
  
```  
// C3265_2.cpp  
// compile with: /clr /LD  
#include <vcclr.h>  
  
ref class A { };  
  
class B  
// try the following line instead  
// ref class B   
{  
   A ^a;   // C3265  
   // or embed the managed handle using gcroot  
   // try the following line instead  
   // gcroot<A^> a;  
};  
```  
