---
title: "toupper、_toupper、towupper、_toupper_l、_towupper_l | Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _toupper_l
- towupper
- toupper
- _towupper_l
- _toupper
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-string-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- towupper
- _toupper
- _totupper
- toupper
dev_langs: C++
helpviewer_keywords:
- _toupper function
- towupper function
- uppercase, converting strings to
- totupper function
- string conversion, to different characters
- towupper_l function
- toupper_l function
- string conversion, case
- _toupper_l function
- _towupper_l function
- _totupper function
- case, converting
- characters, converting
- toupper function
ms.assetid: cdef1b0f-b19c-4d11-b7d2-cf6334c9b6cc
caps.latest.revision: "16"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 0414cd211cb9b833f24d2aac9ad9a82758c4efcf
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="toupper-toupper-towupper-toupperl-towupperl"></a>toupper、_toupper、towupper、_toupper_l、_towupper_l
将字符转换为大写。  
  
## <a name="syntax"></a>语法  
  
```  
int toupper(  
   int c   
);  
int _toupper(  
   int c   
);  
int towupper(  
   wint_t c   
);  
int _toupper_l(  
   int c ,  
   _locale_t locale  
);  
int _towupper_l(  
   wint_t c ,  
   _locale_t locale  
);  
```  
  
#### <a name="parameters"></a>参数  
 `c`  
 要转换的字符。  
  
 `locale`  
 要使用的区域设置。  
  
## <a name="return-value"></a>返回值  
 如果可行，则其中的各个例程将转换 `c` 的副本，并返回结果。  
  
 如果 `c` 是 `iswlower` 为非零值的宽字符并且有 `iswupper` 为非零值的对应宽字符，则 `towupper` 返回对应的宽字符；否则，`towupper` 返回未改变的 `c`。  
  
 没有保留任何返回值以指示错误。  
  
 若要使 `toupper` 提供预期结果，[__isascii](../../c-runtime-library/reference/isascii-isascii-iswascii.md) 和 [islower](../../c-runtime-library/reference/islower-iswlower-islower-l-iswlower-l.md) 必须均返回非零值。  
  
## <a name="remarks"></a>备注  
 如果可行且恰当，则其中的各个例程将指定小写字母转换为大写字母。 `towupper` 的大小写转换是特定于区域设置的。 只改变与当前区域设置相关的字符的大小写。 没有 `_l` 后缀的函数使用当前设置的区域设置。 这些带有 `_l` 后缀的函数的版本将区域设置用作参数并使用它，而不是使用当前设置的区域设置。 有关详细信息，请参阅 [Locale](../../c-runtime-library/locale.md)。  
  
 若要使 `toupper` 提供预期结果，[__isascii](../../c-runtime-library/reference/isascii-isascii-iswascii.md) 和 [isupper](../../c-runtime-library/reference/isupper-isupper-l-iswupper-iswupper-l.md) 必须均返回非零值。  
  
 [数据转换例程](../../c-runtime-library/data-conversion.md)  
  
### <a name="generic-text-routine-mappings"></a>一般文本例程映射  
  
|TCHAR.H 例程|未定义 _UNICODE 和 _MBCS|已定义 _MBCS|已定义 _UNICODE|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_totupper`|`toupper`|`_mbctoupper`|`towupper`|  
|`_totupper_l`|`_toupper_l`|`_mbctoupper_l`|`_towupper_l`|  
  
> [!NOTE]
>  `_toupper_l` 和 `_towupper_l` 没有区域设置相关性，并且不应直接调用。 它们供 `_totupper_l` 内部使用。  
  
## <a name="requirements"></a>惠?  
  
|例程所返回的值|必需的标头|  
|-------------|---------------------|  
|`toupper`|\<ctype.h>|  
|`_toupper`|\<ctype.h>|  
|`towupper`|\<ctype.h 1> 或 \<wchar.h 1>|  
  
 有关其他兼容性信息，请参见“简介”中的 [兼容性](../../c-runtime-library/compatibility.md) 。  
  
## <a name="example"></a>示例  
 请参阅 [to 函数](../../c-runtime-library/to-functions.md)中的示例。  
  
## <a name="see-also"></a>请参阅  
 [is、isw 例程](../../c-runtime-library/is-isw-routines.md)   
 [to 函数](../../c-runtime-library/to-functions.md)   
 [区域设置](../../c-runtime-library/locale.md)   
 [多字节字符序列的解释](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)