---
title: "消息映射宏 (MFC) |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- AFXWIN/DECLARE_MESSAGE_MAP
- AFXWIN/BEGIN_MESSAGE_MAP
- AFXWIN/BEGIN_TEMPLATE_MESSAGE_MAP
- AFXWIN/END_MESSAGE_MAP
- AFXWIN/ON_COMMAND
- AFXWIN/ON_COMMAND_EX
- AFXWIN/ON_CONTROL
- AFXWIN/ON_MESSAGE
- AFXWIN/ON_OLECMD
- AFXWIN/ON_REGISTERED_MESSAGE
- AFXWIN/ON_REGISTERED_THREAD_MESSAGE
- AFXWIN/ON_THREAD_MESSAGE
- AFXWIN/ON_UPDATE_COMMAND_UI
- AFXWIN/ON_COMMAND_RANGE
- AFXWIN/ON_UPDATE_COMMAND_UI_RANGE
- AFXWIN/ON_CONTROL_RANGE
dev_langs: C++
helpviewer_keywords:
- message map macros
- Windows messages [MFC], declaration
- demarcating Windows messages
- message maps [MFC], macros
- message maps [MFC], declaration and demarcation
- message mapping macros
- ranges, message map
- message map ranges
ms.assetid: 531b15ce-32b5-4ca0-a849-bb519616c731
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 7bf56b243118ceb7fdd995fc6970f6c49e0a5499
ms.sourcegitcommit: 54035dce0992ba5dce0323d67f86301f994ff3db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/03/2018
---
# <a name="message-map-macros-mfc"></a>消息映射宏 (MFC)
为了支持消息映射，MFC 提供了以下宏：  
  
### <a name="message-map-declaration-and-demarcation-macros"></a>消息映射声明和分界宏  
  
