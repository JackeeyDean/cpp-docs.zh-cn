---
title: "编译器错误 C3888 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3888
dev_langs: C++
helpviewer_keywords: C3888
ms.assetid: 40820812-79c5-4dcd-a19d-b4164d25fc8a
caps.latest.revision: "3"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: e6f0310324afcbde112623959c4dc3b11155fed1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3888"></a>编译器错误 C3888
“name”：C++/CLI 不支持与此 literal 数据成员关联的常量表达式  
  
 使用 *literal* 关键字声明的 [名称](../../windows/literal-cpp-component-extensions.md) 数据成员是使用编译器不支持的值初始化的。 编译器仅支持常量整型、枚举或字符串类型。 **C3888** 错误可能的原因是数据成员是使用字节数组初始化的。  
  
### <a name="to-correct-this-error"></a>更正此错误  
  
1.  检查声明的 literal 数据成员是否是支持的类型。  
  
## <a name="see-also"></a>请参阅  
 [名称](../../windows/literal-cpp-component-extensions.md)