---
title: doca_netflow_template
summary: Template for the records. struct record_exmaple { uint32_t src_addr_V4; uint32_t dst_addr_V4; } struct doca_netflow_flowset_field fields[] = { {.type = DOCA_NETFLOW_IPV4_SRC_ADDR, .length = DOCA_NETFLOW_IPV4_SRC_ADDR_DEFAULT_LENGTH}, {.type = DOCA_NETFLOW_IPV4_DST_ADDR, .length = DOCA_NETFLOW_IPV4_DST_ADDR_DEFAULT_LENGTH} }; struct doca_netflow_template template = { .field_count = 2; .fields = fields; };. 

---

# doca_netflow_template

**Module:** **[NetFlow](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/)**



Template for the records. struct record_exmaple { uint32_t src_addr_V4; uint32_t dst_addr_V4; } struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/) fields[] = { {.type = DOCA_NETFLOW_IPV4_SRC_ADDR, .length = DOCA_NETFLOW_IPV4_SRC_ADDR_DEFAULT_LENGTH}, {.type = DOCA_NETFLOW_IPV4_DST_ADDR, .length = DOCA_NETFLOW_IPV4_DST_ADDR_DEFAULT_LENGTH} }; struct [doca_netflow_template]() template = { .field_count = 2; .fields = fields; };.  [More...](#detailed-description)


`#include <doca_netflow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| int | **[field_count](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/#variable-field_count)**  |
| struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/) * | **[fields](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/#variable-fields)**  |

## Detailed Description

```cpp
struct doca_netflow_template;
```

Template for the records. struct record_exmaple { uint32_t src_addr_V4; uint32_t dst_addr_V4; } struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/) fields[] = { {.type = DOCA_NETFLOW_IPV4_SRC_ADDR, .length = DOCA_NETFLOW_IPV4_SRC_ADDR_DEFAULT_LENGTH}, {.type = DOCA_NETFLOW_IPV4_DST_ADDR, .length = DOCA_NETFLOW_IPV4_DST_ADDR_DEFAULT_LENGTH} }; struct [doca_netflow_template]() template = { .field_count = 2; .fields = fields; };. 

**Note**: all fields are in network byte order. 
## Public Attributes Documentation

### variable field_count

```cpp
int field_count;
```


number of fields in 'fields' array - will be converted to uint16 


### variable fields

```cpp
struct doca_netflow_flowset_field * fields;
```


array of field info 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT