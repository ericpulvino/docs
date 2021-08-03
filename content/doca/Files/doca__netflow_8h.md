---
title: doca_netflow.h

---

# doca_netflow.h



## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[doca_netflow_default_record](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/)** <br>Flow record, represent a flow at specific moment, usually after a flow end or after some timeout. Each one is a data record that will appear in the collector. This template is based on V5 fields with additional V9 fields.  |
| struct | **[doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/)** <br>One field in netflow template, please look at doca_netflow_types for type macros.  |
| struct | **[doca_netflow_template](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/)** <br>Template for the records. struct record_exmaple { uint32_t src_addr_V4; uint32_t dst_addr_V4; } struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/) fields[] = { {.type = DOCA_NETFLOW_IPV4_SRC_ADDR, .length = DOCA_NETFLOW_IPV4_SRC_ADDR_DEFAULT_LENGTH}, {.type = DOCA_NETFLOW_IPV4_DST_ADDR, .length = DOCA_NETFLOW_IPV4_DST_ADDR_DEFAULT_LENGTH} }; struct [doca_netflow_template]() template = { .field_count = 2; .fields = fields; };.  |

## Functions

|                | Name           |
| -------------- | -------------- |
| struct [doca_netflow_default_record](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/) | **[__attribute__](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#function-__attribute__)**((packed) ) |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) const struct [doca_netflow_template](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/) * | **[doca_netflow_template_default_get](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#function-doca_netflow_template_default_get)**(void )<br>Return a default [doca_netflow_template](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/) for use in send function, if using default template use [doca_netflow_default_record](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/) struct for records.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_netflow_exporter_init](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#function-doca_netflow_exporter_init)**(const char * netflow_conf_file)<br>Init exporter memory, set configs and open connection.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_netflow_exporter_send](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#function-doca_netflow_exporter_send)**(const struct [doca_netflow_template](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/) * template, const void ** records, size_t length, int * error)<br>Sending netflow records. Need to init first.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_netflow_exporter_destroy](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#function-doca_netflow_exporter_destroy)**(void )<br>Free the exporter memory and close connection.  |

## Attributes

|                | Name           |
| -------------- | -------------- |
| __be32 | **[src_addr_v4](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-src_addr_v4)**  |
| __be32 | **[dst_addr_v4](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-dst_addr_v4)**  |
| struct in6_addr | **[src_addr_v6](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-src_addr_v6)**  |
| struct in6_addr | **[dst_addr_v6](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-dst_addr_v6)**  |
| __be32 | **[next_hop_v4](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-next_hop_v4)**  |
| struct in6_addr | **[next_hop_v6](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-next_hop_v6)**  |
| __be16 | **[input](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-input)**  |
| __be16 | **[output](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-output)**  |
| __be16 | **[src_port](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-src_port)**  |
| __be16 | **[dst_port](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-dst_port)**  |
| uint8_t | **[tcp_flags](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-tcp_flags)**  |
| uint8_t | **[protocol](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-protocol)**  |
| uint8_t | **[tos](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-tos)**  |
| __be16 | **[src_as](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-src_as)**  |
| __be16 | **[dst_as](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-dst_as)**  |
| uint8_t | **[src_mask](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-src_mask)**  |
| uint8_t | **[dst_mask](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-dst_mask)**  |
| __be32 | **[d_pkts](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-d_pkts)**  |
| __be32 | **[d_octets](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-d_octets)**  |
| __be32 | **[first](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-first)**  |
| __be32 | **[last](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-last)**  |
| __be64 | **[flow_id](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-flow_id)**  |
| char | **[application_name](localhost:1313/networking-ethernet-software/doca/files/doca__netflow_8h/#variable-application_name)**  |
| struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/) | **[__attribute__](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#variable-__attribute__)**  |

## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[DOCA_NETFLOW_CONF_DEFAULT_PATH](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#define-doca_netflow_conf_default_path)** <br>default conf path to look for  |


## Functions Documentation

### function __attribute__

```cpp
struct doca_netflow_default_record __attribute__(
    (packed) 
)
```


### function doca_netflow_template_default_get

```cpp
__DOCA_EXPERIMENTAL const struct doca_netflow_template * doca_netflow_template_default_get(
    void 
)
```

Return a default [doca_netflow_template](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/) for use in send function, if using default template use [doca_netflow_default_record](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/) struct for records. 

**Return**: pointer containing the default template 

### function doca_netflow_exporter_init

```cpp
__DOCA_EXPERIMENTAL int doca_netflow_exporter_init(
    const char * netflow_conf_file
)
```

Init exporter memory, set configs and open connection. 

**Parameters**: 

  * **netflow_conf_file** Doca netflow configure file pointer including a section marked as [doca_netflow_conf], if a NULL pointer is given then look at default path in DOCA_NETFLOW_CONF_DEFAULT_PATH. This function can be called again only after doca_netflow_exporter_destroy was called. 


**Return**: 0 on success, error code otherwise. 

### function doca_netflow_exporter_send

```cpp
__DOCA_EXPERIMENTAL int doca_netflow_exporter_send(
    const struct doca_netflow_template * template,
    const void ** records,
    size_t length,
    int * error
)
```

Sending netflow records. Need to init first. 

**Parameters**: 

  * **template** Template pointer how the records are structed. for more info reffer to [doca_netflow_template](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/). 
  * **records** Array of pointers to the flows structs to send, must be packed. strings must be a direct array in the struct not a pointer. 
  * **length** Records array size. 
  * **error** If return value is -1 populate this field with the error. 


**Return**: Number of records sent, -1 on error. 

**Note**: 

  * if the return value is positive but not equal to length then just some of the records have sent. the send function sould run again with the remaining records. please reffer to the exmaple. 
  * When sending more then 30 records the lib split the records to multiple packets because packet can send up to 30 records (Netflow protocol limit) 


### function doca_netflow_exporter_destroy

```cpp
__DOCA_EXPERIMENTAL void doca_netflow_exporter_destroy(
    void 
)
```

Free the exporter memory and close connection. 


## Attributes Documentation

### variable src_addr_v4

```cpp
__be32 src_addr_v4;
```


Source IPV4 Address 


### variable dst_addr_v4

```cpp
__be32 dst_addr_v4;
```


Destination IPV4 Address 


### variable src_addr_v6

```cpp
struct in6_addr src_addr_v6;
```


Source IPV6 Address 


### variable dst_addr_v6

```cpp
struct in6_addr dst_addr_v6;
```


Destination IPV6 Address 


### variable next_hop_v4

```cpp
__be32 next_hop_v4;
```


Next hop router's IPV4 Address 


### variable next_hop_v6

```cpp
struct in6_addr next_hop_v6;
```


Next hop router's IPV6 Address 


### variable input

```cpp
__be16 input;
```


Input interface index 


### variable output

```cpp
__be16 output;
```


Output interface index 


### variable src_port

```cpp
__be16 src_port;
```


TCP/UDP source port number or equivalent 


### variable dst_port

```cpp
__be16 dst_port;
```


TCP/UDP destination port number or equivalent 


### variable tcp_flags

```cpp
uint8_t tcp_flags;
```


Cumulative OR of tcp flags 


### variable protocol

```cpp
uint8_t protocol;
```


IP protocol type (for example, TCP = 6;UDP = 17) 


### variable tos

```cpp
uint8_t tos;
```


IP Type-of-Service 


### variable src_as

```cpp
__be16 src_as;
```


originating AS of source address 


### variable dst_as

```cpp
__be16 dst_as;
```


originating AS of destination address 


### variable src_mask

```cpp
uint8_t src_mask;
```


source address prefix mask bits 


### variable dst_mask

```cpp
uint8_t dst_mask;
```


destination address prefix mask bits 


### variable d_pkts

```cpp
__be32 d_pkts;
```


Packets sent in Duration 


### variable d_octets

```cpp
__be32 d_octets;
```


Octets sent in Duration. 


### variable first

```cpp
__be32 first;
```


SysUptime at start of flow 


### variable last

```cpp
__be32 last;
```


and of last packet of flow 


### variable flow_id

```cpp
__be64 flow_id;
```


This identifies a transaction within a connection 


### variable application_name

```cpp
char application_name;
```


Name associated with a classification 


### variable __attribute__

```cpp
struct doca_netflow_flowset_field __attribute__;
```



## Macros Documentation

### define DOCA_NETFLOW_CONF_DEFAULT_PATH

```cpp
#define DOCA_NETFLOW_CONF_DEFAULT_PATH "/etc/doca_netflow.conf"
```

default conf path to look for 

## Source code

```cpp
/*
 * Copyright (C) 2021 Mellanox Technologies, Ltd. ALL RIGHTS RESERVED.
 *
 * This software product is a proprietary product of Mellanox Technologies Ltd.
 * (the "Company") and all right, title, and interest in and to the software
 * product, including all associated intellectual property rights, are and
 * shall remain exclusively with the Company.
 *
 * This software product is governed by the End User License Agreement
 * provided with the software product.
 *
 */

#ifndef _DOCA_NETFLOW__H_
#define _DOCA_NETFLOW__H_

#ifdef __cplusplus
extern "C" {
#endif

#include <linux/types.h>
#include <stdbool.h>
#include <stddef.h>
#include <stdint.h>
#include "doca_compat.h"
#include "doca_netflow_types.h"

#define DOCA_NETFLOW_CONF_DEFAULT_PATH "/etc/doca_netflow.conf"

struct doca_netflow_default_record {
    __be32 src_addr_v4;             
    __be32 dst_addr_v4;             
    struct in6_addr src_addr_v6;            
    struct in6_addr dst_addr_v6;            
    __be32 next_hop_v4;             
    struct in6_addr next_hop_v6;            
    __be16 input;                   
    __be16 output;                  
    __be16 src_port;                
    __be16 dst_port;                
    uint8_t tcp_flags;              
    uint8_t protocol;               
    uint8_t tos;                    
    __be16 src_as;                  
    __be16 dst_as;                  
    uint8_t src_mask;               
    uint8_t dst_mask;               
    __be32 d_pkts;                  
    __be32 d_octets;                
    __be32 first;                   
    __be32 last;                    
    __be64 flow_id;                 
    char application_name[DOCA_NETFLOW_APPLICATION_NAME_DEFAULT_LENGTH];
} __attribute__((packed));

struct doca_netflow_flowset_field {
    int type;   
    int length; 
};

struct doca_netflow_template {
    int field_count; 
    struct doca_netflow_flowset_field *fields; 
};

__DOCA_EXPERIMENTAL
const struct doca_netflow_template *doca_netflow_template_default_get(void);

__DOCA_EXPERIMENTAL
int doca_netflow_exporter_init(const char *netflow_conf_file);

__DOCA_EXPERIMENTAL
int doca_netflow_exporter_send(const struct doca_netflow_template *template, const void **records,
                   size_t length, int *error);

__DOCA_EXPERIMENTAL
void doca_netflow_exporter_destroy(void);

#ifdef __cplusplus
}
#endif

#endif
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT
