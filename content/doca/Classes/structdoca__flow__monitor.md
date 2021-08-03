---
title: doca_flow_monitor
summary: doca monitor action configuration 

---

# doca_flow_monitor

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



doca monitor action configuration 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint8_t | **[flags](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/#variable-flags)**  |
| uint32_t | **[id](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/#variable-id)**  |
| uint64_t | **[cir](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/#variable-cir)**  |
| uint64_t | **[cbs](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/#variable-cbs)**  |
| struct doca_flow_monitor::@10 | **[@11](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/#variable-@11)**  |
| uint32_t | **[aging](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/#variable-aging)**  |

## Public Attributes Documentation

### variable flags

```cpp
uint8_t flags;
```


indicate which actions be included 


### variable id

```cpp
uint32_t id;
```


meter id 


### variable cir

```cpp
uint64_t cir;
```


Committed Information Rate (bytes/second). 


### variable cbs

```cpp
uint64_t cbs;
```


### variable @11

```cpp
struct doca_flow_monitor::@10 @11;
```


meter action configuration 


### variable aging

```cpp
uint32_t aging;
```


aging time in seconds. 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT