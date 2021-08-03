---
title: doca_dpi_parsing_info
summary: L2-L4 flow information. 

---

# doca_dpi_parsing_info

**Module:** **[Deep packet inspection](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/)**



L2-L4 flow information. 


`#include <doca_dpi.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| __be16 | **[ethertype](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/#variable-ethertype)**  |
| uint8_t | **[l4_protocol](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/#variable-l4_protocol)**  |
| in_port_t | **[l4_dport](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/#variable-l4_dport)**  |
| in_port_t | **[l4_sport](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/#variable-l4_sport)**  |
| struct in_addr | **[ipv4](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/#variable-ipv4)**  |
| struct in6_addr | **[ipv6](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/#variable-ipv6)**  |
| union doca_dpi_parsing_info::@0 | **[dst_ip](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/#variable-dst_ip)**  |

## Public Attributes Documentation

### variable ethertype

```cpp
__be16 ethertype;
```


Ethertype of the packet in network byte order 


### variable l4_protocol

```cpp
uint8_t l4_protocol;
```


Layer 4 protocol 


### variable l4_dport

```cpp
in_port_t l4_dport;
```


Layer 4 destination port in network byte order 


### variable l4_sport

```cpp
in_port_t l4_sport;
```


Layer 4 source port in network byte order 


### variable ipv4

```cpp
struct in_addr ipv4;
```


Ipv4 destination address in network byte order 


### variable ipv6

```cpp
struct in6_addr ipv6;
```


Ipv6 destination address in network byte order 


### variable dst_ip

```cpp
union doca_dpi_parsing_info::@0 dst_ip;
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT