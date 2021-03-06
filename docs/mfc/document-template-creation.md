---
title: "文档模板创建 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- document templates [MFC]
- constructors [MFC], document template
- document templates [MFC], creating
- MFC, document templates
- templates [MFC], document templates
ms.assetid: c87f1821-7cbf-442e-9690-f126ae7fb783
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 04950601a74b1ed3e44b236e1d07dcdff997eca6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="document-template-creation"></a>文档模板创建
在响应中创建新文档时`New`或**打开**命令**文件**菜单中，文档模板还创建新的框架窗口对其进行查看该文档可访问。  
  
 文档模板构造函数指定哪些类型的文档、 windows 和模板将能够创建的视图。 这是由传递给文档模板构造函数的实参来确定的。 下面的代码演示创建[CMultiDocTemplate](../mfc/reference/cmultidoctemplate-class.md)示例应用程序：  
  
 [!code-cpp[NVC_MFCDocView#7](../mfc/codesnippet/cpp/document-template-creation_1.cpp)]  
  
 指向新的指针`CMultiDocTemplate`对象用作的自变量[AddDocTemplate](../mfc/reference/cwinapp-class.md#adddoctemplate)。 自变量`CMultiDocTemplate`构造函数包含文档类型的菜单和快捷键，与关联的资源 ID 和三个使用[RUNTIME_CLASS](../mfc/reference/run-time-object-model-services.md#runtime_class)宏。 `RUNTIME_CLASS`返回[CRuntimeClass](../mfc/reference/cruntimeclass-structure.md)作为其自变量名为的 c + + 类的对象。 这三种`CRuntimeClass`对象传递给文档模板构造函数提供文档创建过程中创建的指定类的新对象所需的信息。 该示例演示如何创建的文档模板创建`CScribDoc`对象与`CScribView`附加的对象。 视图是由标准 MDI 子框架窗口确定框架。  
  
## <a name="see-also"></a>请参阅  
 [文档模板和文档/视图创建过程](../mfc/document-templates-and-the-document-view-creation-process.md)   
 [文档/视图创建](../mfc/document-view-creation.md)   
 [MFC 对象之间的关系](../mfc/relationships-among-mfc-objects.md)   
 [创建新文档、窗口和视图](../mfc/creating-new-documents-windows-and-views.md)

