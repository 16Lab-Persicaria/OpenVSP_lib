---
title: vsp::UpdateCountMgrSingleton

---

# vsp::UpdateCountMgrSingleton






`#include <APIUpdateCountMgr.h>`

Inherits from [MessageBase](Classes/class_message_base.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| unsigned long | **[GetUpdateCount](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-getupdatecount)**() |
| void | **[ResetUpdateCount](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-resetupdatecount)**() |
| unsigned long | **[GetAndResetUpdateCount](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-getandresetupdatecount)**() |
| virtual void | **[MessageCallback](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-messagecallback)**(const [MessageBase](Classes/class_message_base.md) * from, const [MessageData](Classes/class_message_data.md) & data)<br>Callback function executed when message received.  |
| UpdateCountMgrSingleton & | **[getInstance](Classes/classvsp_1_1_update_count_mgr_singleton.md#function-getinstance)**() |

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

Callback function executed when message received. 

**Parameters**: 

  * **from** [MessageBase](Classes/class_message_base.md) that sent message. 
  * **data** Message data. 


**Reimplements**: [MessageBase::MessageCallback](Classes/class_message_base.md#function-messagecallback)


### function getInstance

```cpp
static inline UpdateCountMgrSingleton & getInstance()
```


-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800