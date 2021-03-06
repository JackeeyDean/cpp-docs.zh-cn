---
title: "CMFCPopupMenuBar 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCPopupMenuBar
- AFXPOPUPMENUBAR/CMFCPopupMenuBar
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::AdjustSizeImmediate
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::BuildOrigItems
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::CloseDelayedSubMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::ExportToMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::FindDestintationToolBar
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetCurrentMenuImageSize
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetDefaultMenuId
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetLastCommandIndex
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetOffset
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::ImportFromMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsDropDownListMode
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsPaletteMode
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsRibbonPanel
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsRibbonPanelInRegularMode
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::LoadFromHash
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::RestoreDelayedSubMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::SetButtonStyle
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::SetOffset
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::StartPopupMenuTimer
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::m_bDisableSideBarInXPMode
dev_langs: C++
helpviewer_keywords:
- CMFCPopupMenuBar [MFC], AdjustSizeImmediate
- CMFCPopupMenuBar [MFC], BuildOrigItems
- CMFCPopupMenuBar [MFC], CloseDelayedSubMenu
- CMFCPopupMenuBar [MFC], ExportToMenu
- CMFCPopupMenuBar [MFC], FindDestintationToolBar
- CMFCPopupMenuBar [MFC], GetCurrentMenuImageSize
- CMFCPopupMenuBar [MFC], GetDefaultMenuId
- CMFCPopupMenuBar [MFC], GetLastCommandIndex
- CMFCPopupMenuBar [MFC], GetOffset
- CMFCPopupMenuBar [MFC], ImportFromMenu
- CMFCPopupMenuBar [MFC], IsDropDownListMode
- CMFCPopupMenuBar [MFC], IsPaletteMode
- CMFCPopupMenuBar [MFC], IsRibbonPanel
- CMFCPopupMenuBar [MFC], IsRibbonPanelInRegularMode
- CMFCPopupMenuBar [MFC], LoadFromHash
- CMFCPopupMenuBar [MFC], RestoreDelayedSubMenu
- CMFCPopupMenuBar [MFC], SetButtonStyle
- CMFCPopupMenuBar [MFC], SetOffset
- CMFCPopupMenuBar [MFC], StartPopupMenuTimer
- CMFCPopupMenuBar [MFC], m_bDisableSideBarInXPMode
ms.assetid: 4c93c459-7f70-4240-8c63-280bb811e374
caps.latest.revision: "32"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 002e059fd905930409cb5f2745628f8ac1dea103
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="cmfcpopupmenubar-class"></a>CMFCPopupMenuBar 类
嵌入到弹出菜单的菜单栏。  
  
## <a name="syntax"></a>语法  
  
```  
class CMFCPopupMenuBar : public CMFCToolBar  
```  
  
## <a name="members"></a>成员  
  
### <a name="public-methods"></a>公共方法  
  
