---
title: "Platform:: recreateexception 方法 |Microsoft 文档"
ms.custom: 
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: VCCORLIB/Platform::Exception
dev_langs: C++
helpviewer_keywords: Platform::Exception Class
ms.assetid: fa73d1ab-86e4-4d26-a7d9-81938c1c7e77
caps.latest.revision: "6"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 3aa5ed7cecab49f44eb44b43747b06e63adb8605
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="platformrecreateexception-method"></a>Platform::ReCreateException 方法
此方法仅供内部使用，不用于用户代码。 请改用 exception:: createexception 方法。

## <a name="syntax"></a>语法

```cpp
static Exception^ ReCreateException(int hr)
```

### <a name="parameters"></a>参数
`hr`

### <a name="property-valuereturn-value"></a>属性值/返回值

基于指定的 HRESULT 返回新的 Platform::Exception^。

