---
title: vsp::UpdateCountMgrSingleton

---

# vsp::UpdateCountMgrSingleton






`#include <APIUpdateCountMgr.h>`

Inherits from MessageBase

## Public Functions

|                | Name           |
| -------------- | -------------- |
| unsigned long | **[GetUpdateCount](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-getupdatecount)**() |
| void | **[ResetUpdateCount](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-resetupdatecount)**() |
| unsigned long | **[GetAndResetUpdateCount](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-getandresetupdatecount)**() |
| virtual void | **[MessageCallback](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-messagecallback)**(const MessageBase * from, const MessageData & data) |
| UpdateCountMgrSingleton & | **[getInstance](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-getinstance)**() |

## Public Functions Documentation

### function GetUpdateCount

```cpp
unsigned long GetUpdateCount()
```


### function ResetUpdateCount

```cpp
void ResetUpdateCount()
```


### function GetAndResetUpdateCount

```cpp
unsigned long GetAndResetUpdateCount()
```


### function MessageCallback

```cpp
virtual void MessageCallback(
    const MessageBase * from,
    const MessageData & data
)
```


### function getInstance

```cpp
static inline UpdateCountMgrSingleton & getInstance()
```


-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800