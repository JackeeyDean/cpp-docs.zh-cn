---
title: "创建对话框类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- dialog boxes [MFC], creating
- MFC dialog boxes [MFC], creating
- files [MFC], creating
- dialog classes [MFC], Add Class Wizard
- dialog classes [MFC], creating
ms.assetid: d5321741-da41-47a8-bb1c-6a0e8b28c4c1
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: f2d8d62dc21aacb29f1133596c7f04251e88f1b5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="creating-your-dialog-class"></a>创建自己的对话框类
对于每个程序中的对话框，创建一个新的对话框类，用于对话框资源。  
  
 [添加类](../ide/adding-a-class-visual-cpp.md)说明如何创建一个新的对话框类。 当使用添加类向导创建对话框类时，它将写入以下各项。H 和。您指定的 CPP 文件：  
  
 在。H 文件：  
  
-   对话框类的类声明。 类派生自[CDialog](../mfc/reference/cdialog-class.md)。  
  
 在。CPP 文件：  
  
-   消息映射的类。  
  
-   对话框中的标准构造函数。  
  
-   重写[DoDataExchange](../mfc/reference/cwnd-class.md#dodataexchange)成员函数。 编辑此函数。 它用于对话框数据交换和验证功能，更高版本中所述[对话框数据交换和验证](../mfc/dialog-data-exchange-and-validation.md)。  
  
## <a name="see-also"></a>请参阅  
 [使用代码向导创建对话框类](../mfc/creating-a-dialog-class-with-code-wizards.md)   
 [对话框的生命周期](../mfc/life-cycle-of-a-dialog-box.md)

