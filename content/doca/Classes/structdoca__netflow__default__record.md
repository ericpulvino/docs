---
title: doca_netflow_default_record
summary: Flow record, represent a flow at specific moment, usually after a flow end or after some timeout. Each one is a data record that will appear in the collector. This template is based on V5 fields with additional V9 fields. 

---

# doca_netflow_default_record

**Module:** **[NetFlow](localhost:1313/networking-ethernet-software/doca/modules/group___n_e_t_f_l_o_w/)**



Flow record, represent a flow at specific moment, usually after a flow end or after some timeout. Each one is a data record that will appear in the collector. This template is based on V5 fields with additional V9 fields.  [More...](#detailed-description)


`#include <doca_netflow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| __be32 | **[src_addr_v4](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-src_addr_v4)**  |
| __be32 | **[dst_addr_v4](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-dst_addr_v4)**  |
| struct in6_addr | **[src_addr_v6](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-src_addr_v6)**  |
| struct in6_addr | **[dst_addr_v6](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-dst_addr_v6)**  |
| __be32 | **[next_hop_v4](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-next_hop_v4)**  |
| struct in6_addr | **[next_hop_v6](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-next_hop_v6)**  |
| __be16 | **[input](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-input)**  |
| __be16 | **[output](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-output)**  |
| __be16 | **[src_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-src_port)**  |
| __be16 | **[dst_port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-dst_port)**  |
| uint8_t | **[tcp_flags](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-tcp_flags)**  |
| uint8_t | **[protocol](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-protocol)**  |
| uint8_t | **[tos](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-tos)**  |
| __be16 | **[src_as](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-src_as)**  |
| __be16 | **[dst_as](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-dst_as)**  |
| uint8_t | **[src_mask](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-src_mask)**  |
| uint8_t | **[dst_mask](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-dst_mask)**  |
| __be32 | **[d_pkts](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-d_pkts)**  |
| __be32 | **[d_octets](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-d_octets)**  |
| __be32 | **[first](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-first)**  |
| __be32 | **[last](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-last)**  |
| __be64 | **[flow_id](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-flow_id)**  |
| char | **[application_name](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/#variable-application_name)**  |

## Detailed Description

```cpp
struct doca_netflow_default_record;
```

Flow record, represent a flow at specific moment, usually after a flow end or after some timeout. Each one is a data record that will appear in the collector. This template is based on V5 fields with additional V9 fields. 

**Note**: all fields are in network byte order. 
## Public Attributes Documentation

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


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT