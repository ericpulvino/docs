---
title: doca_flow_tun
summary: doca flow tunnel information 

---

# doca_flow_tun

**Module:** **[flow net define](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/)**



doca flow tunnel information 


`#include <doca_flow_net.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| enum [doca_flow_tun_type](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#enum-doca_flow_tun_type) | **[type](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/#variable-type)**  |
| uint32_t | **[vxlan_tun_id](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/#variable-vxlan_tun_id)**  |
| [doca_be32_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be32_t) | **[gre_key](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/#variable-gre_key)**  |
| union doca_flow_tun::@14 | **[@15](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/#variable-@15)**  |

## Public Attributes Documentation

### variable type

```cpp
enum doca_flow_tun_type type;
```


tunnel type 


### variable vxlan_tun_id

```cpp
uint32_t vxlan_tun_id;
```


vxlan vni 


### variable gre_key

```cpp
doca_be32_t gre_key;
```


gre key 


### variable @15

```cpp
union doca_flow_tun::@14 @15;
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT