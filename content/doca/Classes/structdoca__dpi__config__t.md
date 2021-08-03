---
title: doca_dpi_config_t
summary: DPI init configuration. 

---

# doca_dpi_config_t

**Module:** **[Deep packet inspection](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/)**



DPI init configuration. 


`#include <doca_dpi.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint16_t | **[nb_queues](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__config__t/#variable-nb_queues)**  |
| uint32_t | **[max_packets_per_queue](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__config__t/#variable-max_packets_per_queue)**  |
| uint32_t | **[max_sig_match_len](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__config__t/#variable-max_sig_match_len)**  |

## Public Attributes Documentation

### variable nb_queues

```cpp
uint16_t nb_queues;
```


Number of DPI queues 


### variable max_packets_per_queue

```cpp
uint32_t max_packets_per_queue;
```


Number of packets concurrently processed by the DPI engine. 


### variable max_sig_match_len

```cpp
uint32_t max_sig_match_len;
```


The minimum required overlap between two packets for regex match 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT