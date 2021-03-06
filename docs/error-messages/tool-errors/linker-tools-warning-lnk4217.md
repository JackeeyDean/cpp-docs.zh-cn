---
title: "链接器工具警告 LNK4217 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: LNK4217
dev_langs: C++
helpviewer_keywords: LNK4217
ms.assetid: 280dc03e-5933-4e8d-bb8c-891fbe788738
caps.latest.revision: "12"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 09c984d7675c73bdf225bae7d3014f81153d20e2
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="linker-tools-warning-lnk4217"></a>链接器工具警告 LNK4217
本地定义的符号 symbol 函数 function 中导入  
  
 [__declspec （dllimport)](../../cpp/dllexport-dllimport.md)即使本地定义该符号指定符号。 删除`__declspec`修饰符来解决此警告。  
  
 `symbol`是在映像中定义的符号名称。 `function`是导入符号的函数。  
  
 使用选项进行编译时，将不会出现此警告[/clr](../../build/reference/clr-common-language-runtime-compilation.md)。  
  
 如果你尝试将两个模块链接在一起，而是应编译第一个模块的导入库的第二个模块时，也会发生 LNK4217。  
  
```  
// LNK4217.cpp  
// compile with: /LD  
#include "windows.h"  
__declspec(dllexport) void func(unsigned short*) {}  
```  
  
 然后，  
  
```  
// LNK4217b.cpp  
// compile with: /c  
#include "windows.h"  
__declspec(dllexport) void func(unsigned short*) {}  
```  
  
 尝试链接这两个模块将导致 LNK4217，编译第二个示例与第一个示例，若要解决的导入库。