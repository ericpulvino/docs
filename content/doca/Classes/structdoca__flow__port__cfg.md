---
title: doca_flow_port_cfg
summary: doca flow port configuration 

---

# doca_flow_port_cfg

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



doca flow port configuration 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint16_t | **[port_id](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__port__cfg/#variable-port_id)**  |
| enum [doca_flow_port_type](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-doca_flow_port_type) | **[type](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__port__cfg/#variable-type)**  |
| const char * | **[devargs](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__port__cfg/#variable-devargs)**  |
| uint16_t | **[priv_data_size](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__port__cfg/#variable-priv_data_size)**  |

## Public Attributes Documentation

### variable port_id

```cpp
uint16_t port_id;
```


dpdk port id 


### variable type

```cpp
enum doca_flow_port_type type;
```


mapping type of port 


### variable devargs

```cpp
const char * devargs;
```


specific per port type cfg 


### variable priv_data_size

```cpp
uint16_t priv_data_size;
```


user private data 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT