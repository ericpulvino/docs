---
title: doca_flow_match
summary: doca flow matcher information 

---

# doca_flow_match

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



doca flow matcher information 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint32_t | **[flags](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-flags)**  |
| uint8_t | **[out_src_mac](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-out_src_mac)**  |
| uint8_t | **[out_dst_mac](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-out_dst_mac)**  |
| [doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t) | **[vlan_id](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-vlan_id)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[out_src_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-out_src_ip)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[out_dst_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-out_dst_ip)**  |
| uint8_t | **[out_l4_type](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-out_l4_type)**  |
| [doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t) | **[out_src_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-out_src_port)**  |
| [doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t) | **[out_dst_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-out_dst_port)**  |
| struct [doca_flow_tun](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/) | **[tun](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-tun)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[in_src_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-in_src_ip)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[in_dst_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-in_dst_ip)**  |
| uint8_t | **[in_l4_type](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-in_l4_type)**  |
| [doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t) | **[in_src_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-in_src_port)**  |
| [doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t) | **[in_dst_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/#variable-in_dst_port)**  |

## Public Attributes Documentation

### variable flags

```cpp
uint32_t flags;
```


match items which are no value 


### variable out_src_mac

```cpp
uint8_t out_src_mac;
```


outer source mac address 


### variable out_dst_mac

```cpp
uint8_t out_dst_mac;
```


outer destination mac address 


### variable vlan_id

```cpp
doca_be16_t vlan_id;
```


outer vlan id 


### variable out_src_ip

```cpp
struct doca_flow_ip_addr out_src_ip;
```


outer source ip address 


### variable out_dst_ip

```cpp
struct doca_flow_ip_addr out_dst_ip;
```


outer destination ip address 


### variable out_l4_type

```cpp
uint8_t out_l4_type;
```


outer layer 4 protocol type 


### variable out_src_port

```cpp
doca_be16_t out_src_port;
```


outer layer 4 source port 


### variable out_dst_port

```cpp
doca_be16_t out_dst_port;
```


outer layer 4 destination port 


### variable tun

```cpp
struct doca_flow_tun tun;
```


tunnel info 


### variable in_src_ip

```cpp
struct doca_flow_ip_addr in_src_ip;
```


inner source ip address if tunnel is used 


### variable in_dst_ip

```cpp
struct doca_flow_ip_addr in_dst_ip;
```


inner destination ip address if tunnel is used 


### variable in_l4_type

```cpp
uint8_t in_l4_type;
```


inner layer 4 protocol type if tunnel is used 


### variable in_src_port

```cpp
doca_be16_t in_src_port;
```


inner layer 4 source port if tunnel is used 


### variable in_dst_port

```cpp
doca_be16_t in_dst_port;
```


inner layer 4 destination port if tunnel is used 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT