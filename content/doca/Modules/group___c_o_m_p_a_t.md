---
title: Compatibility Management

---

# Compatibility Management

 [More...](#detailed-description)

## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental)** <br>To set a Symbol (or specifically a function) as experimental.  |

## Detailed Description


Lib to define compatibility with current version, define experimental Symbols.

To set a Symbol (or specifically a function) as experimental:

__DOCA_EXPERIMENTAL int func_declare(int param1, int param2);

To remove warnings of experimental compile with "-D DOCA_ALLOW_EXPERIMENTAL_API" 




## Macros Documentation

### define __DOCA_EXPERIMENTAL

```cpp
#define __DOCA_EXPERIMENTAL __attribute__((deprecated("Symbol is defined as experimental"), section(".text.experimental")))
```

To set a Symbol (or specifically a function) as experimental. 



-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT