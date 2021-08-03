---
title: flow

---

# flow

 [More...](#detailed-description)

## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/)** <br>doca flow error message struct  |
| struct | **[doca_flow_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/)** <br>doca flow global configuration  |
| struct | **[doca_flow_port_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__port__cfg/)** <br>doca flow port configuration  |
| struct | **[doca_flow_match](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/)** <br>doca flow matcher information  |
| struct | **[doca_flow_encap_action](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/)** <br>doca flow encap data information  |
| struct | **[doca_flow_actions](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/)** <br>doca flow actions information  |
| struct | **[doca_flow_fwd](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/)** <br>forwarding configuration  |
| struct | **[doca_flow_monitor](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/)** <br>doca monitor action configuration  |
| struct | **[doca_flow_pipe_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/)** <br>pipeline configuration  |
| struct | **[doca_flow_query](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__query/)** <br>flow query result  |

## Types

|                | Name           |
| -------------- | -------------- |
| enum| **[doca_flow_error_type](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-doca_flow_error_type)** { DOCA_ERROR_UNKNOWN, DOCA_ERROR_UNSUPPORTED, DOCA_ERROR_PIPE_BUILD_ITEM, DOCA_ERROR_PIPE_BUILD_ACTION}<br>doca flow error type define  |
| enum| **[doca_flow_port_type](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-doca_flow_port_type)** { DOCA_FLOW_PORT_DPDK_BY_ID}<br>doca flow port type  |
| enum| **[doca_flow_match_flags](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-doca_flow_match_flags)** { DOCA_FLOW_MATCH_TCP_FIN}<br>doca flow match flags  |
| enum| **[doca_flow_fwd_type](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-doca_flow_fwd_type)** { DOCA_FLOW_FWD_NONE = 0, DOCA_FLOW_FWD_RSS, DOCA_FLOW_FWD_PORT, DOCA_FLOW_FWD_PIPE, DOCA_FLOW_FWD_DROP}<br>forwarding action type  |
| enum| **[doca_rss_type](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-doca_rss_type)** { DOCA_FLOW_RSS_IP = (1 << 0), DOCA_FLOW_RSS_UDP = (1 << 1), DOCA_FLOW_RSS_TCP = (1 << 2)}<br>rss offload types  |
| enum| **[@1](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#enum-@1)** { DOCA_FLOW_MONITOR_NONE = 0, DOCA_FLOW_MONITOR_METER = (1 << 1), DOCA_FLOW_MONITOR_COUNT = (1 << 2), DOCA_FLOW_MONITOR_AGING = (1 << 3)}<br>doca monitor action flags  |

## Functions

|                | Name           |
| -------------- | -------------- |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_flow_init](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_init)**(const struct [doca_flow_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/) * cfg, struct [doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/) * error)<br>Initialize the doca flow.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_flow_destroy](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_destroy)**(void )<br>Destroy the doca flow.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) struct doca_flow_port * | **[doca_flow_port_start](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_port_start)**(const struct [doca_flow_port_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__port__cfg/) * cfg, struct [doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/) * error)<br>Start a doca port.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_flow_port_stop](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_port_stop)**(struct doca_flow_port * port)<br>Stop a doca port.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) uint8_t * | **[doca_flow_port_priv_data](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_port_priv_data)**(struct doca_flow_port * port)<br>Get pointer of user private data.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) struct doca_flow_pipe * | **[doca_flow_create_pipe](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_create_pipe)**(const struct [doca_flow_pipe_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/) * cfg, const struct [doca_flow_fwd](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/) * fwd, struct [doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/) * error)<br>Create one new pipe.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) struct doca_flow_pipe_entry * | **[doca_flow_pipe_add_entry](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_pipe_add_entry)**(uint16_t pipe_queue, struct doca_flow_pipe * pipe, const struct [doca_flow_match](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/) * match, const struct [doca_flow_actions](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/) * actions, const struct [doca_flow_monitor](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/) * monitor, const struct [doca_flow_fwd](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/) * fwd, struct [doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/) * error)<br>Add one new entry to a pipe.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_flow_pipe_rm_entry](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_pipe_rm_entry)**(uint16_t pipe_queue, struct doca_flow_pipe_entry * entry)<br>Free one pipe entry.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_flow_destroy_pipe](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_destroy_pipe)**(uint16_t port_id, struct doca_flow_pipe * pipe)<br>Destroy one pipe.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_flow_flush_pipe](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_flush_pipe)**(uint16_t port_id)<br>flush pipes of one port  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_flow_destroy_port](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_destroy_port)**(uint16_t port_id)<br>Destroy a doca port.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_flow_dump_pipe](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_dump_pipe)**(uint16_t port_id, FILE * f)<br>Dump pipe of one port.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_flow_query](localhost:1313/networking-ethernet-software/doca/modules/group___flow/#function-doca_flow_query)**(struct doca_flow_pipe_entry * entry, struct [doca_flow_query](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__query/) * query_stats)<br>Extract information about specific entry.  |

## Detailed Description


DOCA HW offload flow library. For more details please refer to the user guide on DOCA devzone. 

## Types Documentation

### enum doca_flow_error_type

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_ERROR_UNKNOWN | |  Unknown error  |
| DOCA_ERROR_UNSUPPORTED | |  Operation unsupported  |
| DOCA_ERROR_PIPE_BUILD_ITEM | |  Build pipe match items error  |
| DOCA_ERROR_PIPE_BUILD_ACTION | |  Build pipe actions error  |



doca flow error type define 

### enum doca_flow_port_type

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_FLOW_PORT_DPDK_BY_ID | |  dpdk port by mapping id  |



doca flow port type 

### enum doca_flow_match_flags

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_FLOW_MATCH_TCP_FIN | |  match tcp packets with Fin flag  |



doca flow match flags 

### enum doca_flow_fwd_type

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_FLOW_FWD_NONE | 0|  No forward action be set  |
| DOCA_FLOW_FWD_RSS | |  Forwards packets to rss  |
| DOCA_FLOW_FWD_PORT | |  Forwards packets to one port  |
| DOCA_FLOW_FWD_PIPE | |  Forwards packets to another pipe  |
| DOCA_FLOW_FWD_DROP | |  Drops packets  |



forwarding action type 

### enum doca_rss_type

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_FLOW_RSS_IP | (1 << 0)|  rss by ip head  |
| DOCA_FLOW_RSS_UDP | (1 << 1)|  rss by udp head  |
| DOCA_FLOW_RSS_TCP | (1 << 2)|  rss by tcp head  |



rss offload types 

### enum @1

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_FLOW_MONITOR_NONE | 0|  No monitor action be set  |
| DOCA_FLOW_MONITOR_METER | (1 << 1)|  set monitor with meter action  |
| DOCA_FLOW_MONITOR_COUNT | (1 << 2)|  set monitor with counter action  |
| DOCA_FLOW_MONITOR_AGING | (1 << 3)|  set monitor with aging action  |



doca monitor action flags 


## Functions Documentation

### function doca_flow_init

```cpp
__DOCA_EXPERIMENTAL int doca_flow_init(
    const struct doca_flow_cfg * cfg,
    struct doca_flow_error * error
)
```

Initialize the doca flow. 

**Parameters**: 

  * **cfg** Port configuration, see [doca_flow_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/) for details. 
  * **error** Output error, set [doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/) for details. 


**Return**: 0 on success, a negative errno value otherwise and error is set. 

This is the global initialize function for doca flow, will initialize all resource used by doca flow.

It must be invoked first before any function in the API. One time call, used for doca flow initialize and global configurations.


### function doca_flow_destroy

```cpp
__DOCA_EXPERIMENTAL void doca_flow_destroy(
    void 
)
```

Destroy the doca flow. 

**Parameters**: 

  * **** 


Release all the resource used by doca flow .

It must be invoked at the end of application exit.


### function doca_flow_port_start

```cpp
__DOCA_EXPERIMENTAL struct doca_flow_port * doca_flow_port_start(
    const struct doca_flow_port_cfg * cfg,
    struct doca_flow_error * error
)
```

Start a doca port. 

**Parameters**: 

  * **cfg** Port configuration, see [doca_flow_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/) for details. 
  * **error** Output error, set [doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/) for details. 


**Return**: Port handler on success, NULL otherwise and error is set 

start a port with configuration, will create one port in doca flow layer, allocate all resources used by this port, and create the default offload flows include jump and default RSS for traffic.


### function doca_flow_port_stop

```cpp
__DOCA_EXPERIMENTAL int doca_flow_port_stop(
    struct doca_flow_port * port
)
```

Stop a doca port. 

**Parameters**: 

  * **port** Port struct 


**Return**: 0 on success, negative fail. 

Stop the port, disable the traffic.


### function doca_flow_port_priv_data

```cpp
__DOCA_EXPERIMENTAL uint8_t * doca_flow_port_priv_data(
    struct doca_flow_port * port
)
```

Get pointer of user private data. 

**Parameters**: 

  * **port** Port struct 


**Return**: private data head pointer 

user can manage specific data structure in port structure. the size of the data structure is given on port configuration, see [doca_flow_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/) for more details.


### function doca_flow_create_pipe

```cpp
__DOCA_EXPERIMENTAL struct doca_flow_pipe * doca_flow_create_pipe(
    const struct doca_flow_pipe_cfg * cfg,
    const struct doca_flow_fwd * fwd,
    struct doca_flow_error * error
)
```

Create one new pipe. 

**Parameters**: 

  * **cfg** Pipe configuration 
  * **fwd** Fwd configuration for the pipe 
  * **error** Output error 


**Return**: Pipe handler on success, NULL otherwise and error is set 

create new pipeline to match and offload specific packets, the pipe configuration includes those components: 

```
match: match one packet by inner or outer fields.
match_mask: the mask of match items.
actions: include the modify specific packets fields , Encap and
             Decap actions.
monitor: include Count, Age, and Meter actions.
fwd: the destination of matched action, include RSS, Hairpin,
        Port, and Drop actions.
```

 this API will create the pipe, but not actual start the HW offload.


### function doca_flow_pipe_add_entry

```cpp
__DOCA_EXPERIMENTAL struct doca_flow_pipe_entry * doca_flow_pipe_add_entry(
    uint16_t pipe_queue,
    struct doca_flow_pipe * pipe,
    const struct doca_flow_match * match,
    const struct doca_flow_actions * actions,
    const struct doca_flow_monitor * monitor,
    const struct doca_flow_fwd * fwd,
    struct doca_flow_error * error
)
```

Add one new entry to a pipe. 

**Parameters**: 

  * **pipe_queue** indentify each queue 
  * **pipe** Pointer to pipe 
  * **match** Pointer to match, indicate specific packet match information 
  * **actions** Pointer to modify actions, indicate specific modify information 
  * **monitor** Pointer to monitor actions. 
  * **fwd** Pointer to fwd actions. 
  * **error** Output error 


**Return**: Pipe entry handler on success, NULL otherwise and error is set 

when one packet match to one pipe, will start HW offload, pipe only define which files to match, when do offload, we need detail information from packets, or we need set some specific actions that pipe not define, the parameters include:

match: the detail packets fields according to the pipe definition. actions: the real actions according to the pipe definition. monitor: define the monitor actions if pipe not define it. fwd: define the forward action if pipe not define it.

This API will do the actual HW offload, with the input detail packets information.


### function doca_flow_pipe_rm_entry

```cpp
__DOCA_EXPERIMENTAL int doca_flow_pipe_rm_entry(
    uint16_t pipe_queue,
    struct doca_flow_pipe_entry * entry
)
```

Free one pipe entry. 

**Parameters**: 

  * **pipe_queue** indentify each queue 
  * **entry** the pipe entry be removed 
  * **error** Output error 


**Return**: 0 on success, negative on fail. 

This API will free the pipe entry, cancel HW offload. Application will hold the entry pointer when create one entry, if no need use this offload, for example, the entry aged, then use this API to free it.


### function doca_flow_destroy_pipe

```cpp
__DOCA_EXPERIMENTAL void doca_flow_destroy_pipe(
    uint16_t port_id,
    struct doca_flow_pipe * pipe
)
```

Destroy one pipe. 

**Parameters**: 

  * **port_id** port id of the port 
  * **pipe** Pointer to pipe 


Destroy the pipe, and the pipe entries matched this pipe.


### function doca_flow_flush_pipe

```cpp
__DOCA_EXPERIMENTAL void doca_flow_flush_pipe(
    uint16_t port_id
)
```

flush pipes of one port 

**Parameters**: 

  * **port_id** port id of the port 


Destroy all pipes and all pipe entries belong to the port.


### function doca_flow_destroy_port

```cpp
__DOCA_EXPERIMENTAL void doca_flow_destroy_port(
    uint16_t port_id
)
```

Destroy a doca port. 

**Parameters**: 

  * **port_id** port id of the port 


Destroy the doca port, free all resource of the port.


### function doca_flow_dump_pipe

```cpp
__DOCA_EXPERIMENTAL void doca_flow_dump_pipe(
    uint16_t port_id,
    FILE * f
)
```

Dump pipe of one port. 

**Parameters**: 

  * **port_id** port id of the port 
  * **f** the out put file of the pipe information 


Dump all pipes and all entries information belong to this port.


### function doca_flow_query

```cpp
__DOCA_EXPERIMENTAL int doca_flow_query(
    struct doca_flow_pipe_entry * entry,
    struct doca_flow_query * query_stats
)
```

Extract information about specific entry. 

**Parameters**: 

  * **entry** the pipe entry be queried 
  * **query_stats** data retrieved by the query 


**Return**: 0 on success, negative on fail. 

Query the packet statistics about specific pipe entry






-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT