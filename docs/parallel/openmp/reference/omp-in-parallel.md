---
title: "omp_in_parallel |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: omp_in_parallel
dev_langs: C++
helpviewer_keywords: omp_in_parallel OpenMP function
ms.assetid: 1f01a1b4-78c5-496a-afb7-a43ecdad83d6
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 29aff17bd8da79bcdac0b2f1f4a2544acf6dc600
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ompinparallel"></a>omp_in_parallel
返回非零，如果从调用并行区域内。  
  
## <a name="syntax"></a>语法  
  
```  
int omp_in_parallel( );  
```  
  
## <a name="remarks"></a>备注  
 有关详细信息，请参阅[3.1.6 omp_in_parallel 函数](../../../parallel/openmp/3-1-6-omp-in-parallel-function.md)。  
  
## <a name="example"></a>示例  
  
```  
// omp_in_parallel.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
int main( )   
{  
    omp_set_num_threads(4);  
    printf_s("%d\n", omp_in_parallel( ));  
  
    #pragma omp parallel  
        #pragma omp master  
        {  
            printf_s("%d\n", omp_in_parallel( ));  
        }  
}  
```  
  
```Output  
0  
1  
```  
  
## <a name="see-also"></a>请参阅  
 [函数](../../../parallel/openmp/reference/openmp-functions.md)