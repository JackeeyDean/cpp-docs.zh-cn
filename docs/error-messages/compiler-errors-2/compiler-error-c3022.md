---
title: "编译器错误 C3022 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3022
dev_langs: C++
helpviewer_keywords: C3022
ms.assetid: 9f1d444c-6c6e-48d9-9346-69128390aa33
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 29630a3bf366a7714f012fc2ecd25880390319c3
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3022"></a>编译器错误 C3022
“clause”：在 OpenMP “directive” 指令上的“value”的计划类型无效  
  
 一个不支持的值传递到子句。  
  
 以下示例生成 C3022：  
  
```  
// C3022.cpp  
// compile with: /openmp /link vcomps.lib  
#include <stdio.h>  
#include "omp.h"  
  
int main() {  
   int i;  
  
   #pragma omp parallel for schedule(10)   // C3022  
   for (i = 0; i < 10; ++i) ;  
  
   #pragma omp parallel for schedule(x)   // C3022  
   for (i = 0; i < 10; ++i) ;  
  
   // OK  
   #pragma omp parallel for schedule(runtime)  
   for (i = 0; i < 10; ++i)  
   ;  
}  
```