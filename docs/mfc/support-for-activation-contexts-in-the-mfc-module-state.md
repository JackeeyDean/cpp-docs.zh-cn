---
title: "对 MFC 模块状态中的激活上下文的支持 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- activation contexts [MFC]
- activation contexts [MFC], MFC support
ms.assetid: 1e49eea9-3620-46dd-bc5f-d664749567c7
caps.latest.revision: "14"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 41aa0987a6fad48e57544ebbdd708d60c000382e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="support-for-activation-contexts-in-the-mfc-module-state"></a>针对 MFC 模块状态中的激活上下文的支持
MFC 使用用户模块提供的清单资源创建激活上下文。 有关如何创建激活上下文的详细信息，请参阅下列主题：  
  
-   [激活上下文](http://msdn.microsoft.com/library/aa374153)  
  
-   [应用程序清单](http://msdn.microsoft.com/library/aa374191)  
  
-   [程序集清单](http://msdn.microsoft.com/library/aa374219)  
  
## <a name="remarks"></a>备注  
 在读取这些 Windows SDK 主题，请注意，MFC 激活上下文机制类似的 Windows SDK 激活上下文，只不过 MFC 不使用 Windows SDK 激活上下文 API。  
  
 激活上下文在 MFC 应用程序、 用户 Dll 和 MFC 扩展 Dll 中工作，通过以下方式：  
  
-   MFC 应用程序为其清单资源使用资源 ID 1。 在这种情况下，MFC 不会创建其自己的激活上下文，但将使用默认应用程序上下文。  
  
-   MFC 用户 DLL 为其清单资源使用资源 ID 2。 此时，MFC 将为每用户 DLL 创建激活上下文，以便其他用户 DLL 可使用同一库（例如，公共控件库）的不同版本。  
  
-   MFC 扩展 DLL 依赖其承载应用程序或用户 DLL 建立其激活上下文。  
  
 尽管可以使用上述过程中在修改的激活上下文状态[使用激活上下文 API](http://msdn.microsoft.com/library/aa376620)，使用 MFC 激活上下文机制将非常有用，在基于 DLL 的插件体系结构的开发时未被轻松 （或不可能） 来手动切换激活状态之前和之后外部的即插即用的外接程序的单个调用。  
  
 在中创建的激活上下文[AfxWinInit](../mfc/reference/application-information-and-management.md#afxwininit)。 它将在 `AFX_MODULE_STATE` 析构函数中销毁。 激活上下文句柄保留在 `AFX_MODULE_STATE` 中。 (`AFX_MODULE_STATE`中所述[AfxGetStaticModuleState](reference/extension-dll-macros.md#afxgetstaticmodulestate)。)  
  
 [AFX_MANAGE_STATE](reference/extension-dll-macros.md#afx_manage_state)宏激活和停用的激活上下文。 将为静态 MFC 库以及 MFC DLL 启用 `AFX_MANAGE_STATE`，以使 MFC 代码在用户 DLL 选择的正确激活上下文中执行。  
  
## <a name="see-also"></a>请参阅  
 [激活上下文](http://msdn.microsoft.com/library/aa374153)   
 [应用程序清单](http://msdn.microsoft.com/library/aa374191)   
 [程序集清单](http://msdn.microsoft.com/library/aa374219)   
 [AfxWinInit](../mfc/reference/application-information-and-management.md#afxwininit)   
 [AfxGetStaticModuleState](reference/extension-dll-macros.md#afxgetstaticmodulestate)   
 [AFX_MANAGE_STATE](reference/extension-dll-macros.md#afx_manage_state)

