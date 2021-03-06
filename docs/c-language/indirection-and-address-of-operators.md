---
title: "间接寻址和 Address-of 运算符 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- address-of operator (&)
- '* operator'
- operators [C++], address-of
- ampersand operator (&)
- '* operator, indirection operator'
- addresses [C++], indirection
- addresses [C++]
- indirection operator
- '& operator, address-of operator'
- null pointers [C++]
- '* operator, address-of operator'
- operators [C++], indirection
ms.assetid: 10d62b00-12ba-4ea9-a2d5-09ac29ca2232
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 715221da8ea960f19e9c4ab0e386afc61c3439fc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="indirection-and-address-of-operators"></a>间接寻址和 Address-of 运算符
间接寻址运算符 (\*) 通过指针间接访问一个值。 操作数必须是一个指针值。 操作的结果是操作数所寻址的值；即其操作数指向的地址处的值。 结果的类型是操作数寻址的类型。  
  
 如果操作数指向函数，则结果是函数指示符。 如果它指向存储位置，则结果是指定存储位置的左值。  
  
 如果该指针的值无效，则结果是未定义的。 以下列表包含使指针值无效的一些最常见条件。  
  
-   该指针为 null 指针。  
  
-   该指针指定引用时不可见的本地项的地址。  
  
-   该指针指定未针对所指向的对象类型正确对齐的地址。  
  
-   该指针指定执行程序未使用的地址。  
  
 Address-of 运算符 (&) 提供其操作数的地址。 Address-of 运算符的操作数可以是函数指示符，也可以是指定不是位域且不使用 register 存储类说明符声明的对象的左值。  
  
 地址操作的结果是一个指向操作数的指针。 该指针寻址的类型是操作数的类型。  
  
 address-of 运算符仅适用于具有基本、结构或在文件范围级别声明的联合类型的变量，或仅适用于下标数组引用。 在这些表达式中，可在地址表达式中添加或提取不包括 address-of 运算符的常数表达式。  
  
## <a name="examples"></a>示例  
 下面的示例使用这些声明：  
  
```  
int *pa, x;  
int a[20];  
double d;  
```  
  
 此语句使用 address-of 运算符：  
  
```  
pa = &a[5];  
```  
  
 Address-of 运算符 (&) 采用数组 `a` 的第六个元素的地址。 结果存储在指针变量 `pa` 中。  
  
```  
x = *pa;  
```  
  
 间接寻址运算符 (\*) 在此示例中用于访问存储在 `pa` 中的地址的 `int` 值。 将此值分配给整数变量 `x`。  
  
```  
if( x == *&x )  
    printf( "True\n" );  
```  
  
 此示例输出单词 `True`，表明对 `x` 的地址应用间接运算符的结果与 `x` 相同。  
  
```  
int roundup( void );     /* Function declaration */  
  
int  *proundup  = roundup;  
int  *pround  = &roundup;  
```  
  
 一旦声明函数 `roundup`，将声明并初始化指向 `roundup` 的两个指针。 第一个指针为 `proundup`，它仅通过函数名称进行初始化；第二个指针为 `pround`，它在初始化中使用 address-of 运算符。 初始化是等效的。  
  
## <a name="see-also"></a>请参阅  
 [间接寻址运算符：*](../cpp/indirection-operator-star.md)   
 [Address-of 运算符：&](../cpp/address-of-operator-amp.md)