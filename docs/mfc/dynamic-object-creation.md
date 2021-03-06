---
title: "动态对象创建 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- object creation [MFC], dynamically at run time
- CObject class [MFC], dynamic object creation
- objects [MFC], creating dynamically at run time
- dynamic object creation [MFC]
ms.assetid: 3e0f51cb-3e24-4231-817f-1c0ce9f2d5df
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 755cbf614966ad6faedbe8db9bbf11ac88c63328
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="dynamic-object-creation"></a>动态对象创建
本文说明了如何在运行时动态地创建对象。 过程使用运行时类信息，如本文所述[访问运行时类信息](../mfc/accessing-run-time-class-information.md)。  
  
#### <a name="to-dynamically-create-an-object-given-its-run-time-class"></a>在给定运行时类的情况下动态创建对象  
  
1.  使用以下代码，借助 `CreateObject` 的 `CRuntimeClass` 函数动态地创建一个对象。 请注意，在失败时，`CreateObject`返回**NULL**而不是引发异常：  
  
     [!code-cpp[NVC_MFCCObjectSample#6](../mfc/codesnippet/cpp/dynamic-object-creation_1.cpp)]  
  
## <a name="see-also"></a>请参阅  
 [使用 CObject](../mfc/using-cobject.md)

