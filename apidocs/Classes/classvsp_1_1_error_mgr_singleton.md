---
title: vsp::ErrorMgrSingleton

---

# vsp::ErrorMgrSingleton






`#include <APIErrorMgr.h>`

Inherits from [MessageBase](Classes/class_message_base.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| bool | **[PopErrorAndPrint](Classes/classvsp_1_1_error_mgr_singleton.md#function-poperrorandprint)**(FILE * stream) |
| void | **[AddError](Classes/classvsp_1_1_error_mgr_singleton.md#function-adderror)**([ERROR_CODE](Modules/group___enumerations.md#enum-error-code) code, const string & desc) |
| void | **[NoError](Classes/classvsp_1_1_error_mgr_singleton.md#function-noerror)**() |
| virtual void | **[MessageCallback](Classes/classvsp_1_1_error_mgr_singleton.md#function-messagecallback)**(const [MessageBase](Classes/class_message_base.md) * from, const [MessageData](Classes/class_message_data.md) & data)<br>Callback function executed when message received.  |
| ErrorMgrSingleton & | **[getInstance](Classes/classvsp_1_1_error_mgr_singleton.md#function-getinstance)**() |

## Additional inherited members

**Public Functions inherited from [MessageBase](Classes/class_message_base.md)**

|                | Name           |
| -------------- | -------------- |
| | **[MessageBase](Classes/class_message_base.md#function-messagebase)**() |
| virtual | **[~MessageBase](Classes/class_message_base.md#function-~messagebase)**() |
| virtual void | **[SetName](Classes/class_message_base.md#function-setname)**(const string & name)<br>Set message listener name.  |
| virtual string | **[GetName](Classes/class_message_base.md#function-getname)**()<br>Get message listener name.  |
| virtual void | **[Register](Classes/class_message_base.md#function-register)**() |
| virtual void | **[Register](Classes/class_message_base.md#function-register)**(const string & name) |
| virtual void | **[UnRegister](Classes/class_message_base.md#function-unregister)**() |

**Protected Attributes inherited from [MessageBase](Classes/class_message_base.md)**

|                | Name           |
| -------------- | -------------- |
| string | **[m_Name](Classes/class_message_base.md#variable-m-name)**  |


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

Callback function executed when message received. 

**Parameters**: 

  * **from** [MessageBase](Classes/class_message_base.md) that sent message. 
  * **data** Message data. 


**Reimplements**: [MessageBase::MessageCallback](Classes/class_message_base.md#function-messagecallback)


### function getInstance

```cpp
static inline ErrorMgrSingleton & getInstance()
```


-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800