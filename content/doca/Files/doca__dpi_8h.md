---
title: doca_dpi.h

---

# doca_dpi.h



## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[doca_dpi_config_t](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__config__t/)** <br>DPI init configuration.  |
| struct | **[doca_dpi_parsing_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/)** <br>L2-L4 flow information.  |
| struct | **[doca_dpi_sig_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__sig__info/)** <br>Signature info.  |
| struct | **[doca_dpi_sig_data](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__sig__data/)** <br>Extra signature data.  |
| struct | **[doca_dpi_result](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/)** <br>Dequeue result.  |
| struct | **[doca_dpi_stat_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/)** <br>DPI statistics.  |

## Types

|                | Name           |
| -------------- | -------------- |
| enum| **[doca_dpi_enqueue_status_t](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#enum-doca_dpi_enqueue_status_t)** { DOCA_DPI_ENQ_PROCESSING, DOCA_DPI_ENQ_PACKET_EMPTY, DOCA_DPI_ENQ_BUSY, DOCA_DPI_ENQ_INVALID_DB, DOCA_DPI_ENQ_INTERNAL_ERR}<br>Status of enqueue operation.  |
| enum| **[doca_dpi_dequeue_status_t](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#enum-doca_dpi_dequeue_status_t)** { DOCA_DPI_DEQ_NA, DOCA_DPI_DEQ_READY}<br>Status of dequeue operation.  |
| enum| **[doca_dpi_flow_status_t](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#enum-doca_dpi_flow_status_t)** { DOCA_DPI_STATUS_LAST_PACKET = 1 << 1, DOCA_DPI_STATUS_DESTROYED = 1 << 2, DOCA_DPI_STATUS_NEW_MATCH = 1 << 3}<br>Status of enqueued entry.  |
| enum| **[doca_dpi_sig_action_t](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#enum-doca_dpi_sig_action_t)** { DOCA_DPI_SIG_ACTION_NA, DOCA_DPI_SIG_ACTION_ALERT, DOCA_DPI_SIG_ACTION_PASS, DOCA_DPI_SIG_ACTION_DROP, DOCA_DPI_SIG_ACTION_REJECT, DOCA_DPI_SIG_ACTION_REJECTSRC, DOCA_DPI_SIG_ACTION_REJECTDST, DOCA_DPI_SIG_ACTION_REJECTBOTH}<br>Signature action. Some signatures may come with an action.  |

## Functions

|                | Name           |
| -------------- | -------------- |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) struct doca_dpi_ctx * | **[doca_dpi_init](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_init)**(const struct [doca_dpi_config_t](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__config__t/) * config, int * error)<br>Initialize the DPI library.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_dpi_destroy](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_destroy)**(struct doca_dpi_ctx * ctx)<br>Free the DPI memory and releases the regex engine.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_dpi_load_signatures](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_load_signatures)**(struct doca_dpi_ctx * ctx, const char * cdo_file)<br>Loads the cdo file.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_dpi_enqueue](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_enqueue)**(struct doca_dpi_flow_ctx * flow_ctx, struct rte_mbuf * pkt, bool initiator, uint32_t payload_offset, void * user_data)<br>Enqueue a new DPI job for processing.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_dpi_dequeue](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_dequeue)**(struct doca_dpi_ctx * ctx, uint16_t dpi_q, struct [doca_dpi_result](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/) * result)<br>Dequeues packets after processing.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) struct doca_dpi_flow_ctx * | **[doca_dpi_flow_create](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_flow_create)**(struct doca_dpi_ctx * ctx, uint16_t dpi_q, const struct [doca_dpi_parsing_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__parsing__info/) * parsing_info, int * error, struct [doca_dpi_result](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/) * result)<br>Creates a new flow on a queue.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_dpi_flow_destroy](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_flow_destroy)**(struct doca_dpi_flow_ctx * flow_ctx)<br>Destroys a flow on a queue.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_dpi_flow_match_get](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_flow_match_get)**(const struct doca_dpi_flow_ctx * flow_ctx, struct [doca_dpi_result](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__result/) * result)<br>Query a flow's match.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_dpi_signature_get](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_signature_get)**(const struct doca_dpi_ctx * ctx, uint32_t sig_id, struct [doca_dpi_sig_data](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__sig__data/) * sig_data)<br>Returns a specific sig info.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) int | **[doca_dpi_signatures_get](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_signatures_get)**(const struct doca_dpi_ctx * ctx, struct [doca_dpi_sig_data](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__sig__data/) ** sig_data)<br>Returns all signatures.  |
| [__DOCA_EXPERIMENTAL](localhost:1313/networking-ethernet-software/doca/modules/group___c_o_m_p_a_t/#define-__doca_experimental) void | **[doca_dpi_stat_get](localhost:1313/networking-ethernet-software/doca/modules/group___d_p_i/#function-doca_dpi_stat_get)**(const struct doca_dpi_ctx * ctx, bool clear, struct [doca_dpi_stat_info](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__stat__info/) * stats)<br>Returns DPI statistics.  |

## Types Documentation

### enum doca_dpi_enqueue_status_t

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_DPI_ENQ_PROCESSING | |  Packet enqueued for processing  |
| DOCA_DPI_ENQ_PACKET_EMPTY | |  No payload, packet was not queued  |
| DOCA_DPI_ENQ_BUSY | |  Packet cannot be enqueued, queue is full  |
| DOCA_DPI_ENQ_INVALID_DB | |  load_signatures failed, or was never called  |
| DOCA_DPI_ENQ_INTERNAL_ERR | |   |



Status of enqueue operation. 

### enum doca_dpi_dequeue_status_t

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_DPI_DEQ_NA | |  No DPI enqueued jobs done, or no packets to dequeue  |
| DOCA_DPI_DEQ_READY | |  DPI Job and result is valid  |



Status of dequeue operation. 

### enum doca_dpi_flow_status_t

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_DPI_STATUS_LAST_PACKET | 1 << 1|  Indicates there are no more packets in queue from this flow.  |
| DOCA_DPI_STATUS_DESTROYED | 1 << 2|  Indicates flow was destroyed while being processed  |
| DOCA_DPI_STATUS_NEW_MATCH | 1 << 3|  Indicates flow was matched on current dequeue  |



Status of enqueued entry. 

### enum doca_dpi_sig_action_t

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_DPI_SIG_ACTION_NA | |  Action not available for signature  |
| DOCA_DPI_SIG_ACTION_ALERT | |  Alert  |
| DOCA_DPI_SIG_ACTION_PASS | |  Signature indicates that the flow is allowed  |
| DOCA_DPI_SIG_ACTION_DROP | |  Signature indicates that the flow should be dropped  |
| DOCA_DPI_SIG_ACTION_REJECT | |  Send RST/ICMP unreach error to the sender of the matching packet  |
| DOCA_DPI_SIG_ACTION_REJECTSRC | |  Send RST/ICMP unreach error to the sender of the matching packet  |
| DOCA_DPI_SIG_ACTION_REJECTDST | |  Send RST/ICMP error packet to receiver of the matching packet  |
| DOCA_DPI_SIG_ACTION_REJECTBOTH | |  Send RST/ICMP error packets to both sides of the conversation  |



Signature action. Some signatures may come with an action. 


## Functions Documentation

### function doca_dpi_init

```cpp
__DOCA_EXPERIMENTAL struct doca_dpi_ctx * doca_dpi_init(
    const struct doca_dpi_config_t * config,
    int * error
)
```

Initialize the DPI library. 

**Parameters**: 

  * **config** See [doca_dpi_config_t](localhost:1313/networking-ethernet-software/doca/classes/structdoca__dpi__config__t/) for details. 
  * **error** Output error, negative value indicates an error. 


**Return**: doca_dpi_ctx - dpi opaque context, NULL on error. 

This function must be invoked first before any function in the API. It should be invoked once per process. This call will probe the first regex device it finds (0). 


### function doca_dpi_destroy

```cpp
__DOCA_EXPERIMENTAL void doca_dpi_destroy(
    struct doca_dpi_ctx * ctx
)
```

Free the DPI memory and releases the regex engine. 

**Parameters**: 

  * **ctx** DPI context to destroy. 


### function doca_dpi_load_signatures

```cpp
__DOCA_EXPERIMENTAL int doca_dpi_load_signatures(
    struct doca_dpi_ctx * ctx,
    const char * cdo_file
)
```

Loads the cdo file. 

**Parameters**: 

  * **ctx** The DPI context. 
  * **cdo_file** CDO file created by the DPI compiler. 


**Return**: 0 on success, error code otherwise. 

The cdo file contains signature information. The cdo file must be loaded before any enqueue call.

Database update: When a new signatures database is available, the user may call this function again. The newly loaded CDO must contain the signatures of the previously loaded CDO or result will be undefined. 


### function doca_dpi_enqueue

```cpp
__DOCA_EXPERIMENTAL int doca_dpi_enqueue(
    struct doca_dpi_flow_ctx * flow_ctx,
    struct rte_mbuf * pkt,
    bool initiator,
    uint32_t payload_offset,
    void * user_data
)
```

Enqueue a new DPI job for processing. 

**Parameters**: 

  * **flow_ctx** The flow context handler. 
  * **pkt** The mbuf to be processed. 
  * **initiator** Indicates to which direction the packet belongs. Typically, the first packet will arrive from the initiator. 
  * **payload_offset** Indicates where the packet's payload begins. 
  * **user_data** Private user data to b returned when the DPI job is dequeued. 


**Return**: doca_dpi_enqueue_status_t or other error code. 

This function is thread-safe per queue. For best performance it should always be called form the same thread/queue on which the flow was created. See Multithreading section of the DPI Programming Guide for more details.

Once a packet is enqueued, the DPI engine will increase ref count in the mbuf. User must not change or reuse the mbuf while it is being processed. See "Packet Ownership" section of the DPI Programming Guide for more details.

The injected packet has to be stripped of FCS. A packet will not be enqueued if:

* Payload length = 0


### function doca_dpi_dequeue

```cpp
__DOCA_EXPERIMENTAL int doca_dpi_dequeue(
    struct doca_dpi_ctx * ctx,
    uint16_t dpi_q,
    struct doca_dpi_result * result
)
```

Dequeues packets after processing. 

**Parameters**: 

  * **ctx** The DPI context. 
  * **dpi_q** The DPI queue from which to enqueue the flows. 
  * **result** Output, matching result. 


**Return**: doca_dpi_dequeue_status_t if successful, error code otherwise 

Only packets enqueued for processing will be returned by this API. Packets will return in the order they were enqueued.


### function doca_dpi_flow_create

```cpp
__DOCA_EXPERIMENTAL struct doca_dpi_flow_ctx * doca_dpi_flow_create(
    struct doca_dpi_ctx * ctx,
    uint16_t dpi_q,
    const struct doca_dpi_parsing_info * parsing_info,
    int * error,
    struct doca_dpi_result * result
)
```

Creates a new flow on a queue. 

**Parameters**: 

  * **ctx** The DPI context. 
  * **dpi_q** The DPI queue on which to create the flows 
  * **parsing_info** L3/L4 information. 
  * **error** Output, Negative if error occurred. 
  * **result** Output, If flow was matched based on the parsing info, result->matched will be true. 


**Return**: NULL on error. 

Must be called before enqueuing any new packet. A flow must not be created on 2 different queues.


### function doca_dpi_flow_destroy

```cpp
__DOCA_EXPERIMENTAL void doca_dpi_flow_destroy(
    struct doca_dpi_flow_ctx * flow_ctx
)
```

Destroys a flow on a queue. 

**Parameters**: 

  * **flow_ctx** The flow context to destroy. 


Should be called when a flow is terminated or times out


### function doca_dpi_flow_match_get

```cpp
__DOCA_EXPERIMENTAL int doca_dpi_flow_match_get(
    const struct doca_dpi_flow_ctx * flow_ctx,
    struct doca_dpi_result * result
)
```

Query a flow's match. 

**Parameters**: 

  * **flow_ctx** The flow context of the flow to be queried. 
  * **result** Output, latest match on this flow. 


**Return**: 0 on success, error code otherwise. 

### function doca_dpi_signature_get

```cpp
__DOCA_EXPERIMENTAL int doca_dpi_signature_get(
    const struct doca_dpi_ctx * ctx,
    uint32_t sig_id,
    struct doca_dpi_sig_data * sig_data
)
```

Returns a specific sig info. 

**Parameters**: 

  * **ctx** The DPI context. 
  * **sig_id** The DPI queue on which the flow was created. 
  * **sig_data** Output of the sig metadata. 


**Return**: 0 on success, error code otherwise. 

### function doca_dpi_signatures_get

```cpp
__DOCA_EXPERIMENTAL int doca_dpi_signatures_get(
    const struct doca_dpi_ctx * ctx,
    struct doca_dpi_sig_data ** sig_data
)
```

Returns all signatures. 

**Parameters**: 

  * **ctx** The DPI context. 
  * **sig_data** Output of the sig data. 


**Return**: 0 on success, error code otherwise. 

It is the responsibility of the user to free the array. Because this function copies all the sig info, it is highly recommended to call this function only once after loading the database, and not during packet processing.


### function doca_dpi_stat_get

```cpp
__DOCA_EXPERIMENTAL void doca_dpi_stat_get(
    const struct doca_dpi_ctx * ctx,
    bool clear,
    struct doca_dpi_stat_info * stats
)
```

Returns DPI statistics. 

**Parameters**: 

  * **ctx** The DPI context. 
  * **clear** Clear the statistics after fetching them. 
  * **stats** Output struct containing the statistics. 




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

#ifndef DOCA_DPI_H_
#define DOCA_DPI_H_

#ifdef __cplusplus
extern "C" {
#endif

#include <stdint.h>
#include <stdbool.h>
#include <rte_mbuf.h>
#include <netinet/in.h>
#include <linux/types.h>

#include <doca_compat.h>

enum doca_dpi_enqueue_status_t {
    DOCA_DPI_ENQ_PROCESSING,
    DOCA_DPI_ENQ_PACKET_EMPTY,
    DOCA_DPI_ENQ_BUSY,
    DOCA_DPI_ENQ_INVALID_DB,
    DOCA_DPI_ENQ_INTERNAL_ERR,
    /* Other system errors possible */
};

enum doca_dpi_dequeue_status_t {
    DOCA_DPI_DEQ_NA,
    DOCA_DPI_DEQ_READY,
};

enum doca_dpi_flow_status_t {
    DOCA_DPI_STATUS_LAST_PACKET = 1 << 1,
    DOCA_DPI_STATUS_DESTROYED = 1 << 2,
    DOCA_DPI_STATUS_NEW_MATCH = 1 << 3,
};

enum doca_dpi_sig_action_t {
    DOCA_DPI_SIG_ACTION_NA,
    DOCA_DPI_SIG_ACTION_ALERT,
    DOCA_DPI_SIG_ACTION_PASS,
    DOCA_DPI_SIG_ACTION_DROP,
    DOCA_DPI_SIG_ACTION_REJECT,
    DOCA_DPI_SIG_ACTION_REJECTSRC,
    DOCA_DPI_SIG_ACTION_REJECTDST,
    DOCA_DPI_SIG_ACTION_REJECTBOTH,
};

struct doca_dpi_config_t {
    uint16_t nb_queues;
    uint32_t max_packets_per_queue;
    uint32_t max_sig_match_len;
};

struct doca_dpi_parsing_info {
    __be16 ethertype;
    uint8_t l4_protocol;
    in_port_t l4_dport;
    in_port_t l4_sport;
    union {
        struct in_addr ipv4;
        struct in6_addr ipv6;
    } dst_ip;
};

struct doca_dpi_sig_info {
    uint32_t sig_id;
    int action;
};

struct doca_dpi_sig_data {
    uint32_t sig_id;
    char name[1024];
};

struct doca_dpi_result {
    bool matched;
    void *user_data;
    struct rte_mbuf *pkt;
    struct doca_dpi_sig_info info;
    int status_flags;
};

struct doca_dpi_stat_info {
    uint32_t nb_scanned_pkts;
    uint32_t nb_matches;
    uint32_t nb_http_parser_based;
    uint32_t nb_ssl_parser_based;
    uint32_t nb_tcp_based;
    uint32_t nb_udp_based;
    uint32_t nb_other_l4;
    uint32_t nb_other_l7;
};

struct doca_dpi_flow_ctx;

struct doca_dpi_ctx;

__DOCA_EXPERIMENTAL
struct doca_dpi_ctx *doca_dpi_init(const struct doca_dpi_config_t *config, int *error);

__DOCA_EXPERIMENTAL
void doca_dpi_destroy(struct doca_dpi_ctx *ctx);

__DOCA_EXPERIMENTAL
int doca_dpi_load_signatures(struct doca_dpi_ctx *ctx, const char *cdo_file);

__DOCA_EXPERIMENTAL
int doca_dpi_enqueue(struct doca_dpi_flow_ctx *flow_ctx, struct rte_mbuf *pkt,
             bool initiator, uint32_t payload_offset, void *user_data);

__DOCA_EXPERIMENTAL
int doca_dpi_dequeue(struct doca_dpi_ctx *ctx, uint16_t dpi_q, struct doca_dpi_result *result);

__DOCA_EXPERIMENTAL
struct doca_dpi_flow_ctx *doca_dpi_flow_create(struct doca_dpi_ctx *ctx, uint16_t dpi_q,
                           const struct doca_dpi_parsing_info *parsing_info,
                           int *error,
                           struct doca_dpi_result *result);

__DOCA_EXPERIMENTAL
void doca_dpi_flow_destroy(struct doca_dpi_flow_ctx *flow_ctx);

__DOCA_EXPERIMENTAL
int doca_dpi_flow_match_get(const struct doca_dpi_flow_ctx *flow_ctx,
                struct doca_dpi_result *result);

__DOCA_EXPERIMENTAL
int doca_dpi_signature_get(const struct doca_dpi_ctx *ctx, uint32_t sig_id,
               struct doca_dpi_sig_data *sig_data);

__DOCA_EXPERIMENTAL
int doca_dpi_signatures_get(const struct doca_dpi_ctx *ctx, struct doca_dpi_sig_data **sig_data);

__DOCA_EXPERIMENTAL
void doca_dpi_stat_get(const struct doca_dpi_ctx *ctx, bool clear,
               struct doca_dpi_stat_info *stats);

#ifdef __cplusplus
}
#endif

#endif /* DPI_H_ */
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT
