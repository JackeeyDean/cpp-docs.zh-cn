---
title: "快捷键编辑器 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.editors.accelerator.F1
dev_langs: C++
helpviewer_keywords:
- accelerator tables [C++], editing
- tables [Visual Studio], accelerator key
- accelerator keys
- resource editors, Accelerator editor
- keyboard shortcuts [C++], Accelerator editor
- Accelerator editor
ms.assetid: 013c30b6-5d61-4f1c-acef-8bd15bed7060
caps.latest.revision: "12"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: e078dbd3dc8d462ef4bca6e6f1056afb9ce8724c
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="accelerator-editor"></a>快捷键编辑器
快捷键对应表是一个 Windows 资源，包含由快捷键和与之关联的命令标识符组成的列表。 一个程序可以拥有多个快捷键对应表。  
  
 通常情况下，快捷键用作程序命令的键盘快捷键，也可用于菜单或工具栏。 但是，快捷键对应表可用于为没有关联用户界面对象的命令定义组合键。  
  
 可以使用 [类视图](http://msdn.microsoft.com/en-us/8d7430a9-3e33-454c-a9e1-a85e3d2db925) 将快捷键命令与代码挂接。  
  
 使用快捷键编辑器，可以执行下列操作：  
  
-   [设置快捷键属性](../windows/setting-accelerator-properties.md)  
  
-   [将快捷键与菜单项关联](../windows/associating-an-accelerator-key-with-a-menu-item.md)  
  
-   [编辑快捷键对应表](../windows/editing-accelerator-tables.md)  
  
-   [使用预定义快捷键](../windows/predefined-accelerator-keys.md)  
  
    > [!TIP]
    >  使用快捷键编辑器时，可以单击鼠标右键以显示常用命令的快捷菜单。 可用命令取决于指针所指向的内容。  
  
    > [!NOTE]
    >  Windows 不允许创建空快捷键对应表。 如果创建的快捷键对应表中没有任何条目，在保存表时会被自动删除。  
  
 有关将资源添加到托管项目的信息，请参阅[桌面应用中的资源](/dotnet/framework/resources/index)中*.NET Framework 开发指南。* 有关手动将资源文件添加到托管项目、 访问资源、 显示静态资源和将资源字符串分配给属性的信息，请参阅[对于桌面应用程序创建资源文件](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)。 全球化和本地化的资源在托管应用中的信息，请参阅[Globalizing 和本地化的.NET Framework 应用程序](/dotnet/standard/globalization-localization/index)。  
  
## <a name="requirements"></a>惠?  
 Win32  
  
## <a name="see-also"></a>请参阅  
 [资源编辑器](../windows/resource-editors.md)

