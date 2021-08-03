---
title: doca_compat.h

---

# doca_compat.h



## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental)** <br>To set a Symbol (or specifically a function) as experimental.  |




## Macros Documentation

### define __DOCA_EXPERIMENTAL

```cpp
#define __DOCA_EXPERIMENTAL __attribute__((deprecated("Symbol is defined as experimental"), section(".text.experimental")))
```

To set a Symbol (or specifically a function) as experimental. 

## Source code

```cpp
/*
 * Copyright (C) 2021 Mellanox Technologies, Ltd. ALL RIGHTS RESERVED.
 *
 * This software product is a proprietary product of Mellanox Technologies Ltd.
 * (the "Company") and all right, title, and interest in and to the software
 * product, including all associated intellectual property rights, are and
 * shall remain exclusively with the Company.
 *
 * This software product is governed by the End User License Agreement
 * provided with the software product.
 *
 */

#ifndef _DOCA_COMPAT_H_
#define _DOCA_COMPAT_H_

#ifdef __cplusplus
extern "C" {
#endif

#ifndef DOCA_ALLOW_EXPERIMENTAL_API

#define __DOCA_EXPERIMENTAL \
__attribute__((deprecated("Symbol is defined as experimental"), section(".text.experimental")))

#else

#define __DOCA_EXPERIMENTAL \
__attribute__((section(".text.experimental")))

#endif

#ifdef __cplusplus
}
#endif

#endif
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT
