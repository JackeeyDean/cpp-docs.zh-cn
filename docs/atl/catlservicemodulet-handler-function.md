---
title: "CAtlServiceModuleT::Handler 函数 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CServiceModule::Handler
- CServiceModule.Handler
- Handler
dev_langs: C++
helpviewer_keywords: Handler method
ms.assetid: 14db5f2a-be87-4774-a296-445cb6fc7b2e
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 00158bbed5318d919c284b91cd651141a35bd441
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="catlservicemodulethandler-function"></a>CAtlServiceModuleT::Handler 函数
`CAtlServiceModuleT::Handler`服务控制管理器 (SCM) 调用来检索服务的状态，并授予它 （例如停止或暂停） 的各种说明的例程。 SCM 将传递到操作代码`Handler`以指示服务应执行的操作。 一个默认 ATL 生成服务仅处理停止指令。 如果 SCM 通过停止指令，则服务将通知 SCM 程序即将停止。 然后，服务调用`PostThreadMessage`发布到其自身发出退出的消息。 这将终止消息循环并将最终关闭服务。  
  
 若要处理的详细说明，你需要更改`m_status`中初始化的数据成员`CAtlServiceModuleT`构造函数。 此数据成员通知 SCM 时服务选择服务控制面板应用程序中启用哪些按钮。  
  
## <a name="see-also"></a>请参阅  
 [服务](../atl/atl-services.md)   
 [CAtlServiceModuleT::Handler](../atl/reference/catlservicemodulet-class.md#handler)

