---
title: doca_flow_encap_action
summary: doca flow encap data information 

---

# doca_flow_encap_action

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



doca flow encap data information 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint8_t | **[src_mac](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/#variable-src_mac)**  |
| uint8_t | **[dst_mac](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/#variable-dst_mac)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[src_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/#variable-src_ip)**  |
| struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/) | **[dst_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/#variable-dst_ip)**  |
| struct [doca_flow_tun](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/) | **[tun](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/#variable-tun)**  |

## Public Attributes Documentation

### variable src_mac

```cpp
uint8_t src_mac;
```


source mac address 


### variable dst_mac

```cpp
uint8_t dst_mac;
```


destination mac address 


### variable src_ip

```cpp
struct doca_flow_ip_addr src_ip;
```


source ip address 


### variable dst_ip

```cpp
struct doca_flow_ip_addr dst_ip;
```


destination ip address 


### variable tun

```cpp
struct doca_flow_tun tun;
```


tunnel info 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT