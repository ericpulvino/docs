---
title: doca_dpi_result
summary: Dequeue result. 

---

# doca_dpi_result

**Module:** **[Deep packet inspection](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/)**



Dequeue result. 


`#include <doca_dpi.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| bool | **[matched](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/#variable-matched)**  |
| void * | **[user_data](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/#variable-user_data)**  |
| struct rte_mbuf * | **[pkt](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/#variable-pkt)**  |
| struct [doca_dpi_sig_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__sig__info/) | **[info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/#variable-info)**  |
| int | **[status_flags](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/#variable-status_flags)**  |

## Public Attributes Documentation

### variable matched

```cpp
bool matched;
```


Indicates flow was matched 


### variable user_data

```cpp
void * user_data;
```


User data provided on enqueue 


### variable pkt

```cpp
struct rte_mbuf * pkt;
```


Pkt provided on enqueue 


### variable info

```cpp
struct doca_dpi_sig_info info;
```


Signature information 


### variable status_flags

```cpp
int status_flags;
```


doca_dpi_flow_status flags 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT