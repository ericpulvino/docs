---
title: doca_flow_pipe_cfg
summary: pipeline configuration 

---

# doca_flow_pipe_cfg

**Module:** **[flow](localhost:1313/networking-ethernet-software/doca/modules/group___flow/)**



pipeline configuration 


`#include <doca_flow.h>`

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| const char * | **[name](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/#variable-name)**  |
| struct doca_flow_port * | **[port](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/#variable-port)**  |
| struct [doca_flow_match](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/) * | **[match](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/#variable-match)**  |
| struct [doca_flow_match](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/) * | **[match_mask](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/#variable-match_mask)**  |
| struct [doca_flow_actions](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/) * | **[actions](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/#variable-actions)**  |
| struct [doca_flow_monitor](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/) * | **[monitor](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/#variable-monitor)**  |

## Public Attributes Documentation

### variable name

```cpp
const char * name;
```


name for the pipeline 


### variable port

```cpp
struct doca_flow_port * port;
```


port for the pipeline 


### variable match

```cpp
struct doca_flow_match * match;
```


matcher for the pipeline 


### variable match_mask

```cpp
struct doca_flow_match * match_mask;
```


match mask for the pipeline 


### variable actions

```cpp
struct doca_flow_actions * actions;
```


actions for the pipeline 


### variable monitor

```cpp
struct doca_flow_monitor * monitor;
```


monitor for the pipeline 


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT