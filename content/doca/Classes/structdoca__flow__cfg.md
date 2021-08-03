---
title: doca_flow_cfg
summary: doca flow global configuration 

---

# doca_flow_cfg

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



doca flow global configuration 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint32_t | **[total_sessions](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/#variable-total_sessions)**  |
| uint16_t | **[queues](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/#variable-queues)**  |
| bool | **[is_hairpin](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/#variable-is_hairpin)**  |
| bool | **[aging](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/#variable-aging)**  |

## Public Attributes Documentation

### variable total_sessions

```cpp
uint32_t total_sessions;
```


total flows count 


### variable queues

```cpp
uint16_t queues;
```


queue id for each offload thread 


### variable is_hairpin

```cpp
bool is_hairpin;
```


when true, the fwd will be hairpin queue 


### variable aging

```cpp
bool aging;
```


when true, aging is handled by doca 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT