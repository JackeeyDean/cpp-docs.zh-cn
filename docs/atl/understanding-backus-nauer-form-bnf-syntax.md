---
title: "ATL 注册机构和巴科斯-诺尔窗体 (BNF) 语法 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- BNF notation
- Backus Nauer Form (BNF) syntax
ms.assetid: 994bbef0-9077-4aa8-bdfe-b7e830af9acc
caps.latest.revision: "15"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 01d364313420c0a950f8eba222e3ae020fbd86cf
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="understanding-backus-nauer-form-bnf-syntax"></a>了解巴科斯-诺尔范式 (BNF) 语法
使用 ATL 注册器脚本使用 BNF 语法，使用下表中所示的表示法此主题所述。  
  
|约定/符号|含义|  
|------------------------|-------------|  
|`::=`|等效|  
|`&#124;`|或|  
|`X+`|一个或多个`X`s。|  
|`[X]`|`X` 是可选的。 由表示可选分隔符`[]`。|  
|任何**粗体**文本|字符串文本。|  
|任何*斜体化*文本|如何构造字符串文本。|  
  
 上表中所示，注册器脚本使用字符串文本。 这些值是必须出现在你的脚本的实际文本。 下表描述了在 ATL 注册器脚本中使用的字符串文本。  
  
|字符串文本|操作|  
|--------------------|------------|  
|**ForceRemove**|完全删除的下一个键 （如果存在），然后重新创建它。|  
|**NoRemove**|不会在取消注册过程中删除的下一个键。|  
|**val**|指定`<Key Name>`是实际的命名的值。|  
|**删除**|在注册过程中删除的下一个键。|  
|**秒**|指定下一步的值是一个字符串 (**REG_SZ**)。|  
|**d**|指定下一步的值是**DWORD** (**REG_DWORD**)。|  
|**m**|指定下一步的值是 multistring 上 (**REG_MULTI_SZ**)。|  
|**b**|指定的下一步的值是一个二进制值 (**REG_BINARY**)。|  
  
## <a name="bnf-syntax-examples"></a>BNF 语法示例  
 以下是几个语法示例来帮助你了解表示法和字符串文本在 ATL 注册器脚本中的工作。  
  
### <a name="syntax-example-1"></a>语法示例 1  
  
```  
<registry expression> ::= <Add Key>  
```  
  
 指定`registry expression`等效于`Add Key`。  
  
### <a name="syntax-example-2"></a>语法示例 2  
  
```  
<registry expression> ::= <Add Key> | <Delete Key>  
```  
  
 指定`registry expression`等效`Add Key`或`Delete Key`。  
  
### <a name="syntax-example-3"></a>语法示例 3  
  
```  
<Key Name> ::= '<AlphaNumeric>+'  
```  
  
 指定`Key Name`相当于一个或多个`AlphaNumerics`。  
  
### <a name="syntax-example-4"></a>语法示例 4  
  
```  
<Add Key> ::= [ForceRemove | NoRemove | val]<Key Name>  
```  
  
 指定`Add Key`等效于`Key Name`，且字符串文本， `ForceRemove`， `NoRemove`，和`val`，都是可选的。  
  
### <a name="syntax-example-5"></a>语法示例 5  
  
```  
<AlphaNumeric> ::= any character not NULL, that is, ASCII 0  
```  
  
 指定`AlphaNumeric`等效到任何非 NULL 字符。  
  
### <a name="syntax-example-6"></a>语法示例 6  
  
```  
val 'testmulti' = m 'String 1\0String 2\0'  
```  
  
 指定的键名`testmulti`名值组成`String 1`和`String 2`。  
  
### <a name="syntax-example-7"></a>语法示例 7  
  
```  
val 'testhex' = d '&H55'  
```  
  
 指定的键名`testhex`是**DWORD**值设置为十六进制 55 (十进制 85)。 请注意此格式符合**& H**作为表示法在 Visual Basic 规范中找到。  
  
## <a name="see-also"></a>请参阅  
 [创建注册器脚本](../atl/creating-registrar-scripts.md)

