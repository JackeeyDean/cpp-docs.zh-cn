---
title: "simple_partitioner 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- simple_partitioner
- PPL/concurrency::simple_partitioner
- PPL/concurrency::simple_partitioner::simple_partitioner
dev_langs: C++
helpviewer_keywords: simple_partitioner class
ms.assetid: d7e997af-54d1-43f5-abe0-def72df6edb3
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: f1d509afd9cddd8ac119d12ce2a0cb88906e83aa
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="simplepartitioner-class"></a>simple_partitioner 类
`simple_partitioner` 类表示由 `parallel_for` 循环访问的范围的静态分区。 分区程序将该范围分成区块，以便每个区块都至少具有区块大小指定的迭代数量。  
  
## <a name="syntax"></a>语法  
  
```
class simple_partitioner;
```  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|描述|  
|----------|-----------------|  
|[simple_partitioner](#ctor)|构造 `simple_partitioner` 对象。|  
|[~ simple_partitioner 析构函数](#dtor)|销毁 `simple_partitioner` 对象。|  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 `simple_partitioner`  
  
## <a name="requirements"></a>惠?  
 **标头：** ppl.h  
  
 **命名空间：** 并发  
  
##  <a name="dtor"></a>~ simple_partitioner 

 销毁 `simple_partitioner` 对象。  
  
```
~simple_partitioner();
```  
  
##  <a name="ctor"></a>simple_partitioner 

 构造 `simple_partitioner` 对象。  
  
```
explicit simple_partitioner(_Size_type _Chunk_size);
```  
  
### <a name="parameters"></a>参数  
 `_Chunk_size`  
  
## <a name="see-also"></a>请参阅  
 [并发命名空间](concurrency-namespace.md)
