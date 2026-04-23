---
title: vsp::ErrorMgrSingleton

---

# vsp::ErrorMgrSingleton






`#include <APIErrorMgr.h>`

Inherits from MessageBase

## Public Functions

|                | Name           |
| -------------- | -------------- |
| bool | **[PopErrorAndPrint](Classes/classvsp_1_1_error_mgr_singleton.md#function-poperrorandprint)**(FILE * stream) |
| void | **[AddError](Classes/classvsp_1_1_error_mgr_singleton.md#function-adderror)**([ERROR_CODE](Modules/group___enumerations.md#enum-error-code) code, const string & desc) |
| void | **[NoError](Classes/classvsp_1_1_error_mgr_singleton.md#function-noerror)**() |
| virtual void | **[MessageCallback](Classes/classvsp_1_1_error_mgr_singleton.md#function-messagecallback)**(const MessageBase * from, const MessageData & data) |
| ErrorMgrSingleton & | **[getInstance](Classes/classvsp_1_1_error_mgr_singleton.md#function-getinstance)**() |

## Public Functions Documentation

### function PopErrorAndPrint

```cpp
bool PopErrorAndPrint(
    FILE * stream
)
```


### function AddError

```cpp
void AddError(
    ERROR_CODE code,
    const string & desc
)
```


### function NoError

```cpp
void NoError()
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
static inline ErrorMgrSingleton & getInstance()
```


-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800