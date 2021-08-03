---
title: Classes

---

# Classes




* **struct [doca_dpi_config_t](Classes/structdoca__dpi__config__t.md)** <br>DPI init configuration. 
* **struct [doca_dpi_parsing_info](Classes/structdoca__dpi__parsing__info.md)** <br>L2-L4 flow information. 
* **struct [doca_dpi_result](Classes/structdoca__dpi__result.md)** <br>Dequeue result. 
* **struct [doca_dpi_sig_data](Classes/structdoca__dpi__sig__data.md)** <br>Extra signature data. 
* **struct [doca_dpi_sig_info](Classes/structdoca__dpi__sig__info.md)** <br>Signature info. 
* **struct [doca_dpi_stat_info](Classes/structdoca__dpi__stat__info.md)** <br>DPI statistics. 
* **struct [doca_flow_actions](Classes/structdoca__flow__actions.md)** <br>doca flow actions information 
* **struct [doca_flow_cfg](Classes/structdoca__flow__cfg.md)** <br>doca flow global configuration 
* **struct [doca_flow_encap_action](Classes/structdoca__flow__encap__action.md)** <br>doca flow encap data information 
* **struct [doca_flow_error](Classes/structdoca__flow__error.md)** <br>doca flow error message struct 
* **struct [doca_flow_fwd](Classes/structdoca__flow__fwd.md)** <br>forwarding configuration 
* **struct [doca_flow_ip_addr](Classes/structdoca__flow__ip__addr.md)** <br>doca flow ip address 
* **struct [doca_flow_match](Classes/structdoca__flow__match.md)** <br>doca flow matcher information 
* **struct [doca_flow_monitor](Classes/structdoca__flow__monitor.md)** <br>doca monitor action configuration 
* **struct [doca_flow_pipe_cfg](Classes/structdoca__flow__pipe__cfg.md)** <br>pipeline configuration 
* **struct [doca_flow_port_cfg](Classes/structdoca__flow__port__cfg.md)** <br>doca flow port configuration 
* **struct [doca_flow_query](Classes/structdoca__flow__query.md)** <br>flow query result 
* **struct [doca_flow_tun](Classes/structdoca__flow__tun.md)** <br>doca flow tunnel information 
* **struct [doca_netflow_default_record](Classes/structdoca__netflow__default__record.md)** <br>Flow record, represent a flow at specific moment, usually after a flow end or after some timeout. Each one is a data record that will appear in the collector. This template is based on V5 fields with additional V9 fields. 
* **struct [doca_netflow_flowset_field](Classes/structdoca__netflow__flowset__field.md)** <br>One field in netflow template, please look at doca_netflow_types for type macros. 
* **struct [doca_netflow_template](Classes/structdoca__netflow__template.md)** <br>Template for the records. struct record_exmaple { uint32_t src_addr_V4; uint32_t dst_addr_V4; } struct [doca_netflow_flowset_field](Classes/structdoca__netflow__flowset__field.md) fields[] = { {.type = DOCA_NETFLOW_IPV4_SRC_ADDR, .length = DOCA_NETFLOW_IPV4_SRC_ADDR_DEFAULT_LENGTH}, {.type = DOCA_NETFLOW_IPV4_DST_ADDR, .length = DOCA_NETFLOW_IPV4_DST_ADDR_DEFAULT_LENGTH} }; struct [doca_netflow_template]() template = { .field_count = 2; .fields = fields; };. 



-------------------------------

Updated on  2 August 2021 at 19:52:09 EDT
