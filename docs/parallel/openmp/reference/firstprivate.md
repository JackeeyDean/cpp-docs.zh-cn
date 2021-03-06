---
title: "firstprivate |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: firstprivate
dev_langs: C++
helpviewer_keywords: firstprivate OpenMP clause
ms.assetid: db479766-6d3b-4bbd-b28e-b192d826788c
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 8c7d4a5ba23e343f7858bf3320ed05ebce84f1c2
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="firstprivate"></a>firstprivate
指定每个线程都应具有自己的变量中，实例和变量应用变量的值进行初始化，因为它在并行构造之前已存在。  
  
## <a name="syntax"></a>语法  
  
```  
firstprivate(var)  
```  
  
#### <a name="parameters"></a>参数  
  
|参数|描述|  
|---------------|-----------------|  
|`var`|此变量具有实例在每个线程，并将用变量的值初始化，因为它在并行构造之前已存在。 如果指定多个变量，则请用逗号分隔变量名。|  
  
## <a name="remarks"></a>备注  
  
## <a name="remarks"></a>备注  
 `firstprivate`适用于以下指令：  
  
-   [for](../../../parallel/openmp/reference/for-openmp.md)  
  
-   [parallel](../../../parallel/openmp/reference/parallel.md)  
  
-   [部分](../../../parallel/openmp/reference/sections-openmp.md)  
  
-   [single](../../../parallel/openmp/reference/single.md)  
  
 有关详细信息，请参阅[2.7.2.2 firstprivate](../../../parallel/openmp/2-7-2-2-firstprivate.md)。  
  
## <a name="example"></a>示例  
 有关使用示例`firstprivate`，请参阅中的示例[私有](../../../parallel/openmp/reference/private-openmp.md)。  
  
## <a name="see-also"></a>请参阅  
 [子句](../../../parallel/openmp/reference/openmp-clauses.md)