|名称|描述|  
|----------|-----------------|  
|[CMFCPopupMenuBar::AdjustSizeImmediate](#adjustsizeimmediate)|立即重新计算一个窗格的布局。 (重写[CPane::AdjustSizeImmediate](../../mfc/reference/cpane-class.md#adjustsizeimmediate)。)|  
|[CMFCPopupMenuBar::BuildOrigItems](#buildorigitems)|从指定的菜单资源加载弹出菜单项。|  
|[CMFCPopupMenuBar::CloseDelayedSubMenu](#closedelayedsubmenu)|关闭延迟的弹出菜单按钮。|  
|[CMFCPopupMenuBar::ExportToMenu](#exporttomenu)|生成中的菜单的弹出菜单按钮。|  
|[CMFCPopupMenuBar::FindDestintationToolBar](#finddestintationtoolbar)|查找指定的点所在的工具栏。|  
|[CMFCPopupMenuBar::GetCurrentMenuImageSize](#getcurrentmenuimagesize)|指示菜单按钮图像的大小。|  
|[CMFCPopupMenuBar::GetDefaultMenuId](#getdefaultmenuid)|返回默认菜单项的标识符。|  
|[CMFCPopupMenuBar::GetLastCommandIndex](#getlastcommandindex)|获取最近调用菜单命令的索引。|  
|[CMFCPopupMenuBar::GetOffset](#getoffset)|获取弹出菜单栏的行偏移量。|  
|[CMFCPopupMenuBar::ImportFromMenu](#importfrommenu)|从指定菜单导入弹出菜单按钮。|  
|[CMFCPopupMenuBar::IsDropDownListMode](#isdropdownlistmode)|指示弹出菜单栏是否在下拉列表列表模式下。|  
|[CMFCPopupMenuBar::IsPaletteMode](#ispalettemode)|指示弹出菜单栏是否在调色板模式下。|  
|[CMFCPopupMenuBar::IsRibbonPanel](#isribbonpanel)|指示这是一个功能区面板 (`FALSE`默认情况下)。|  
|[CMFCPopupMenuBar::IsRibbonPanelInRegularMode](#isribbonpanelinregularmode)|指示这是一个功能区面板常规模式下 (`FALSE`默认情况下)。|  
|[CMFCPopupMenuBar::LoadFromHash](#loadfromhash)|加载已存档的菜单。|  
|[CMFCPopupMenuBar::RestoreDelayedSubMenu](#restoredelayedsubmenu)|还原延迟的菜单按钮用于关闭弹出菜单栏。|  
|[CMFCPopupMenuBar::SetButtonStyle](#setbuttonstyle)|设置给定索引处的工具栏按钮的样式。 (重写[CMFCToolBar::SetButtonStyle](../../mfc/reference/cmfctoolbar-class.md#setbuttonstyle)。)|  
|[CMFCPopupMenuBar::SetOffset](#setoffset)|设置弹出菜单栏的行偏移量。|  
|[CMFCPopupMenuBar::StartPopupMenuTimer](#startpopupmenutimer)|启动指定的延迟的弹出菜单按钮的计时器。|  
  
### <a name="data-members"></a>数据成员  
  
|name|描述|  
|----------|-----------------|  
|[CMFCPopupMenuBar::m_bDisableSideBarInXPMode](#m_bdisablesidebarinxpmode)|指定是否在应用程序具有 Windows XP 的外观时，将会显示灰色侧栏。|  
  
## <a name="remarks"></a>备注  
 `CMFCPopupMenuBar`作为同时创建[CMFCPopupMenu 类](../../mfc/reference/cmfcpopupmenu-class.md)和嵌入其内部。 `CMFCPopupMenuBar`涵盖的整个工作区`CMFCPopupMenu`对象。 它支持键盘和鼠标输入。 它也能进行通信的输入`CMFCPopupMenu`和顶级框架窗口。  
  
## <a name="example"></a>示例  
 下面的示例演示如何初始化`CMFCPopupMenuBar`对象`CMFCPopupMenu`对象。 此代码片段属于 [Draw Client 示例](../../visual-cpp-samples.md)。  
  
 [!code-cpp[NVC_MFC_DrawClient#7](../../mfc/reference/codesnippet/cpp/cmfcpopupmenubar-class_1.cpp)]  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CBasePane](../../mfc/reference/cbasepane-class.md)  
  
 [CPane](../../mfc/reference/cpane-class.md)  
  
 [CMFCBaseToolBar](../../mfc/reference/cmfcbasetoolbar-class.md)  
  
 [CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)  
  
 [CMFCPopupMenuBar](../../mfc/reference/cmfcpopupmenubar-class.md)  
  
## <a name="requirements"></a>惠?  
 **标头：** afxpopupmenubar.h  
  
##  <a name="adjustsizeimmediate"></a>CMFCPopupMenuBar::AdjustSizeImmediate  
 立即重新计算弹出菜单栏窗格的布局。 (重写[CPane::AdjustSizeImmediate](../../mfc/reference/cpane-class.md#adjustsizeimmediate)。  
  
```  
virtual void AdjustSizeImmediate(BOOL bRecalcLayout);
```  
  
### <a name="parameters"></a>参数  
 [in] `bRecalcLayout`  
 `TRUE`自动重新计算弹出窗口的菜单栏窗格中; 的布局否则为`FALSE`。  
  
### <a name="remarks"></a>备注  
  
##  <a name="buildorigitems"></a>CMFCPopupMenuBar::BuildOrigItems  
 从指定的菜单资源加载弹出菜单项。  
  
```  
BOOL BuildOrigItems(UINT uiMenuResID);
```  
  
### <a name="parameters"></a>参数  
 [in] `uiMenuResID`  
 指定要加载该菜单资源的菜单 ID。  
  
### <a name="return-value"></a>返回值  
 返回`TRUE`如果成功或`FALSE`如果不是。  
  
### <a name="remarks"></a>备注  
  
##  <a name="closedelayedsubmenu"></a>CMFCPopupMenuBar::CloseDelayedSubMenu  
 关闭已延迟的弹出菜单按钮。  
  
```  
virtual void CloseDelayedSubMenu();
```  
  
### <a name="remarks"></a>备注  
  
##  <a name="exporttomenu"></a>CMFCPopupMenuBar::ExportToMenu  
 生成中的菜单的弹出菜单按钮。  
  
```  
virtual HMENU ExportToMenu() const;  
```  
  
### <a name="return-value"></a>返回值  
 返回到新菜单的句柄。  
  
### <a name="remarks"></a>备注  
  
##  <a name="finddestintationtoolbar"></a>CMFCPopupMenuBar::FindDestintationToolBar  
 查找指定的点所在的工具栏。  
  
```  
CMFCToolBar* FindDestintationToolBar(CPoint point);
```  
  
### <a name="parameters"></a>参数  
 [in] `point`  
 在屏幕上点。  
  
### <a name="return-value"></a>返回值  
 返回的句柄到工具栏其中点位于，如果 therei 为 1，或`NULL`如果不是。  
  
### <a name="remarks"></a>备注  
  
##  <a name="getcurrentmenuimagesize"></a>CMFCPopupMenuBar::GetCurrentMenuImageSize  
 指示菜单按钮图像的大小。  
  
```  
virtual CSize GetCurrentMenuImageSize() const;  
```  
  
### <a name="return-value"></a>返回值  
 在工具栏中返回菜单按钮图像的大小。  
  
### <a name="remarks"></a>备注  
  
##  <a name="getdefaultmenuid"></a>CMFCPopupMenuBar::GetDefaultMenuId  
 返回默认菜单项的标识符。  
  
```  
UINT GetDefaultMenuId() const;  
```  
  
### <a name="return-value"></a>返回值  
 在弹出菜单栏中返回默认菜单项的标识符。  
  
### <a name="remarks"></a>备注  
  
##  <a name="getlastcommandindex"></a>CMFCPopupMenuBar::GetLastCommandIndex  
 获取最近调用菜单命令的索引。  
  
```  
static int __stdcall GetLastCommandIndex();
```  
  
### <a name="return-value"></a>返回值  
 返回已调用的最后一个菜单命令的索引。  
  
### <a name="remarks"></a>备注  
  
##  <a name="getoffset"></a>CMFCPopupMenuBar::GetOffset  
 获取弹出菜单栏的行偏移量。  
  
```  
int GetOffset() const;  
```  
  
### <a name="return-value"></a>返回值  
 返回的弹出菜单栏的行偏移量。  
  
### <a name="remarks"></a>备注  
 此值设置使用[CMFCPopupMenuBar::SetOffset](#setoffset)。  
  
##  <a name="importfrommenu"></a>CMFCPopupMenuBar::ImportFromMenu  
 从指定菜单导入弹出菜单按钮。  
  
```  
virtual BOOL ImportFromMenu(
    HMENU hMenu,  
    BOOL bShowAllCommands = FALSE);
```  
  
### <a name="parameters"></a>参数  
 [in] `hMenu`  
 要从中导入的弹出菜单按钮菜单。  
  
 [in] `bShowAllCommands`  
 `TRUE`如果该菜单上的所有命令导入，或`FALSE`如果很少使用的可能被隐藏。  
  
### <a name="return-value"></a>返回值  
 返回`TRUE`如果菜单按钮已成功从菜单中，导入或`FALSE`如果不是。  
  
### <a name="remarks"></a>备注  
  
##  <a name="isdropdownlistmode"></a>CMFCPopupMenuBar::IsDropDownListMode  
 指示弹出菜单栏是否在下拉列表列表模式下。  
  
```  
BOOL IsDropDownListMode() const;  
```  
  
### <a name="return-value"></a>返回值  
 返回`TRUE`弹出菜单栏是否在下拉列表列表模式下，或`FALSE`如果不是。  
  
### <a name="remarks"></a>备注  
  
##  <a name="ispalettemode"></a>CMFCPopupMenuBar::IsPaletteMode  
 指示弹出菜单栏是否在调色板模式下。  
  
```  
BOOL IsPaletteMode() const;  
```  
  
### <a name="return-value"></a>返回值  
 返回`TRUE`如果启用了调色板模式，或`FALSE`如果不是。  
  
### <a name="remarks"></a>备注  
 当菜单栏设置到调色板模式时，菜单项将出现在多个列和有限的数量的行。  
  
##  <a name="isribbonpanel"></a>CMFCPopupMenuBar::IsRibbonPanel  
 指示这是一个功能区面板 (`FALSE`默认情况下)。  
  
```  
virtual BOOL IsRibbonPanel() const;  
```  
  
### <a name="return-value"></a>返回值  
 返回`FALSE`默认情况下，该值指示这不功能区面板。  
  
### <a name="remarks"></a>备注  
  
##  <a name="isribbonpanelinregularmode"></a>CMFCPopupMenuBar::IsRibbonPanelInRegularMode  
 指示这是一个功能区面板常规模式下 (`FALSE`默认情况下)。  
  
```  
virtual BOOL IsRibbonPanelInRegularMode() const;  
```  
  
### <a name="return-value"></a>返回值  
 返回`FALSE`默认情况下，该值指示，这不功能区面板的常规模式下。  
  
### <a name="remarks"></a>备注  
  
##  <a name="loadfromhash"></a>CMFCPopupMenuBar::LoadFromHash  
 加载已存档的菜单。  
  
```  
BOOL LoadFromHash(HMENU hMenu);
```  
  
### <a name="parameters"></a>参数  
 [in] `hMenu`  
 要加载的已存档菜单句柄。  
  
### <a name="return-value"></a>返回值  
 返回`TRUE`如果成功，加载菜单或`FALSE`如果不是。  
  
### <a name="remarks"></a>备注  
  
##  <a name="m_bdisablesidebarinxpmode"></a>CMFCPopupMenuBar::m_bDisableSideBarInXPMode  
 一个布尔型参数，该值指示当有 Windows XP 外观时，你的应用程序是否具有灰色侧栏。  
  
```  
BOOL m_bDisableSideBarInXPMode;  
```  
  
### <a name="remarks"></a>备注  
 如果此成员变量设置为`FALSE`和你的应用程序具有 Windows XP 的外观，框架应用程序中绘制灰色侧栏。  
  
 默认值为 `FALSE`。  
  
##  <a name="restoredelayedsubmenu"></a>CMFCPopupMenuBar::RestoreDelayedSubMenu  
 还原延迟的菜单按钮用于关闭弹出菜单栏。  
  
```  
virtual void RestoreDelayedSubMenu();
```  
  
### <a name="remarks"></a>备注  
  
##  <a name="setbuttonstyle"></a>CMFCPopupMenuBar::SetButtonStyle  
 设置给定索引处的工具栏按钮的样式。 (重写[CMFCToolBar::SetButtonStyle](../../mfc/reference/cmfctoolbar-class.md#setbuttonstyle)。)  
  
```  
virtual void SetButtonStyle(
    int nIndex,  
    UINT nStyle);
```  
  
### <a name="parameters"></a>参数  
 [in] `nIndex`  
 都要设置其样式工具栏按钮的从零开始的索引。  
  
 [in] `nStyle`  
 按钮样式。 请参阅[工具栏控件样式](../../mfc/reference/toolbar-control-styles.md)可用工具栏按钮样式的列表。  
  
### <a name="remarks"></a>备注  
  
##  <a name="setoffset"></a>CMFCPopupMenuBar::SetOffset  
 设置弹出菜单栏的行偏移量。  
  
```  
void SetOffset(int iOffset);
```  
  
### <a name="parameters"></a>参数  
 [in] `iOffset`  
 应偏移弹出菜单栏的行数。  
  
### <a name="remarks"></a>备注  
  
##  <a name="startpopupmenutimer"></a>CMFCPopupMenuBar::StartPopupMenuTimer  
 启动指定的延迟的弹出菜单按钮的计时器。  
  
```  
void StartPopupMenuTimer(
    CMFCToolBarMenuButton* pMenuButton,  
    int nDelayFactor = 1);
```  
  
### <a name="parameters"></a>参数  
 [in] `pMenuButton`  
 指向为其设置延迟计时器的菜单按钮的指针。  
  
 [in] `nDelayFactor`  
 一个延迟的系数，等于至少一个，以乘以标准菜单延迟时间 （通常为半秒和 5 秒）。  
  
### <a name="remarks"></a>备注  
  
## <a name="see-also"></a>请参阅  
 [层次结构图](../../mfc/hierarchy-chart.md)   
 [类](../../mfc/reference/mfc-classes.md)   
 [CMFCColorBar 类](../../mfc/reference/cmfccolorbar-class.md)   
 [CMFCPopupMenu 类](../../mfc/reference/cmfcpopupmenu-class.md)
