---
title: flow net define

---

# flow net define

 [More...](#detailed-description)

## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/)** <br>doca flow ip address  |
| struct | **[doca_flow_tun](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/)** <br>doca flow tunnel information  |

## Types

|                | Name           |
| -------------- | -------------- |
| enum| **[doca_flow_ip_type](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#enum-doca_flow_ip_type)** { DOCA_FLOW_ADDR_NONE = 0, DOCA_FLOW_IP4_ADDR = 4, DOCA_FLOW_IP6_ADDR = 6}<br>doca flow ip address type  |
| enum| **[doca_flow_tun_type](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#enum-doca_flow_tun_type)** { DOCA_FLOW_TUN_NONE = 0, DOCA_FLOW_TUN_VXLAN, DOCA_FLOW_TUN_GTPU, DOCA_FLOW_TUN_GRE}<br>doca flow tunnel type  |
| typedef uint16_t | **[doca_be16_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be16_t)**  |
| typedef uint32_t | **[doca_be32_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be32_t)**  |
| typedef uint64_t | **[doca_be64_t](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#typedef-doca_be64_t)**  |

## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[DOCA_ETHER_ADDR_LEN](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#define-doca_ether_addr_len)**  |
|  | **[DOCA_PROTO_TCP](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#define-doca_proto_tcp)**  |
|  | **[DOCA_PROTO_UDP](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#define-doca_proto_udp)**  |
|  | **[DOCA_PROTO_GRE](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#define-doca_proto_gre)**  |
|  | **[DOCA_GTPU_PORT](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#define-doca_gtpu_port)**  |
|  | **[DOCA_VXLAN_DEFAULT_PORT](localhost:1313/networking-ethernet-software/doca/modules/group___f_l_o_w___n_e_t/#define-doca_vxlan_default_port)**  |

## Detailed Description


DOCA HW offload flow net structure define. For more details please refer to the user guide on DOCA devzone. 

## Types Documentation

### enum doca_flow_ip_type

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_FLOW_ADDR_NONE | 0|  ip address is not set  |
| DOCA_FLOW_IP4_ADDR | 4|  ip address is ipv4  |
| DOCA_FLOW_IP6_ADDR | 6|  ip address is ipv6  |



doca flow ip address type 

### enum doca_flow_tun_type

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_FLOW_TUN_NONE | 0|  tunnel is not set  |
| DOCA_FLOW_TUN_VXLAN | |  tunnel is vxlan type  |
| DOCA_FLOW_TUN_GTPU | |  tunnel is gptu type  |
| DOCA_FLOW_TUN_GRE | |  tunnel is gre type  |



doca flow tunnel type 

### typedef doca_be16_t

```cpp
typedef uint16_t doca_be16_t;
```


16-bit big-endian value. 


### typedef doca_be32_t

```cpp
typedef uint32_t doca_be32_t;
```


32-bit big-endian value. 


### typedef doca_be64_t

```cpp
typedef uint64_t doca_be64_t;
```


64-bit big-endian value. 





## Macros Documentation

### define DOCA_ETHER_ADDR_LEN

```cpp
#define DOCA_ETHER_ADDR_LEN (6)
```


length of ether add length. 


### define DOCA_PROTO_TCP

```cpp
#define DOCA_PROTO_TCP (6)
```


Transmission Control Protocol. 


### define DOCA_PROTO_UDP

```cpp
#define DOCA_PROTO_UDP (17)
```


User Datagram Protocol. 


### define DOCA_PROTO_GRE

```cpp
#define DOCA_PROTO_GRE (47)
```


Cisco GRE tunnels (rfc 1701,1702). 


### define DOCA_GTPU_PORT

```cpp
#define DOCA_GTPU_PORT (2152)
```


gepu upd port id. 


### define DOCA_VXLAN_DEFAULT_PORT

```cpp
#define DOCA_VXLAN_DEFAULT_PORT (4789)
```


default vxlan port id. 




-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT