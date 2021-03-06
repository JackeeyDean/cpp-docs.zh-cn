---
title: "OLE 拖放和数据传输类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.classes.ole
dev_langs: C++
helpviewer_keywords:
- ActiveX classes [MFC]
- OLE drag and drop [MFC], and data transfer classes
- drag and drop [MFC], classes
- data transfer [MFC], OLE
- data transfer classes [MFC]
ms.assetid: c8ab2825-ed69-4b88-8ae6-f368b94726b8
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 0e8c5a54184bcf6450bf39b39a6b90d7865c09d3
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ole-drag-and-drop-and-data-transfer-classes"></a>OLE 拖放和数据传输类
在 OLE 数据传输中使用这些类。 它们允许应用程序通过使用剪贴板或拖到和放置之间传输数据。  
  
 [COleDropSource](../mfc/reference/coledropsource-class.md)  
 控制从开始到完成拖放操作。 此类可确定当拖动操作开始和结束时。 它还显示在拖放操作期间的光标反馈。  
  
 [COleDataSource](../mfc/reference/coledatasource-class.md)  
 应用程序提供的数据传输数据时使用。 `COleDataSource`可能会被视为的面向对象的剪贴板对象。  
  
 [COleDropTarget](../mfc/reference/coledroptarget-class.md)  
 表示拖放操作的目标。 A`COleDropTarget`对象对应于在屏幕上窗口。 它确定是否接受任何数据放到它上面并实现实际放操作。  
  
 [COleDataObject](../mfc/reference/coledataobject-class.md)  
 用作接收者端`COleDataSource`。 `COleDataObject`对象提供对存储的数据访问`COleDataSource`对象。  
  
## <a name="see-also"></a>请参阅  
 [类概述](../mfc/class-library-overview.md)

