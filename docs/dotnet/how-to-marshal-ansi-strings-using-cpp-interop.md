---
title: "如何： 使用 c + + 互操作封送 ANSI 字符串 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: get-started-article
dev_langs: C++
helpviewer_keywords:
- interop [C++], strings
- ANSI [C++], marshaling strings
- marshaling [C++], strings
- C++ Interop, strings
- data marshaling [C++], strings
ms.assetid: 5eda2eb6-5140-40f0-82cf-7ce171fffb45
caps.latest.revision: "16"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 7e70d62fa7a94a7278080c31f6650b31b71ff35b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="how-to-marshal-ansi-strings-using-c-interop"></a>如何：使用 C++ 互操作封送 ANSI 字符串
本主题演示 ANSI 字符串可以是如何使用 c + + 互操作，但.NET Framework 传递<xref:System.String>表示以 Unicode 格式的字符串，因此转换为 ANSI 是一个额外的步骤。 用于与其他字符串类型进行交互，请参阅以下主题：  
  
-   [如何：使用 C++ 互操作封送 Unicode 字符串](../dotnet/how-to-marshal-unicode-strings-using-cpp-interop.md)  
  
-   [如何：使用 C++ 互操作封送 COM 字符串](../dotnet/how-to-marshal-com-strings-using-cpp-interop.md)  
  
 下面的代码示例使用[managed、 unmanaged](../preprocessor/managed-unmanaged.md) #pragma 指令来实现托管和非托管函数中同一文件中，但如果在单独的文件中定义，这些函数互操作方式相同。 因为文件仅包含非托管的函数并不需要与编译[/clr （公共语言运行时编译）](../build/reference/clr-common-language-runtime-compilation.md)，它们可以保留其性能特征。  
  
## <a name="example"></a>示例  
 示例演示如何从托管的非 ANSI 字符串传递到非托管的函数使用<xref:System.Runtime.InteropServices.Marshal.StringToHGlobalAnsi%2A>。 此方法的非托管堆上分配内存，并执行转换后返回的地址。 也就是说，没有固定是必要的 （因为在 GC 堆上的内存不被传递给非托管函数），并从返回 IntPtr<xref:System.Runtime.InteropServices.Marshal.StringToHGlobalAnsi%2A>必须显式释放或会导致内存泄漏。  
  
```  
// MarshalANSI1.cpp  
// compile with: /clr  
#include <iostream>  
#include <stdio.h>  
  
using namespace std;  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
#pragma unmanaged  
  
void NativeTakesAString(const char* p) {  
   printf_s("(native) received '%s'\n", p);  
}  
  
#pragma managed  
  
int main() {  
   String^ s = gcnew String("sample string");  
   IntPtr ip = Marshal::StringToHGlobalAnsi(s);  
   const char* str = static_cast<const char*>(ip.ToPointer());  
  
   Console::WriteLine("(managed) passing string...");  
   NativeTakesAString( str );  
  
   Marshal::FreeHGlobal( ip );  
}  
```  
  
## <a name="example"></a>示例  
 下面的示例演示如何访问由非托管函数调用托管函数中的 ANSI 字符串所需的数据封送处理。 托管的函数，在接收到本机的字符串中，可以直接使用或将其转换为非托管的字符串使用<xref:System.Runtime.InteropServices.Marshal.PtrToStringAnsi%2A>方法，如所示。  
  
```  
// MarshalANSI2.cpp  
// compile with: /clr  
#include <iostream>  
#include <vcclr.h>  
  
using namespace std;  
  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
#pragma managed  
  
void ManagedStringFunc(char* s) {  
   String^ ms = Marshal::PtrToStringAnsi(static_cast<IntPtr>(s));  
   Console::WriteLine("(managed): received '{0}'", ms);  
}  
  
#pragma unmanaged  
  
void NativeProvidesAString() {  
   cout << "(native) calling managed func...\n";  
   ManagedStringFunc("test string");  
}  
  
#pragma managed  
  
int main() {  
   NativeProvidesAString();  
}  
```  
  
## <a name="see-also"></a>请参阅  
 [使用 C++ 互操作（隐式 PInvoke）](../dotnet/using-cpp-interop-implicit-pinvoke.md)