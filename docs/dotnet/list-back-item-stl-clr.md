---
title: "list::back_item (STL/CLR) |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::list::back_item
dev_langs: C++
helpviewer_keywords: back_item member [STL/CLR]
ms.assetid: 63dcdd21-61f7-4e0f-88a7-c9c8f8a2c50a
caps.latest.revision: "16"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 5e41b042843b3d2d302e517e9281a1bb28e9afc7
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="listbackitem-stlclr"></a>list::back_item (STL/CLR)
访问最后一个元素。  
  
## <a name="syntax"></a>语法  
  
```  
property value_type back_item;  
```  
  
## <a name="remarks"></a>备注  
 属性访问受控序列，必须为非空的最后一个元素。 你可以使用它来读取或写入的最后一个元素，当你知道它存在。  
  
## <a name="example"></a>示例  
  
```  
// cliext_list_back_item.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect last item   
    System::Console::WriteLine("back_item = {0}", c1.back_item);   
  
// alter last item and reinspect   
    c1.back_item = L'x';   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
back_item = c  
 a b x  
```  
  
## <a name="requirements"></a>惠?  
 **标头：** \<cliext/列表 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>请参阅  
 [列表 (STL/CLR)](../dotnet/list-stl-clr.md)   
 [list:: back (STL/CLR)](../dotnet/list-back-stl-clr.md)   
 [list:: front (STL/CLR)](../dotnet/list-front-stl-clr.md)   
 [list::front_item (STL/CLR)](../dotnet/list-front-item-stl-clr.md)