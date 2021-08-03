---
title: doca_netflow_flowset_field
summary: One field in netflow template, please look at doca_netflow_types for type macros. 

---

# doca_netflow_flowset_field

**Module:** **[NetFlow](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/)**



One field in netflow template, please look at doca_netflow_types for type macros. 


`#include <doca_netflow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| int | **[type](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/#variable-type)**  |
| int | **[length](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/#variable-length)**  |

## Public Attributes Documentation

### variable type

```cpp
int type;
```


field number id (see link) - will be converted to uint16 


### variable length

```cpp
int length;
```


field len in bytes (see link) - will be converted to uint16 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT