---
title: "预定义规则 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- rules, predefined
- NMAKE program, predefined rules
- predefined rules in NMAKE
ms.assetid: 638cdc3f-4aba-4b4f-96e3-ad65b0364f12
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 3be1c8eea7b11f60e9ce9a7cbf5ebc0c2b99b698
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="predefined-rules"></a>预定义的规则
预定义的推理规则使用 NMAKE 提供命令和选项宏。  
  
|规则|命令|默认<br /><br /> action|Batch<br /><br /> 规则|在上运行的平台 nmake|  
|----------|-------------|------------------------|--------------------|----------------------------|  
|。 asm.exe|$(AS) $(AFLAGS) $<|ml $<|否|x86|  
|。 asm.obj|$(AS) $(AFLAGS) /c $<|ml /c $<|是|x86|  
|。 asm.exe|$(AS) $(AFLAGS) $<|ml64 $<|否|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
|。 asm.obj|$(AS) $(AFLAGS) /c $<|ml64 /c $<|是|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
|。 c.exe|$(CC) $(CFLAGS) $<|cl $<|no|全部|  
|。 c.obj|$(CC) $(CFLAGS) /c $<|cl /c $<|是|全部|  
|。 cc.exe|$(CC) $(CFLAGS) $<|cl $<|no|全部|  
|。 cc.obj|$(CC) $(CFLAGS) /c $<|cl /c $<|是|全部|  
|。 cpp.exe|$(CPP) $(CPPFLAGS) $<|cl $<|no|全部|  
|。 cpp.obj|$(CPP) $(CPPFLAGS) /c $<|cl /c $<|是|全部|  
|。 cxx.exe|$(CXX) $(CXXFLAGS) $<|cl $<|no|全部|  
|。 cxx.obj|$(CXX) $(CXXFLAGS) /c $<|cl /c $<|是|全部|  
|。 rc.res|$(RC) $(RFLAGS) /r $<|rc /r $<|否|全部|  
  
## <a name="see-also"></a>请参阅  
 [推理规则](../build/inference-rules.md)