---
title: doca_flow_actions
summary: doca flow actions information 

---

# doca_flow_actions

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



doca flow actions information 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| bool | **[decap](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-decap)**  |
| uint8_t | **[mod_src_mac](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-mod_src_mac)**  |
| uint8_t | **[mod_dst_mac](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-mod_dst_mac)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[mod_src_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-mod_src_ip)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[mod_dst_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-mod_dst_ip)**  |
| [doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t) | **[mod_src_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-mod_src_port)**  |
| [doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t) | **[mod_dst_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-mod_dst_port)**  |
| bool | **[dec_ttl](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-dec_ttl)**  |
| bool | **[has_encap](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-has_encap)**  |
| struct [doca_flow_encap_action](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/) | **[encap](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/#variable-encap)**  |

## Public Attributes Documentation

### variable decap

```cpp
bool decap;
```


when true, will do decap 


### variable mod_src_mac

```cpp
uint8_t mod_src_mac;
```


modify source mac address 


### variable mod_dst_mac

```cpp
uint8_t mod_dst_mac;
```


modify destination mac address 


### variable mod_src_ip

```cpp
struct doca_flow_ip_addr mod_src_ip;
```


modify source ip address 


### variable mod_dst_ip

```cpp
struct doca_flow_ip_addr mod_dst_ip;
```


modify destination ip address 


### variable mod_src_port

```cpp
doca_be16_t mod_src_port;
```


modify layer 4 source port 


### variable mod_dst_port

```cpp
doca_be16_t mod_dst_port;
```


modify layer 4 destination port 


### variable dec_ttl

```cpp
bool dec_ttl;
```


decrease TTL value 


### variable has_encap

```cpp
bool has_encap;
```


when true, will do encap 


### variable encap

```cpp
struct doca_flow_encap_action encap;
```


encap data information 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT