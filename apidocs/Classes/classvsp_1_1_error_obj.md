---
title: vsp::ErrorObj

---

# vsp::ErrorObj

**Module:** **[API Error Functions](Modules/group___a_p_i_error.md)**



 [More...](#detailed-description)


`#include <APIErrorMgr.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[ErrorObj](Classes/classvsp_1_1_error_obj.md#function-errorobj)**() |
| | **[ErrorObj](Classes/classvsp_1_1_error_obj.md#function-errorobj)**([ERROR_CODE](Modules/group___enumerations.md#enum-error-code) err_code, const string & err_str) |
| | **[ErrorObj](Classes/classvsp_1_1_error_obj.md#function-errorobj)**(const ErrorObj & from) |
| | **[~ErrorObj](Classes/classvsp_1_1_error_obj.md#function-~errorobj)**() |
| void | **[NoError](Classes/classvsp_1_1_error_obj.md#function-noerror)**() |

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| [ERROR_CODE](Modules/group___enumerations.md#enum-error-code) | **[m_ErrorCode](Classes/classvsp_1_1_error_obj.md#variable-m-errorcode)**  |
| string | **[m_ErrorString](Classes/classvsp_1_1_error_obj.md#variable-m-errorstring)**  |

## Detailed Description

```cpp
class vsp::ErrorObj;
```


[ErrorObj](Classes/classvsp_1_1_error_obj.md) is defined by an error code enum and associated error string. 

## Public Functions Documentation

### function ErrorObj

```cpp
ErrorObj()
```


### function ErrorObj

```cpp
ErrorObj(
    ERROR_CODE err_code,
    const string & err_str
)
```


### function ErrorObj

```cpp
ErrorObj(
    const ErrorObj & from
)
```


### function ~ErrorObj

```cpp
inline ~ErrorObj()
```


### function NoError

```cpp
inline void NoError()
```


## Public Attributes Documentation

### variable m_ErrorCode

```cpp
ERROR_CODE m_ErrorCode;
```


### variable m_ErrorString

```cpp
string m_ErrorString;
```


-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800