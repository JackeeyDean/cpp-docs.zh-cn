---
title: "处理控件通知消息中日期和时间选取器 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- DTN_CLOSEUP
- DTN_DATETIMECHANGE
- DTN_DROPDOWN
dev_langs: C++
helpviewer_keywords:
- DTN_DROPDOWN notification [MFC]
- DTN_DATETIMECHANGE notification [MFC]
- DTN_CLOSEUP notification [MFC]
- DateTimePicker control [MFC], handling notifications
- CDateTimeCtrl class [MFC], handling notifications
- DTN_FORMAT notification [MFC]
- DateTimePicker control [MFC]
ms.assetid: ffbe29ab-ff80-4609-89f7-260b404439c4
caps.latest.revision: "11"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 836714f7a7ca17d759d0d71a7cbb30d63fdfaf95
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="processing-notification-messages-in-date-and-time-picker-controls"></a>处理日期和时间选取器控件中的通知消息
用户与日期和时间选取器控件，该控件进行交互 (`CDateTimeCtrl`) 将通知消息发送到其父窗口，通常是视图或对话框对象。 如果您要在响应中做些什么，请处理这些消息。 例如，当用户打开日期和时间选取器，以便显示嵌入的月历控件， **DTN_DROPDOWN**发送通知。  
  
 请使用“属性”窗口将通知处理程序添加到你希望实现的那些消息的父类。  
  
 以下列表介绍由日期和时间选取器控件发送各种通知。  
  
-   **DTN_DROPDOWN**通知即将显示嵌入的月历控件的父级。 此通知将只发送时**DTS_UPDOWN**尚未设置样式。 此通知的详细信息，请参阅[访问嵌入月历控件](../mfc/accessing-the-embedded-month-calendar-control.md)。  
  
-   **DTN_CLOSEUP**通知即将关闭嵌入的月历控件的父级。 此通知将只发送时**DTS_UPDOWN**尚未设置样式。  
  
-   **DTN_DATETIMECHANGE**通知控件中发生了更改的父级。  
  
-   **DTN_FORMAT**通知父级需要文本中的回调字段中显示。 此通知并回调字段的详细信息，请参阅[日期和时间选取器控件中使用回调字段](../mfc/using-callback-fields-in-a-date-and-time-picker-control.md)。  
  
-   **DTN_FORMATQUERY**请求父提供将在回调字段中显示的字符串的最大大小。 处理此通知就可以控制对在所有时间，减少闪烁控件的显示中正确显示输出。 此通知的详细信息，请参阅[日期和时间选取器控件中使用回调字段](../mfc/using-callback-fields-in-a-date-and-time-picker-control.md)。  
  
-   **DTN_USERSTRING**通知父用户已完成编辑日期和时间选取器控件的内容。 此通知将只发送时**DTS_APPCANPARSE**设置样式。  
  
-   **DTN_WMKEYDOWN**通知父级，当用户在回调字段键入。 处理此通知来模拟键盘响应支持的日期和时间选取器控件中的非回调字段相同。 此通知的详细信息，请参阅[DTP 控件中支持回调字段](http://msdn.microsoft.com/library/windows/desktop/bb761726)Windows SDK 中。  
  
## <a name="see-also"></a>请参阅  
 [使用 CDateTimeCtrl](../mfc/using-cdatetimectrl.md)   
 [控件](../mfc/controls-mfc.md)

