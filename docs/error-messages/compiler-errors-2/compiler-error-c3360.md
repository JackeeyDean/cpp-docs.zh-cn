---
title: "编译器错误 C3360 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3360
dev_langs: C++
helpviewer_keywords: C3360
ms.assetid: 6acf983a-dbb6-422b-b045-a34bb4ba6761
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 7500ee2dd9820d1a3f87d7a8cf59203a113151ec
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3360"></a>编译器错误 C3360
“字符串”：无法创建名称  
  
 传递给 [uuid](../../windows/uuid-cpp-attributes.md) 特性的值无效。  
  
 以下示例生成 C3360：  
  
```  
// C3360.cpp  
[ uuid("1") ]  
// try this line instead  
// [ uuid("12341234-1234-1234-1234-123412341234") ]  
struct A   // C3360  
{  
};  
  
int main()  
{  
}  
```