|||  
|-|-|  
|[DECLARE_MESSAGE_MAP](#declare_message_map)|声明将在类中使用消息映射来将消息映射到函数（必须在类声明中使用）。|  
|[BEGIN_MESSAGE_MAP](#begin_message_map)|开始消息映射的定义（必须在类实现中使用）。|  
|[BEGIN_TEMPLATE_MESSAGE_MAP](#begin_template_interface_map)|开始消息映射上包含单个模板自变量的类类型的定义。 |
|[END_MESSAGE_MAP](#end_message_map)|结束消息映射的定义（必须在类实现中使用）。|  
  
### <a name="message-mapping-macros"></a>消息映射宏  
  
|||  
|-|-|  
|[ON_COMMAND](#on_command)|指示哪个函数将处理指定的命令消息。|  
|[ON_COMMAND_EX](#on_command_ex)|指示哪个函数将处理指定的命令消息。|  
|[ON_CONTROL](#on_control)|指示哪个函数将处理指定的控件通知消息。|  
|[ON_MESSAGE](#on_message)|指示哪个函数将处理用户定义的消息。|  
|[ON_OLECMD](#on_olecmd)|指示哪个函数将处理 DocObject 或其容器中的菜单命令。|  
|[ON_REGISTERED_MESSAGE](#on_registered_message)|指示哪个函数将处理已注册的用户定义消息。|  
|[ON_REGISTERED_THREAD_MESSAGE](#on_registered_thread_message)|指示哪个函数将在您具有 `CWinThread` 类时处理已注册的用户定义消息。|  
|[ON_THREAD_MESSAGE](#on_thread_message)|指示哪个函数将在您具有 `CWinThread` 类时处理用户定义的消息。|  
|[ON_UPDATE_COMMAND_UI](#on_update_command_ui)|指示哪个函数将处理指定的用户界面更新命令消息。|  
  
### <a name="message-map-range-macros"></a>消息映射范围宏  
  
|||  
|-|-|  
|[ON_COMMAND_RANGE](#on_command_range)|指示哪个函数将处理在宏的前两个参数中指定的命令 ID 的范围。|  
|[ON_UPDATE_COMMAND_UI_RANGE](#on_update_command_ui_range)|指示哪个更新处理程序将处理命令中指定的 Id 的前两个 pa 范围] rameters 此宏。|  
|[ON_CONTROL_RANGE](#on_control_range)|指示哪个函数将处理来自在宏的第二个和第三个参数中指定的控件 ID 的范围的通知。 第一个参数是控件通知消息，如**BN_CLICKED**。|  
  
 有关消息映射、 消息映射声明和分界宏和消息映射宏的详细信息，请参阅[消息映射](../../mfc/reference/message-maps-mfc.md)和[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)。 有关消息映射范围的详细信息，请参阅[消息映射范围的处理程序](../../mfc/handlers-for-message-map-ranges.md)。  


## <a name="begin_message_map"></a>BEGIN_MESSAGE_MAP
开始消息映射的定义。  
  
### <a name="syntax"></a>语法  
  
```  
BEGIN_MESSAGE_MAP( theClass, baseClass )  
```  
  
### <a name="parameters"></a>参数  
 `theClass`  
 指定其消息映射这类的名称。  
  
 `baseClass`  
 指定 `theClass` 的基类的名称。  
  
### <a name="remarks"></a>备注  
 在实现 (.cpp) 文件中定义你的类的成员函数，开始使用消息映射`BEGIN_MESSAGE_MAP`宏，然后为每个消息处理程序函数，添加宏条目并完成用消息映射`END_MESSAGE_MAP`宏。  
  
 有关消息映射的详细信息，请参阅[消息映射](message-maps-mfc.md)  
  
### <a name="example"></a>示例  
```cpp  
BEGIN_MESSAGE_MAP(CMainFrame, CMDIFrameWnd)
   ON_WM_CREATE()
END_MESSAGE_MAP()
```
  
### <a name="requirements"></a>惠?  
 **标头:** afxwin.h 

##  <a name="begin_template_message_map"></a>BEGIN_TEMPLATE_MESSAGE_MAP
开始消息映射上包含单个模板自变量的类类型的定义。  
   
### <a name="syntax"></a>语法  
  ```
BEGIN_TEMPLATE_MESSAGE_MAP( theClass, type_name, baseClass )  
```
### <a name="parameters"></a>参数  
 `theClass`  
 指定其消息映射这类的名称。    
 `type_name`  
 为类指定的模板参数的名称。    
 `baseClass`  
 指定 `theClass` 的基类的名称。  
   
### <a name="remarks"></a>备注  
 此宏等同于[BEGIN_MESSAGE_MAP](message-map-macros-mfc.md#begin_message_map)宏; 但是，此宏适用于包含单个模板自变量的类。  
  
 在你的类的方法的实现部分，开始使用消息映射**BEGIN_TEMPLATE_MESSAGE_MAP**宏; 然后为每个消息处理程序方法添加宏条目，就像为标准的消息映射。 与**BEGIN_MESSAGE_MAP**宏，完成与模板消息映射[END_MESSAGE_MAP](message-map-macros-mfc.md#end_message_map)宏。  
  
 有关实现模板类的消息映射的详细信息，请参阅[如何： 为一种模板类创建消息映射](../how-to-create-a-message-map-for-a-template-class.md)。  
   
### <a name="requirements"></a>惠?  
 **标头:** afxwin.h  
 
## <a name="declare_message_map"></a>DECLARE_MESSAGE_MAP
 声明类定义消息映射。 每个`CCmdTarget`-程序中的派生的类必须提供一个消息映射来处理消息。  
  
### <a name="syntax"></a>语法  
  
```    
DECLARE_MESSAGE_MAP( )  
```  
  
### <a name="remarks"></a>备注  
 使用`DECLARE_MESSAGE_MAP`宏在类声明的末尾。 然后，在定义类的成员函数的.cpp 文件，使用`BEGIN_MESSAGE_MAP`宏，为每个消息处理程序函数，宏项和`END_MESSAGE_MAP`宏。  
  
> [!NOTE]
>  如果声明后的任何成员`DECLARE_MESSAGE_MAP`，必须指定新的访问类型 (**公共**， `private`，或`protected`) 为它们。  
  
 有关详细信息消息映射和`DECLARE_MESSAGE_MAP`宏，请参阅[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)。  
  
### <a name="example"></a>示例  
```cpp  
class CMainFrame : public CMDIFrameWnd
{
   DECLARE_MESSAGE_MAP()

   // Remainder of class declaration omitted.
``` 
  
### <a name="requirements"></a>惠?  
 **标头:** afxwin.h  


## <a name="end_message_map"></a>END_MESSAGE_MAP
结束消息映射的定义。  
  
### <a name="syntax"></a>语法  
  
```   
END_MESSAGE_MAP( )  
```  
  
### <a name="remarks"></a>备注  
 有关详细信息消息映射和`END_MESSAGE_MAP`宏，请参阅[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)。  
  
### <a name="requirements"></a>惠?  
 **标头:** afxwin.h  

## <a name="on_command"></a>ON_COMMAND
此宏将命令消息映射到的成员函数。  
  
### <a name="syntax"></a>语法  
  
```  
ON_COMMAND( id, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `id`  
 命令 ID。  
  
 `memberFxn`  
 命令映射到的消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 它指示哪个函数将处理命令消息从一个命令用户界面对象，如菜单项或工具栏按钮。  
  
 当命令目标对象收到 Windows **WM_COMMAND**消息具有指定 ID，`ON_COMMAND`将调用成员函数`memberFxn`处理消息。  
  
 使用`ON_COMMAND`将单个命令映射到的成员函数。 使用[ON_COMMAND_RANGE](#on_command_range)以将各种命令 id 映射到一个成员函数。 只有一个消息映射条目可以与给定的命令 id 匹配。也就是说，不能映射到多个处理程序的命令。 有关详细信息和示例，请参阅[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)。  
  
### <a name="example"></a>示例  
```cpp  
BEGIN_MESSAGE_MAP(CMFCListViewDoc, CDocument)
   ON_COMMAND(ID_MYCOMMAND, &CMFCListViewDoc::OnMycommand)
END_MESSAGE_MAP()
``` 
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  

 ## <a name="on_command_ex"></a>ON_COMMAND_EX
扩展命令处理程序成员函数。  
   
### <a name="syntax"></a>语法  
  ```  
ON_COMMAND_EX(id, memberFxn);  
```
### <a name="parameters"></a>参数  
 `id`  
 命令 ID。  
  
 `memberFxn`  
 命令映射到消息处理程序函数的名称。  
   
### <a name="remarks"></a>备注 
命令消息处理程序以扩展的形式是可用于高级用途。 `ON_COMMAND_EX`宏用于此类消息处理程序，并提供 [ON_COMMAND] (#on_command) 功能的超集。  扩展的命令处理程序成员函数采用一个参数**UINT**包含命令 ID，并返回**BOOL**。 返回值应为真 

此宏将命令消息映射到扩展的命令处理程序成员函数。  
   
### <a name="syntax"></a>语法  
```  
ON_COMMAND_EX(id,  memberFxn);  
```
### <a name="parameters"></a>参数  
 `id`  
 命令 ID。  
  
 `memberFxn`  
 命令映射到的消息处理程序函数的名称。  
   
### <a name="remarks"></a>备注  
 命令消息处理程序以扩展的形式是可用于高级用途。 `ON_COMMAND_EX`宏用于此类消息处理程序中，并且它提供的超集[ON_COMMAND](message-map-macros-mfc.md#on_command)功能。 扩展的命令处理程序成员函数采用一个参数**UINT**包含命令 ID，并返回**BOOL**。 返回值应为 TRUE，以指示已处理该命令;否则路由到其他命令目标对象将继续。  
有关详细信息，请参阅技术说明 [TN006： 消息映射] tm006 消息 maps.md)。  
   
### <a name="requirements"></a>惠?  
 标头文件： afxmsg_.h  
   
### <a name="see-also"></a>请参阅  
 [ON_COMMAND](message-map-macros-mfc.md#on_command)   
 [TN006： 消息映射] tm006 消息 maps.md)

  
## <a name="on_control"></a>ON_CONTROL
指示哪个函数将处理自定义控件通知消息。  
  
### <a name="syntax"></a>语法  
  
```  
ON_CONTROL( wNotifyCode, id, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `wNotifyCode`  
 控件通知代码。  
  
 `id`  
 命令 ID。  
  
 `memberFxn`  
 命令映射到的消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 控件通知消息是那些从控件发送到其父窗口。  
  
 应该有且仅有`ON_CONTROL`消息映射每个控件通知消息，必须映射到消息处理程序函数中的宏语句。  
  
 有关详细信息和示例，请参阅[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)。  
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  
  

## <a name="on_message"></a>ON_MESSAGE  
指示哪个函数将处理用户定义的消息。  
  
### <a name="syntax"></a>语法  
  
```  
ON_MESSAGE( message, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `message`  
 消息 ID。  
  
 `memberFxn`  
 消息映射到消息处理程序函数的名称。  
  
 函数的类型必须是`afx_msg LRESULT (CWnd::*)(WPARAM, LPARAM)`。  
  
### <a name="remarks"></a>备注  
 用户定义的消息是指不是标准的窗口的任何消息`WM_MESSAGE`消息。 如果选择消息 ID，则必须使用的范围内的值`WM_USER`(0x0400) 到 0x7FFF 或`WM_APP`(0x8000) 到 0xBFFF。 有关消息 Id 的详细信息，请参阅[WM_APP](http://msdn.microsoft.com/library/windows/desktop/ms644930)。  
  
 应该有且仅有`ON_MESSAGE`在必须映射到消息处理程序函数的每个用户定义的消息的消息映射宏语句。  
  
> [!NOTE]
>  用户定义的消息，除了`ON_MESSAGE`处理不太常见的 Windows 消息。 有关详细信息，请参阅知识库文章[99848： 信息： 使用 ON_MESSAGE() 宏映射不太常见消息为](http://go.microsoft.com/fwlink/p/?linkid=192022)。  
  
 有关详细信息和示例，请参阅[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)和[用户定义处理程序](user-defined-handlers.md)  
  
### <a name="example"></a>示例  
```cpp  
#define WM_MYMESSAGE (WM_USER + 100)

BEGIN_MESSAGE_MAP(CMyWnd2, CWnd)
   ON_MESSAGE(WM_MYMESSAGE, OnMyMessage)
END_MESSAGE_MAP()

// inside the class declaration
 afx_msg LRESULT OnMyMessage(WPARAM wParam, LPARAM lParam);

 LRESULT CMyWnd2::OnMyMessage(WPARAM wParam, LPARAM lParam)
{
   UNREFERENCED_PARAMETER(wParam);
   UNREFERENCED_PARAMETER(lParam);

   // Handle message here. 

   return 0;
}
```   
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  

## <a name="on_olecmd"></a>ON_OLECMD  
将命令路由通过命令调度接口`IOleCommandTarget`。  
  
### <a name="syntax"></a>语法  
  
```  
ON_OLECMD( pguid, olecmdid, id )  
```  
  
### <a name="parameters"></a>参数  
 `pguid`  
 该命令所属的命令组的标识符。 使用**NULL**标准组。  
  
 *olecmdid*  
 OLE 命令的标识符。  
  
 `id`  
 菜单 ID、 工具栏 ID、 按钮 ID 或其他资源或发出命令的对象的 ID 中。  
  
### <a name="remarks"></a>备注  
 `IOleCommandTarget`允许容器接收源自 DocObject 的用户界面的命令，并允许要发送的相同命令的容器 (例如新建、 打开、 另存为，和在文件菜单中; 上的打印和复制、 粘贴、 撤消，依次类推编辑菜单上) 到 DocObject。  
  
 `IOleCommandTarget`OLE 自动化的比简单得多`IDispatch`。 `IOleCommandTarget`完全依赖于一组标准的命令，它很少具有参数，且涉及无类型信息 （命令自变量也会降低类型安全）。 如果你确实需要调度带参数的命令，使用[COleServerDoc::OnExecOleCmd](coleserverdoc-class.md#onexecolecmd)。  
  
 `IOleCommandTarget`标准菜单命令已由 MFC 实现中的以下宏：  
  
 **ON_OLECMD_CLEARSELECTION （)**  
  
 将调度清除编辑命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_CLEARSELECTION, ID_EDIT_CLEAR)`  
  
 **ON_OLECMD_COPY （)**  
  
 将调度编辑复制命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_COPY, ID_EDIT_COPY)`  
  
 **ON_OLECMD_CUT （)**  
  
 将调度编辑剪切命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_CUT, ID_EDIT_CUT)`  
  
 **ON_OLECMD_NEW （)**  
  
 将调度文件新的命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_NEW, ID_FILE_NEW)`  
  
 **ON_OLECMD_OPEN （)**  
  
 将调度文件打开的命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_OPEN, ID_FILE_OPEN)`  
  
 **ON_OLECMD_PAGESETUP （)**  
  
 将调度文件页安装程序命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_PAGESETUP, ID_FILE_PAGE_SETUP)`  
  
 **ON_OLECMD_PASTE （)**  
  
 将调度编辑粘贴命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_PASTE, ID_EDIT_PASTE)`  
  
 **ON_OLECMD_PASTESPECIAL （)**  
  
 将调度编辑选择性粘贴命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_PASTESPECIAL, ID_EDIT_PASTE_SPECIAL)`  
  
 **ON_OLECMD_PRINT （)**  
  
 将调度文件打印命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_PRINT, ID_FILE_PRINT)`  
  
 **ON_OLECMD_PRINTPREVIEW （)**  
  
 将调度文件打印预览命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_PRINTPREVIEW, ID_FILE_PRINT_PREVIEW)`  
  
 **ON_OLECMD_REDO （)**  
  
 将调度编辑重做命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_REDO, ID_EDIT_REDO)`  
  
 **ON_OLECMD_SAVE （)**  
  
 将调度文件保存命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_SAVE, ID_FILE_SAVE)`  
  
 **ON_OLECMD_SAVE_AS （)**  
  
 将调度文件另存为命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_SAVEAS, ID_FILE_SAVE_AS)`  
  
 **ON_OLECMD_SAVE_COPY_AS （)**  
  
 将调度文件副本另存为命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_SAVECOPYAS, ID_FILE_SAVE_COPY_AS)`  
  
 **ON_OLECMD_SELECTALL （)**  
  
 将调度编辑选择的所有命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_SELECTALL, ID_EDIT_SELECT_ALL)`  
  
 **ON_OLECMD_UNDO （)**  
  
 将调度编辑撤消命令。 作为实现：  
  
 `ON_OLECMD(NULL, OLECMDID_UNDO, ID_EDIT_UNDO)`  
  
### <a name="requirements"></a>惠?  
 **标头：** afxdocob.h  
  
### <a name="see-also"></a>请参阅  
 [COleCmdUI 类](colecmdui-class.md)   
 [COleServerDoc::OnExecOleCmd](coleserverdoc-class.md#onexecolecmd)

## <a name="on_registered_message"></a>ON_REGISTERED_MESSAGE
Windows **RegisterWindowMessage**函数用于定义新的窗口消息来保证是唯一的在整个系统。  
  
### <a name="syntax"></a>语法  
  
```  
ON_REGISTERED_MESSAGE( nMessageVariable, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `nMessageVariable`  
 已注册的窗口消息 ID 变量中。  
  
 `memberFxn`  
 消息映射到消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 此宏指示哪个函数将处理已注册的消息。  
  
 有关详细信息和示例，请参阅[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)。  
  
### <a name="example"></a>示例  
```cpp  
static UINT NEAR WM_FIND = RegisterWindowMessage(_T("COMMDLG_FIND"));


BEGIN_MESSAGE_MAP(CMyWnd3, CWnd)
   ON_REGISTERED_MESSAGE(WM_FIND, OnFind)
END_MESSAGE_MAP()
```  
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  
  
### <a name="see-also"></a>请参阅  
 [RegisterWindowMessage](http://msdn.microsoft.com/library/windows/desktop/ms644947)   
 [用户定义的处理程序](user-defined-handlers.md)

## <a name="on_registered_thread_message"></a>ON_REGISTERED_THREAD_MESSAGE    
指示哪个函数将处理由 Windows RegisterWindowMessage 函数注册消息。  
  
### <a name="syntax"></a>语法  
  
```  
ON_REGISTERED_THREAD_MESSAGE(nMessageVariable, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `nMessageVariable`  
 已注册的窗口消息 ID 变量中。  
  
 `memberFxn`  
 消息映射到 CWinThread 消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 RegisterWindowMessage 用于定义新的窗口消息来保证是唯一的在整个系统。 CWinThread 类后，ON_REGISTERED_THREAD_MESSAGE 必须使用而不是 ON_REGISTERED_MESSAGE。 
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  

## <a name="on_thread_message"></a>ON_THREAD_MESSAGE  
指示哪个函数将处理用户定义的消息。  
  
### <a name="syntax"></a>语法  
  
```  
ON_THREAD_MESSAGE( message, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `message`  
 消息 ID。  
  
 `memberFxn`  
 名称`CWinThread`-消息的消息映射到处理程序函数。  
  
### <a name="remarks"></a>备注  
 `ON_THREAD_MESSAGE`必须使用而不是`ON_MESSAGE`如果你具有`CWinThread`类。 用户定义的消息是指不是标准的窗口的任何消息**WM_MESSAGE**消息。 应该有且仅有`ON_THREAD_MESSAGE`在必须映射到消息处理程序函数的每个用户定义的消息的消息映射宏语句。  
  
### <a name="requirements"></a>惠?  
 **标头：** afxole.h  

## <a name="on_update_command_ui"></a>ON_UPDATE_COMMAND_UI    
此宏指示哪个函数将处理用户界面更新命令消息。  
  
### <a name="syntax"></a>语法  
  
```  
ON_UPDATE_COMMAND_UI( id, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `id`  
 消息 ID。  
  
 `memberFxn`  
 消息映射到消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 应该有且仅有`ON_UPDATE_COMMAND_UI`中必须映射到消息处理程序函数的每个用户界面更新命令你消息映射宏语句。  
  
 有关详细信息和示例，请参阅[消息处理和映射主题](../../mfc/message-handling-and-mapping.md)。  
  
### <a name="requirements"></a>惠?  
 **标头：** afxole.h  
  
### <a name="see-also"></a>请参阅  
 [CCmdUI 类](ccmdui-class.md)

## <a name="on_command_range"></a>ON_COMMAND_RANGE  
使用此宏将一组连续的命令 Id 映射到单个消息处理程序函数。  
  
### <a name="syntax"></a>语法
  
```  
ON_COMMAND_RANGE( id1, id2, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `id1`  
 在连续范围的命令 Id 的开头的命令 ID。  
  
 `id2`  
 在命令 Id 的连续范围末尾的命令 ID。  
  
 `memberFxn`  
 命令映射到消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 Id 范围开头`id1`和结束的`id2`。  
  
 使用`ON_COMMAND_RANGE`以将各种命令 Id 映射到一个成员函数。 使用[ON_COMMAND](#on_command)将单个命令映射到的成员函数。 只有一个消息映射条目可以匹配给定的命令 id。 也就是说，不能映射到多个处理程序的命令。 映射消息范围的详细信息，请参阅[消息映射范围的处理程序](../../mfc/handlers-for-message-map-ranges.md)。  
  
 没有自动支持的消息映射范围，因此必须自行放置宏。  
  
### <a name="example"></a>示例  
```cpp  
// The code fragment below shows how to use ON_COMMAND_RANGE macro 
// to map a contiguous range of command IDs to a single message  
// handler function (i.e. OnRangeCmds() in the sample below). In  
// addition, it also shows how to use CheckMenuRadioItem() to check a  
// selected menu item and makes it a radio item.

BEGIN_MESSAGE_MAP(CChildFrame, CMDIChildWnd)
   ON_COMMAND_RANGE(ID_COMMAND_RANGECMD1, ID_COMMAND_RANGECMD3, &CChildFrame::OnRangeCmds)
END_MESSAGE_MAP()

void CChildFrame::OnRangeCmds(UINT nID)
{
   CMenu* mmenu = AfxGetMainWnd()->GetMenu();
   CMenu* submenu = mmenu->GetSubMenu(5);
   submenu->CheckMenuRadioItem(ID_COMMAND_RANGECMD1, ID_COMMAND_RANGECMD3, 
      nID, MF_BYCOMMAND);
}
```
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  

## <a name="on_update_command_ui_range"></a>ON_UPDATE_COMMAND_UI_RANGE    
将一组连续的命令 Id 映射到单个更新消息处理程序函数。  
  
### <a name="syntax"></a>语法  
  
```  
ON_UPDATE_COMMAND_UI_RANGE( id1, id2, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `id1`  
 在连续范围的命令 Id 的开头的命令 ID。  
  
 `id2`  
 在命令 Id 的连续范围末尾的命令 ID。  
  
 `memberFxn`  
 命令映射到更新消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 更新消息处理程序更新的菜单项和工具栏按钮与命令关联的状态。 Id 范围开头`id1`和结束的`id2`。  
  
 没有自动支持的消息映射范围，因此必须自行放置宏。  
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  

## <a name="on_control_range"></a>ON_CONTROL_RANGE     
使用此宏将连续范围的控件 Id 映射到单个消息处理程序函数为指定的 Windows 通知消息，如**BN_CLICKED**。  
  
### <a name="syntax"></a>语法  
  
```  
ON_CONTROL_RANGE( wNotifyCode, id1, id2, memberFxn )  
```  
  
### <a name="parameters"></a>参数  
 `wNotifyCode`  
 通知代码向其响应你的处理程序。  
  
 `id1`  
 在连续范围的控件 Id 的开头的命令 ID。  
  
 `id2`  
 控件 Id 的连续范围的末尾处的命令 ID。  
  
 `memberFxn`  
 控件映射到消息处理程序函数的名称。  
  
### <a name="remarks"></a>备注  
 Id 范围开头`id1`和结束的`id2`。 指定来自的任何映射的控件的通知将为调用处理程序。  
  
 没有自动支持的消息映射范围，因此必须自行放置宏。  
  
 有关实现控件 Id 的范围的处理程序函数的详细信息，请参阅[消息映射范围的处理程序](../../mfc/handlers-for-message-map-ranges.md)。  
  
### <a name="requirements"></a>惠?  
 **标头：** afxmsg_.h  
  


