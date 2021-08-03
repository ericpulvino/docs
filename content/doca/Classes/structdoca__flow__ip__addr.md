---
title: doca_flow_ip_addr
summary: doca flow ip address 

---

# doca_flow_ip_addr

**Module:** **[flow net define](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/)**



doca flow ip address 


`#include <doca_flow_net.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint8_t | **[type](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/#variable-type)**  |
| [doca_be32_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be32_t) | **[ipv4_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/#variable-ipv4_addr)**  |
| [doca_be32_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be32_t) | **[ipv6_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/#variable-ipv6_addr)**  |
| union doca_flow_ip_addr::@12 | **[@13](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/#variable-@13)**  |

## Public Attributes Documentation

### variable type

```cpp
uint8_t type;
```


ip address type 


### variable ipv4_addr

```cpp
doca_be32_t ipv4_addr;
```


ipv4 address if type is ipv4 


### variable ipv6_addr

```cpp
doca_be32_t ipv6_addr;
```


ipv6 address if type is ipv6 


### variable @13

```cpp
union doca_flow_ip_addr::@12 @13;
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT