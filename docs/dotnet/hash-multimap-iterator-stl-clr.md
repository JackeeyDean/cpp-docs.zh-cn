---
title: "hash_multimap:: iterator (STL/CLR) |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_multimap::iterator
dev_langs: C++
helpviewer_keywords: iterator member [STL/CLR]
ms.assetid: 3395078b-10fd-4c3a-827f-274ba29372d3
caps.latest.revision: "15"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 40c12c68a2344072cc1ec212ff0fba37ee39802d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="hashmultimapiterator-stlclr"></a>hash_multimap::iterator (STL/CLR)
受控序列的迭代器的类型。  
  
## <a name="syntax"></a>语法  
  
```  
typedef T1 iterator;  
```  
  
## <a name="remarks"></a>备注  
 此类型描述未指定类型的对象`T1`，可用作受控序列的双向迭代器。  
  
## <a name="example"></a>示例  
  
```  
// cliext_hash_multimap_iterator.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
    c1.insert(Myhash_multimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    Myhash_multimap::iterator it = c1.begin();   
    for (; it != c1.end(); ++it)   
        System::Console::Write(" [{0} {1}]", it->first, it->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
[a 1] [b 2] [c 3]  
```  
  
## <a name="requirements"></a>惠?  
 **标头：** \<cliext/hash_map >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>请参阅  
 [hash_multimap (STL/CLR)](../dotnet/hash-multimap-stl-clr.md)   
 [hash_multimap::const_iterator (STL/CLR)](../dotnet/hash-multimap-const-iterator-stl-clr.md)