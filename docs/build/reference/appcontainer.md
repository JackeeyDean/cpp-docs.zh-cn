---
title: "-APPCONTAINER |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: /APPCONTAINER
dev_langs: C++
helpviewer_keywords:
- APPCONTAINER editbin option
- -APPCONTAINER editbin option
- /APPCONTAINER editbin option
ms.assetid: 0ca4f1ec-c8de-4a37-b3e2-deda7af0bb88
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 19e926cbfd1fc58e04c8370825dd83eacff05dfe
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="appcontainer"></a>/APPCONTAINER
标记必须在应用容器中运行的可执行文件 - 例如， [!INCLUDE[win8_appname_long](../../build/includes/win8_appname_long_md.md)] 或通用 Windows 应用。  
  
```  
  
/APPCONTAINER[:NO]  
```  
  
## <a name="remarks"></a>备注  
 设置了 **/APPCONTAINER** 选项的可执行文件只能在应用容器中运行，应用容器是 Windows 8 中引入的进程隔离环境。 对于 [!INCLUDE[win8_appname_long](../../build/includes/win8_appname_long_md.md)] 和通用 Windows 应用，必须设置此选项。  
  
## <a name="see-also"></a>请参阅  
 [EDITBIN 选项](../../build/reference/editbin-options.md)   
 [什么是通用 Windows 应用？](http://go.microsoft.com/fwlink/p/?LinkID=522074)