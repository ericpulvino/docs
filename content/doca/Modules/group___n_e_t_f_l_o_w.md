---
title: NetFlow

---

# NetFlow

 [More...](#detailed-description)

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
| struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/) | **[__attribute__](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#variable-__attribute__)**  |

## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[DOCA_NETFLOW_CONF_DEFAULT_PATH](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/#define-doca_netflow_conf_default_path)** <br>default conf path to look for  |

## Detailed Description


**See**: [https://netflow.caligare.com/netflow_v9.htm](https://netflow.caligare.com/netflow_v9.htm)

Doca lib for export a netflow packet to a netflow collector.

This lib simplifies and centralizes the formatting and exporting of netflow packets. Netflow is a protocol for exporting information about the device network flows to a netflow collector that will aggregate and analyze the data. After creating conf file and invoke init function, the lib send function can be called with netflow struct to send a netflow packet with the format to the collector of choice specified in the conf file. The lib uses the netflow protocol specified by cisco. 
Conf File structure:

doca_netflow.conf

[doca_netflow_conf]

target = <hostname = name/ipv4/ipv6>:<port = integer>

source_id = <ID = integer>

version = <version = 9>

doca_netflow_default.conf

[doca_netflow_conf]

target = 127.0.0.1:2055

source_id = 10

version = 9

Limitations:

The lib supports the netflow V9 format. The lib is not thread safe. 


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



-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT