---
title: doca_flow_fwd
summary: forwarding configuration 

---

# doca_flow_fwd

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



forwarding configuration 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| enum [doca_flow_fwd_type](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-doca_flow_fwd_type) | **[type](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-type)**  |
| uint32_t | **[rss_flags](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-rss_flags)**  |
| uint16_t * | **[rss_queues](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-rss_queues)**  |
| int | **[num_of_queues](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-num_of_queues)**  |
| uint32_t | **[rss_mark](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-rss_mark)**  |
| uint16_t | **[port_id](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-port_id)**  |
| struct doca_flow_pipe * | **[next_pipe](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-next_pipe)**  |
| union doca_flow_fwd::@2 | **[@3](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/#variable-@3)**  |

## Public Attributes Documentation

### variable type

```cpp
enum doca_flow_fwd_type type;
```


indicate the forwarding type 


### variable rss_flags

```cpp
uint32_t rss_flags;
```


rss offload types 


### variable rss_queues

```cpp
uint16_t * rss_queues;
```


rss queues array 


### variable num_of_queues

```cpp
int num_of_queues;
```


number of queues 


### variable rss_mark

```cpp
uint32_t rss_mark;
```


markid of each queues 


### variable port_id

```cpp
uint16_t port_id;
```


destination port id 


### variable next_pipe

```cpp
struct doca_flow_pipe * next_pipe;
```


next pipe pointer 


### variable @3

```cpp
union doca_flow_fwd::@2 @3;
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT