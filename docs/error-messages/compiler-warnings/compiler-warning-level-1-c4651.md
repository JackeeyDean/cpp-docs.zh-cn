---
title: "编译器警告 （等级 1） C4651 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4651
dev_langs: C++
helpviewer_keywords: C4651
ms.assetid: f1ea82aa-4dc1-4972-b55a-57fdb962f0dd
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: dce099d657341ebc957c95ab0cd14f508f9e36ee
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4651"></a>编译器警告（等级 1）C4651
指定有关预编译标头而不是当前的编译的定义  
  
 在生成预编译标头，但不是在此编译中指定的定义。  
  
 定义将实际上内部预编译标头，而不是在代码的其余部分。  
  
 如果使用 /DSYMBOL 生成预编译标头时，编译器将生成此警告，如果 /Yu 编译不具有 /DSYMBOL。  将 /DSYMBOL 添加到 /Yu 命令行可解决此警告。