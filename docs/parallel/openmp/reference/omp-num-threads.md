---
title: "OMP_NUM_THREADS |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: OMP_NUM_THREADS
dev_langs: C++
helpviewer_keywords: OMP_NUM_THREADS OpenMP environment variable
ms.assetid: 4b558124-1387-4c30-a6a5-ff5345a9ced6
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: a5f6af2ff547ddb95b6d4ef6b9c6d353399c17c5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ompnumthreads"></a>OMP_NUM_THREADS
在并行区域中，设置最大线程数，除非通过重写[omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md)或[num_threads](../../../parallel/openmp/reference/num-threads.md)。  
  
## <a name="syntax"></a>语法  
  
```  
set OMP_NUM_THREADS[=num]  
```  
  
## <a name="remarks"></a>备注  
 其中，  
  
 `num`  
 最大你想在并行区域中，最多为 64 Visual c + + 实现中的线程数。  
  
## <a name="remarks"></a>备注  
 **OMP_NUM_THREADS**环境变量可以通过重写[omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md)函数或通过[num_threads](../../../parallel/openmp/reference/num-threads.md)。  
  
 默认值`num`Visual c + + 中实现的 OpenMP 标准是虚拟处理器，包括超线程的 Cpu 数。  
  
 有关详细信息，请参阅[4.2 OMP_NUM_THREADS](../../../parallel/openmp/4-2-omp-num-threads.md)。  
  
## <a name="example"></a>示例  
 下面的命令集**OMP_NUM_THREADS**为 16 的环境变量：  
  
```  
set OMP_NUM_THREADS=16  
```  
  
 下面的命令显示的当前设置**OMP_NUM_THREADS**环境变量：  
  
```  
set OMP_NUM_THREADS  
```  
  
## <a name="see-also"></a>请参阅  
 [环境变量](../../../parallel/openmp/reference/openmp-environment-variables.md)