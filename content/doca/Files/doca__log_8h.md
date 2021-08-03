---
title: doca_log.h

---

# doca_log.h



## Types

|                | Name           |
| -------------- | -------------- |
| enum| **[DOCA_LOG_LEVEL](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#enum-doca_log_level)** { DOCA_LOG_LEVEL_CRIT, DOCA_LOG_LEVEL_ERROR, DOCA_LOG_LEVEL_WARNING, DOCA_LOG_LEVEL_INFO, DOCA_LOG_LEVEL_DEBUG}<br>log levels  |

## Functions

|                | Name           |
| -------------- | -------------- |
| int | **[doca_log_stream_redirect](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#function-doca_log_stream_redirect)**(FILE * stream)<br>redirect the logger to different stream  |
| void | **[doca_log_global_level_set](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#function-doca_log_global_level_set)**(uint32_t level)<br>Set the global log level.  |
| uint32_t | **[doca_log_type_register](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#function-doca_log_type_register)**(const char * type_name) |
| void | **[doca_log](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#function-doca_log)**(uint32_t level, uint32_t type, const char * format, ... ) |

## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[DOCA_LOG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log)**(level, ...) <br>Generates a log message.  |
|  | **[DOCA_LOG_CRIT](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log_crit)**(...) <br>Generates an CRITICAL log message.  |
|  | **[DOCA_LOG_ERR](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log_err)**(...) <br>Generates an ERROR log message.  |
|  | **[DOCA_LOG_WARN](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log_warn)**(...) <br>Generates an WARNING log message.  |
|  | **[DOCA_LOG_INFO](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log_info)**(...) <br>Generates an INFO log message.  |
|  | **[DOCA_LOG_DBG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log_dbg)**(...) <br>Generates an DEBUG log message.  |
|  | **[DOCA_DLOG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_dlog)**(...)  |
|  | **[DOCA_DLOG_CRIT](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_dlog_crit)**(...) <br>Generates an CRIT development log message.  |
|  | **[DOCA_DLOG_ERR](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_dlog_err)**(...) <br>Generates an ERROR development log message.  |
|  | **[DOCA_DLOG_WARN](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_dlog_warn)**(...) <br>Generates an WARNING development log message.  |
|  | **[DOCA_DLOG_INFO](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_dlog_info)**(...) <br>Generates an INFO development log message.  |
|  | **[DOCA_DLOG_DBG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_dlog_dbg)**(...) <br>Generates an DEBUG development log message.  |
|  | **[DOCA_LOG_REGISTER](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log_register)**(TYPE) <br>Registers log type on program start.  |

## Types Documentation

### enum DOCA_LOG_LEVEL

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DOCA_LOG_LEVEL_CRIT | |  Critical log level  |
| DOCA_LOG_LEVEL_ERROR | |  Error log level  |
| DOCA_LOG_LEVEL_WARNING | |  Warning log level  |
| DOCA_LOG_LEVEL_INFO | |  Info log level  |
| DOCA_LOG_LEVEL_DEBUG | |  Debug log level  |



log levels 


## Functions Documentation

### function doca_log_stream_redirect

```cpp
int doca_log_stream_redirect(
    FILE * stream
)
```

redirect the logger to different stream 

**Parameters**: 

  * **stream** Pointer to the stream. can't be NULL. 


**Return**: 0 on success, error code otherwise. 

Dynamically change the logger stream. can be file pointer or any stream. The default stream is stderr.


### function doca_log_global_level_set

```cpp
void doca_log_global_level_set(
    uint32_t level
)
```

Set the global log level. 

**Parameters**: 

  * **level** Log level enum DOCA_LOG_LEVEL 


Dynamically change global log level, any log under this type will be showen


### function doca_log_type_register

```cpp
uint32_t doca_log_type_register(
    const char * type_name
)
```


**Parameters**: 

  * **type_name** The string identifying the log type. should be in an hirechy form (i.e. DPI::Parser) 


**Return**: The log type identifier. negative for err. 

Register a log type

Will return the number associate with the log type. Log type will be showen in the logs.


### function doca_log

```cpp
void doca_log(
    uint32_t level,
    uint32_t type,
    const char * format,
    ... 
)
```


**Parameters**: 

  * **level** Log level enum DOCA_LOG_LEVEL 
  * **type** The log type identifier defined by doca_log_type_register 
  * **format** printf(3) arguments, format and variables 


Generates a log message.

The log will be showen in the doca_log_stream_redirect (see default). This should not be used, please prefer to use DOCA_LOG...




## Macros Documentation

### define DOCA_LOG

```cpp
#define DOCA_LOG(
    level,
    ...
)
	do {                                                                                       \
		[doca_log](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#function-doca_log)(DOCA_LOG_LEVEL_##level, log_id, __VA_ARGS__);                               \
	} while (0)
```

Generates a log message. 

**Parameters**: 

  * **level** Log level enum DOCA_LOG_LEVEL (just ERROR, WARNING...) 
  * **format** printf(3) arguments, format and variables 


The [DOCA_LOG()](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log) is the main log function for logging, This will effect performace. Consider using DOCA_DLOG for the option to remove it on the final compilation. Consider using the specific level DOCA_LOG for better code readebility (i.e. DOCA_LOG_ERROR)


### define DOCA_LOG_CRIT

```cpp
#define DOCA_LOG_CRIT(
    ...
)
[DOCA_LOG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log)(CRIT, __VA_ARGS__)
```

Generates an CRITICAL log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate critical log, This will effect performace. Consider using DOCA_DLOG for the option to remove it on the final compilation.


### define DOCA_LOG_ERR

```cpp
#define DOCA_LOG_ERR(
    ...
)
[DOCA_LOG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log)(ERROR, __VA_ARGS__)
```

Generates an ERROR log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate error log, This will effect performace. Consider using DOCA_DLOG for the option to remove it on the final compilation.


### define DOCA_LOG_WARN

```cpp
#define DOCA_LOG_WARN(
    ...
)
[DOCA_LOG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log)(WARNING, __VA_ARGS__)
```

Generates an WARNING log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate warning log, This will effect performace. Consider using DOCA_DLOG for the option to remove it on the final compilation.


### define DOCA_LOG_INFO

```cpp
#define DOCA_LOG_INFO(
    ...
)
[DOCA_LOG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log)(INFO, __VA_ARGS__)
```

Generates an INFO log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate info log, This will effect performace. Consider using DOCA_DLOG for the option to remove it on the final compilation.


### define DOCA_LOG_DBG

```cpp
#define DOCA_LOG_DBG(
    ...
)
[DOCA_LOG](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log)(DEBUG, __VA_ARGS__)
```

Generates an DEBUG log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate debug log, This will effect performace. Consider using DOCA_DLOG for the option to remove it on the final compilation.


### define DOCA_DLOG

```cpp
#define DOCA_DLOG(
    ...
)

```


### define DOCA_DLOG_CRIT

```cpp
#define DOCA_DLOG_CRIT(
    ...
)
DOCA_DLOG(CRIT, __VA_ARGS__)
```

Generates an CRIT development log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate critical log for development porpeses. To show the logs define DOCA_LOGGING_ALLOW_DLOG in the compilation veribales. This will not effect performance if compiled without DOCA_LOGGING_ALLOW_DLOG, will be removed.


### define DOCA_DLOG_ERR

```cpp
#define DOCA_DLOG_ERR(
    ...
)
DOCA_DLOG(ERROR, __VA_ARGS__)
```

Generates an ERROR development log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate error log for development porpeses. To show the logs define DOCA_LOGGING_ALLOW_DLOG in the compilation veribales. This will not effect performance if compiled without DOCA_LOGGING_ALLOW_DLOG, will be removed.


### define DOCA_DLOG_WARN

```cpp
#define DOCA_DLOG_WARN(
    ...
)
DOCA_DLOG(WARNING, __VA_ARGS__)
```

Generates an WARNING development log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate warning log for development porpeses. To show the logs define DOCA_LOGGING_ALLOW_DLOG in the compilation veribales. This will not effect performance if compiled without DOCA_LOGGING_ALLOW_DLOG, will be removed.


### define DOCA_DLOG_INFO

```cpp
#define DOCA_DLOG_INFO(
    ...
)
DOCA_DLOG(INFO, __VA_ARGS__)
```

Generates an INFO development log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate info log for development porpeses. To show the logs define DOCA_LOGGING_ALLOW_DLOG in the compilation veribales. This will not effect performance if compiled without DOCA_LOGGING_ALLOW_DLOG, will be removed.


### define DOCA_DLOG_DBG

```cpp
#define DOCA_DLOG_DBG(
    ...
)
DOCA_DLOG(DEBUG, __VA_ARGS__)
```

Generates an DEBUG development log message. 

**Parameters**: 

  * **format** printf(3) arguments, format and variables 


Will generate debug log for development porpeses. To show the logs define DOCA_LOGGING_ALLOW_DLOG in the compilation veribales. This will not effect performance if compiled without DOCA_LOGGING_ALLOW_DLOG, will be removed.


### define DOCA_LOG_REGISTER

```cpp
#define DOCA_LOG_REGISTER(
    TYPE
)
static int log_id;								\
static void __attribute__((constructor(65535), used)) __##__LINE__(void) \
{									\
	log_id = [doca_log_type_register](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#function-doca_log_type_register)(#TYPE);	\
}
```

Registers log type on program start. 

**Parameters**: 

  * **TYPE** A string representing the type 


Should be used to register the log type. For example

[DOCA_LOG_REGISTER(dpi)](localhost:1313/networking-ethernet-software/doca/modules/group___l_o_g_g_e_r/#define-doca_log_register)

void foo { DOCA_LOG_INFO("Message"); }


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

#ifndef _DOCA_LOG_H_
#define _DOCA_LOG_H_

#ifdef __cplusplus
extern "C" {
#endif

enum DOCA_LOG_LEVEL {
    DOCA_LOG_LEVEL_CRIT,    
    DOCA_LOG_LEVEL_ERROR,   
    DOCA_LOG_LEVEL_WARNING, 
    DOCA_LOG_LEVEL_INFO,    
    DOCA_LOG_LEVEL_DEBUG    
};

int doca_log_stream_redirect(FILE *stream);

void doca_log_global_level_set(uint32_t level);

uint32_t doca_log_type_register(const char *type_name);

void doca_log(uint32_t level, uint32_t type, const char *format, ...);

#define DOCA_LOG(level, ...)                                                                 \
    do {                                                                                       \
        doca_log(DOCA_LOG_LEVEL_##level, log_id, __VA_ARGS__);                               \
    } while (0)

#define DOCA_LOG_CRIT(...) DOCA_LOG(CRIT, __VA_ARGS__)

#define DOCA_LOG_ERR(...) DOCA_LOG(ERROR, __VA_ARGS__)

#define DOCA_LOG_WARN(...) DOCA_LOG(WARNING, __VA_ARGS__)

#define DOCA_LOG_INFO(...) DOCA_LOG(INFO, __VA_ARGS__)

#define DOCA_LOG_DBG(...) DOCA_LOG(DEBUG, __VA_ARGS__)

#ifdef DOCA_LOGGING_ALLOW_DLOG

#define DOCA_DLOG(level, ...) DOCA_LOG(level, __VA_ARGS__)

#else

#define DOCA_DLOG(...)

#endif

#define DOCA_DLOG_CRIT(...) DOCA_DLOG(CRIT, __VA_ARGS__)

#define DOCA_DLOG_ERR(...) DOCA_DLOG(ERROR, __VA_ARGS__)

#define DOCA_DLOG_WARN(...) DOCA_DLOG(WARNING, __VA_ARGS__)

#define DOCA_DLOG_INFO(...) DOCA_DLOG(INFO, __VA_ARGS__)

#define DOCA_DLOG_DBG(...) DOCA_DLOG(DEBUG, __VA_ARGS__)

#define DOCA_LOG_REGISTER(TYPE)             \
static int log_id;                              \
static void __attribute__((constructor(65535), used)) __##__LINE__(void) \
{                                   \
    log_id = doca_log_type_register(#TYPE); \
}

#ifdef __cplusplus
}
#endif

#endif
```


-------------------------------

Updated on  2 August 2021 at 20:00:04 EDT
