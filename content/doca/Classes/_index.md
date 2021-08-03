---
title: Classes

---

# Classes




* **struct [doca_dpi_config_t](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__config__t/)** <br>DPI init configuration. 
* **struct [doca_dpi_parsing_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/)** <br>L2-L4 flow information. 
* **struct [doca_dpi_result](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/)** <br>Dequeue result. 
* **struct [doca_dpi_sig_data](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__sig__data/)** <br>Extra signature data. 
* **struct [doca_dpi_sig_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__sig__info/)** <br>Signature info. 
* **struct [doca_dpi_stat_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/)** <br>DPI statistics. 
* **struct [doca_flow_actions](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__actions/)** <br>doca flow actions information 
* **struct [doca_flow_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__cfg/)** <br>doca flow global configuration 
* **struct [doca_flow_encap_action](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__encap__action/)** <br>doca flow encap data information 
* **struct [doca_flow_error](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__error/)** <br>doca flow error message struct 
* **struct [doca_flow_fwd](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__fwd/)** <br>forwarding configuration 
* **struct [doca_flow_ip_addr](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__ip__addr/)** <br>doca flow ip address 
* **struct [doca_flow_match](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__match/)** <br>doca flow matcher information 
* **struct [doca_flow_monitor](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__monitor/)** <br>doca monitor action configuration 
* **struct [doca_flow_pipe_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__pipe__cfg/)** <br>pipeline configuration 
* **struct [doca_flow_port_cfg](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__port__cfg/)** <br>doca flow port configuration 
* **struct [doca_flow_query](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__query/)** <br>flow query result 
* **struct [doca_flow_tun](localhost:1313/networking-ethernet-software/doca/classes/structdoca__flow__tun/)** <br>doca flow tunnel information 
* **struct [doca_netflow_default_record](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__default__record/)** <br>Flow record, represent a flow at specific moment, usually after a flow end or after some timeout. Each one is a data record that will appear in the collector. This template is based on V5 fields with additional V9 fields. 
* **struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/)** <br>One field in netflow template, please look at doca_netflow_types for type macros. 
* **struct [doca_netflow_template](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__template/)** <br>Template for the records. struct record_exmaple { uint32_t src_addr_V4; uint32_t dst_addr_V4; } struct [doca_netflow_flowset_field](localhost:1313/networking-ethernet-software/doca/classes/structdoca__netflow__flowset__field/) fields[] = { {.type = DOCA_NETFLOW_IPV4_SRC_ADDR, .length = DOCA_NETFLOW_IPV4_SRC_ADDR_DEFAULT_LENGTH}, {.type = DOCA_NETFLOW_IPV4_DST_ADDR, .length = DOCA_NETFLOW_IPV4_DST_ADDR_DEFAULT_LENGTH} }; struct [doca_netflow_template]() template = { .field_count = 2; .fields = fields; };. 



-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT
