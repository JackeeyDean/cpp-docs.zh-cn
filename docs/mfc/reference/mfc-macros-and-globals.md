---
title: "MFC 宏和全局函数 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.mfc.macros
dev_langs: C++
helpviewer_keywords:
- MFC, global functions and variables
- MFC, macros
- global functions, MFC
- macros, MFC
- global functions [MFC]
- global variables, MFC
- Afx naming convention
- macros
ms.assetid: add4e33f-0e62-4d27-be14-896cb8675d22
caps.latest.revision: "18"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: eeb53dea24ccd4d34ef90045e3254915135e70c2
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="mfc-macros-and-globals"></a>MFC 宏和全局函数
Microsoft 基础类库可以分成两个主要部分: （1） 的 MFC 类和 （2） 宏和全局函数。 如果函数或变量不是类的成员，则全局函数或变量。  
  
 MFC 库和活动模板库 (ATL) 共享字符串转换宏。 有关详细信息，请参阅[字符串转换宏](../../atl/reference/string-conversion-macros.md)ATL 文档中。  
  
 MFC 宏和全局函数提供以下类别中的功能。  
  
## <a name="general-mfc"></a>常规 MFC  
  
-   [数据类型](data-types-mfc.md)  
  
-   [MFC 类对象的类型强制转换](type-casting-of-mfc-class-objects.md)  
  
-   [运行时对象模型服务](run-time-object-model-services.md)  
  
-   [诊断服务](diagnostic-services.md)  
  
-   [异常处理](exception-processing.md)  
  
-   [CString 格式设置和消息框显示](cstring-formatting-and-message-box-display.md)  
  
-   [消息映射](message-map-macros-mfc.md)  

-   [委托和接口映射](delegate-and-interface-maps.md)

-   [模块和 DLL](extension-dll-macros.md)
  
-   [应用程序信息和管理](application-information-and-management.md)  
  
-   [标准命令和窗口 Id](standard-command-and-window-ids.md)  
  
-   [集合类帮助器](collection-class-helpers.md)  
  
-   [灰色和抖色位图函数](gray-and-dithered-bitmap-functions.md)  
  
-   [标准对话框数据交换 (DDX) 例程](standard-dialog-data-exchange-routines.md)  
  
-   [标准对话框数据验证 (DDV) 例程](standard-dialog-data-validation-routines.md)  
  
-   [AFX 消息](afx-messages.md)  
  
-   [工具栏控件样式](toolbar-control-styles.md)  
  
-   [CMFCImagePaintArea::IMAGE_EDIT_MODE 枚举](cmfcimagepaintarea-image-edit-mode-enumeration.md)  

  
## <a name="database"></a>数据库  
  
-   [记录字段交换 (RFX) 函数](record-field-exchange-functions.md)和[批量记录字段交换 (bulk RFX) 函数](record-field-exchange-functions.md)MFC ODBC 类  
  
-   [记录字段交换 (DFX) 函数](record-field-exchange-functions.md)MFC DAO 类  
  
-   [CRecordView 和 CDaoRecordView 的对话框数据交换 (DDX) 函数](dialog-data-exchange-functions-for-crecordview-and-cdaorecordview.md)（MFC ODBC 和 DAO 类）  
  
-   [OLE 控件的对话框数据交换 (DDX) 函数](dialog-data-exchange-functions-for-ole-controls.md)  
  
-   [宏和全局函数来帮助进行直接调用开放式数据库连接 (ODBC) API 函数](database-macros-and-globals.md)  
  
-   [DAO 数据库引擎初始化和终止](dao-database-engine-initialization-and-termination.md)  
  
## <a name="internet"></a>Internet  
  
-   [Internet URL 分析全局函数](internet-url-parsing-globals.md)  
  
## <a name="dhtml--dhtml-event-maps"></a>DHTML / DHTML 事件映射  
  
-   [DHTML 对话框数据交换 (DDX) 帮助器宏](ddx-dhtml-helper-macros.md)  
  
-   [DHTML 事件映射](dhtml-event-maps.md)  
  
## <a name="ole"></a>OLE  
  
-   [OLE 初始化](ole-initialization.md)  
  
-   [应用程序控件](application-control.md)  
  
-   [调度映射](dispatch-maps.md)  
  
 此外，MFC 提供了一个名为函数[AfxEnableControlContainer](ole-initialization.md#afxenablecontrolcontainer)启用任何 OLE 容器开发使用 MFC 4.0 以完全支持嵌入 OLE 控件。  
  
## <a name="ole-controls"></a>OLE 控件  
  
-   [变量参数类型常量](variant-parameter-type-constants.md)  
  
-   [类型库访问](type-library-access.md)  
  
-   [属性页](property-pages-mfc.md)  
  
-   [事件映射](event-maps.md)  
  
-   [事件接收器映射](event-sink-maps.md)  
  
-   [连接映射](connection-maps.md)  
  
-   [注册 OLE 控件](registering-ole-controls.md)  
  
-   [类工厂和许可](class-factories-and-licensing.md)  
  
-   [OLE 控件的持久性](persistence-of-ole-controls.md)  
  
 本部分的第一部分简要讨论每个以前的类别，并列出的全局和类别，以及功能的简要说明中的宏。 以下这是全局函数、 全局变量和宏 MFC 库中的说明。  
  
> [!NOTE]
>  许多全局函数以前缀"Afx"开头，但一些，例如，对话框数据交换 (DDX) 函数和许多数据库函数，不遵循此约定。 所有全局变量开头"afx"作为前缀。 宏不会启动与任何特定的前缀，但它们用大写字母编写。  
  
## <a name="see-also"></a>请参阅  
 [类概述](../../mfc/class-library-overview.md)



