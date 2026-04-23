---
title: D:/RSWdev/godot-cpp-template/external/geom_api/APIErrorMgr.h

---

# D:/RSWdev/godot-cpp-template/external/geom_api/APIErrorMgr.h



## Namespaces

| Name           |
| -------------- |
| **[vsp](Namespaces/namespacevsp.md)**  |

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[vsp::ErrorObj](Classes/classvsp_1_1_error_obj.md)**  |
| class | **[vsp::ErrorMgrSingleton](Classes/classvsp_1_1_error_mgr_singleton.md)**  |

## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[ErrorMgr](Files/_a_p_i_error_mgr_8h.md#define-errormgr)**  |




## Macros Documentation

### define ErrorMgr

```cpp
#define ErrorMgr ErrorMgrSingleton::getInstance()
```


## Source code

```cpp
//
// This file is released under the terms of the NASA Open Source Agreement (NOSA)
// version 1.3 as detailed in the LICENSE file which accompanies this software.
//

// API.h: interface for the Vehicle Class and Vehicle Mgr Singleton.
// J.R Gloudemans
//

#if !defined(APIERRORMGR__INCLUDED_)
#define APIERRORMGR__INCLUDED_

#ifdef SWIG
%feature("autodoc", 1);
%feature("doxygen:ignore:forcpponly", range="end");
%feature("doxygen:ignore:beginPythonOnly", range="end:endPythonOnly", contents="parse");
#endif

#include "APIDefines.h"
#include "MessageMgr.h"

#include <string>
#include <stack>
#include <vector>

using std::string;
using std::stack;
using std::vector;

class Vehicle;

namespace vsp
{


//======================== Error Object ================================//
class ErrorObj
{
public:
    ErrorObj();
    ErrorObj( ERROR_CODE err_code, const string & err_str );
    ErrorObj( const ErrorObj& from );
    ~ErrorObj()         {}


    ERROR_CODE GetErrorCode()

    {
        return m_ErrorCode;
    }

    string GetErrorString()

    {
        return m_ErrorString;
    }

    ERROR_CODE m_ErrorCode;
    string m_ErrorString;

    void NoError()
    {
        m_ErrorCode = VSP_OK;
        m_ErrorString = "No Error";
    }
};


//======================== Error Mgr ================================//
class ErrorMgrSingleton : public MessageBase
{
public:


    bool GetErrorLastCallFlag();                // Did the last call have an error?


    int  GetNumTotalErrors();                   // Total number of errors on stack


    ErrorObj PopLastError();                    // Pop last error off stack


    ErrorObj GetLastError();                    // Get last error but leave on stack

    bool PopErrorAndPrint( FILE* stream );      // Check for error, pop and print to stream


    void SilenceErrors()    { m_PrintErrors = false; };


    void PrintOnErrors()    { m_PrintErrors = true; };


    void AddError( ERROR_CODE code, const string & desc );
    void NoError();

    virtual void MessageCallback( const MessageBase* from, const MessageData& data );

    static ErrorMgrSingleton& getInstance()
    {
        static ErrorMgrSingleton instance;
        return instance;
    }

private:

    bool m_PrintErrors;
    bool m_ErrorLastCallFlag;
    stack< ErrorObj > m_ErrorStack;

    ErrorMgrSingleton();
    ~ErrorMgrSingleton();
    ErrorMgrSingleton( ErrorMgrSingleton const& copy ) = delete;          // Not Implemented
    ErrorMgrSingleton& operator=( ErrorMgrSingleton const& copy ) = delete; // Not Implemented
};

#define ErrorMgr ErrorMgrSingleton::getInstance()

}

#endif // !defined(APIERRORMGR__INCLUDED_)
```


-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800
