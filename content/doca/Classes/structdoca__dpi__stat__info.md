---
title: doca_dpi_stat_info
summary: DPI statistics. 

---

# doca_dpi_stat_info

**Module:** **[Deep packet inspection](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/)**



DPI statistics. 


`#include <doca_dpi.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint32_t | **[nb_scanned_pkts](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_scanned_pkts)**  |
| uint32_t | **[nb_matches](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_matches)**  |
| uint32_t | **[nb_http_parser_based](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_http_parser_based)**  |
| uint32_t | **[nb_ssl_parser_based](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_ssl_parser_based)**  |
| uint32_t | **[nb_tcp_based](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_tcp_based)**  |
| uint32_t | **[nb_udp_based](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_udp_based)**  |
| uint32_t | **[nb_other_l4](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_other_l4)**  |
| uint32_t | **[nb_other_l7](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/#variable-nb_other_l7)**  |

## Public Attributes Documentation

### variable nb_scanned_pkts

```cpp
uint32_t nb_scanned_pkts;
```


Total number of scanned packets 


### variable nb_matches

```cpp
uint32_t nb_matches;
```


Total number of signature matches 


### variable nb_http_parser_based

```cpp
uint32_t nb_http_parser_based;
```


Total number of http signature matches 


### variable nb_ssl_parser_based

```cpp
uint32_t nb_ssl_parser_based;
```


Total number of ssl signature matches 


### variable nb_tcp_based

```cpp
uint32_t nb_tcp_based;
```


Total number of tco signature matches 


### variable nb_udp_based

```cpp
uint32_t nb_udp_based;
```


Total number of udp signature matches 


### variable nb_other_l4

```cpp
uint32_t nb_other_l4;
```


Total number of other l5 signature matches 


### variable nb_other_l7

```cpp
uint32_t nb_other_l7;
```


Total number of other l7 signature matches 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT