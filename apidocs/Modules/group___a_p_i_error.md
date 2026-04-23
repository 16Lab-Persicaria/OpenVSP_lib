---
title: API Error Functions
summary: Handling of OpenVSP ErrorObj information is accomplished through this group of API functions. Click here to return to the main page. 

---

# API Error Functions

Handling of OpenVSP ErrorObj information is accomplished through this group of API functions. Click here to return to the main page. 

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[vsp::ErrorObj](Classes/classvsp_1_1_error_obj.md)**  |

## Functions

|                | Name           |
| -------------- | -------------- |
| ERROR_CODE | **[GetErrorCode](Modules/group___a_p_i_error.md#function-geterrorcode)**() |
| string | **[GetErrorString](Modules/group___a_p_i_error.md#function-geterrorstring)**() |
| bool | **[GetErrorLastCallFlag](Modules/group___a_p_i_error.md#function-geterrorlastcallflag)**() |
| int | **[GetNumTotalErrors](Modules/group___a_p_i_error.md#function-getnumtotalerrors)**() |
| ErrorObj | **[PopLastError](Modules/group___a_p_i_error.md#function-poplasterror)**() |
| ErrorObj | **[GetLastError](Modules/group___a_p_i_error.md#function-getlasterror)**() |
| void | **[SilenceErrors](Modules/group___a_p_i_error.md#function-silenceerrors)**() |
| void | **[PrintOnErrors](Modules/group___a_p_i_error.md#function-printonerrors)**() |


## Functions Documentation

### function GetErrorCode

```
inline ERROR_CODE GetErrorCode()
```


**See**: [ERROR_CODE](Modules/group___enumerations.md#enum-error-code)

**Return**: [ERROR_CODE](Modules/group___enumerations.md#enum-error-code) error code enum 

Get the [ERROR_CODE](Modules/group___enumerations.md#enum-error-code) enum of the last raised error 

ErrorObj err = PopLastError();

if ( err.GetErrorCode() != VSP_CANT_FIND_PARM )            { Print( "---> Error: API PopLast" ); }
```

 \endforcpponly \beginPythonOnly ```py

    ErrorObj err = PopLastError()

if  err.GetErrorCode() != VSP_CANT_FIND_PARM : Print( "---> Error: API PopLast" ); }
```

  


### function GetErrorString

```
inline string GetErrorString()
```


**Return**: Error string 

Get the error string of the last raised error 

//==== Check For API Errors ====//
while ( GetNumTotalErrors() > 0 )
{
    ErrorObj err = PopLastError();
    Print( err.GetErrorString() );
}
```

 \endforcpponly \beginPythonOnly ```py

    #==== Check For API Errors ====//
while  GetNumTotalErrors() > 0 :
    ErrorObj err = PopLastError()
    Print( err.GetErrorString() )
```

  


### function GetErrorLastCallFlag

```
bool GetErrorLastCallFlag()
```


**Return**: False if no error, true otherwise 

Check if there was an error on the last call to the API 

//==== Force API to silence error messages ====//
SilenceErrors();

//==== Bogus Call To Create API Error ====//
Print( string( "---> Test Error Handling" ) );

SetParmVal( "BogusParmID", 23.0 );

if ( !GetErrorLastCallFlag() )                        { Print( "---> Error: API GetErrorLastCallFlag " ); }

//==== Tell API to print error messages ====//
PrintOnErrors();
```

 \endforcpponly \beginPythonOnly ```py

    #==== Force API to silence error messages ====//
SilenceErrors()

#==== Bogus Call To Create API Error ====//
Print( string( "---> Test Error Handling" ) )

SetParmVal( "BogusParmID", 23.0 )

if  not GetErrorLastCallFlag() : Print( "---> Error: API GetErrorLastCallFlag " ); }

#==== Tell API to print error messages ====//
PrintOnErrors()
```

  


### function GetNumTotalErrors

```
int GetNumTotalErrors()
```


**Return**: Number of errors 

Count the total number of errors on the stack 

//==== Force API to silence error messages ====//
SilenceErrors();

Print( "Creating an API error" );
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 );

//==== Check For API Errors ====//
while ( GetNumTotalErrors() > 0 )
{
    ErrorObj err = PopLastError();
    Print( err.GetErrorString() );
}

//==== Tell API to print error messages ====//
PrintOnErrors();
```

 \endforcpponly \beginPythonOnly ```py

    #==== Force API to silence error messages ====//
SilenceErrors()

Print( "Creating an API error" )
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 )

#==== Check For API Errors ====//
while  GetNumTotalErrors() > 0 :
    ErrorObj err = PopLastError()
    Print( err.GetErrorString() )

#==== Tell API to print error messages ====//
PrintOnErrors()
```

  


### function PopLastError

```
ErrorObj PopLastError()
```


**Return**: Error object 

Pop (remove) and return the most recent error from the stack. Note, errors are printed on occurrence by default. 

//==== Force API to silence error messages ====//
SilenceErrors();

Print( "Creating an API error" );
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 );

//==== Check For API Errors ====//
while ( GetNumTotalErrors() > 0 )
{
    ErrorObj err = PopLastError();
    Print( err.GetErrorString() );
}

//==== Tell API to print error messages ====//
PrintOnErrors();
```

 \endforcpponly \beginPythonOnly ```py

    #==== Force API to silence error messages ====//
SilenceErrors()

Print( "Creating an API error" )
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 )

#==== Check For API Errors ====//
while  GetNumTotalErrors() > 0 :
    ErrorObj err = PopLastError()
    Print( err.GetErrorString() )

#==== Tell API to print error messages ====//
PrintOnErrors()
```

  


### function GetLastError

```
ErrorObj GetLastError()
```


**See**: [SilenceErrors](Modules/group___a_p_i_error.md#function-silenceerrors), [PrintOnErrors](Modules/group___a_p_i_error.md#function-printonerrors); 

**Return**: Error object 

Return the most recent error from the stack (does NOT pop error off the stack) 

//==== Force API to silence error messages ====//
SilenceErrors();

Print( "Creating an API error" );
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 );

//==== Check For API Errors ====//
ErrorObj err = GetLastError();

Print( err.GetErrorString() );

//==== Tell API to print error messages ====//
PrintOnErrors();
```

 \endforcpponly \beginPythonOnly ```py

    #==== Force API to silence error messages ====//
SilenceErrors()

Print( "Creating an API error" )
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 )

#==== Check For API Errors ====//
ErrorObj err = GetLastError()

Print( err.GetErrorString() )

#==== Tell API to print error messages ====//
PrintOnErrors()
```

  


### function SilenceErrors

```
inline void SilenceErrors()
```


**See**: [PrintOnErrors](Modules/group___a_p_i_error.md#function-printonerrors)

Prevent errors from printing to stdout as they occur. 

//==== Force API to silence error messages ====//
SilenceErrors();

Print( "Creating an API error" );
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 );

//==== Tell API to print error messages ====//
PrintOnErrors();
```

 \endforcpponly \beginPythonOnly ```py

    #==== Force API to silence error messages ====//
SilenceErrors()

Print( "Creating an API error" )
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 )

#==== Tell API to print error messages ====//
PrintOnErrors()
```

  


### function PrintOnErrors

```
inline void PrintOnErrors()
```


**See**: [SilenceErrors](Modules/group___a_p_i_error.md#function-silenceerrors)

Cause errors to be printed to stdout as they occur. 

//==== Force API to silence error messages ====//
SilenceErrors();

Print( "Creating an API error" );
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 );

//==== Tell API to print error messages ====//
PrintOnErrors();
```

 \endforcpponly \beginPythonOnly ```py

    #==== Force API to silence error messages ====//
SilenceErrors()

Print( "Creating an API error" )
SetParmVal( "ABCDEFG", "Test_Name", "Test_Group", 123.4 )

#==== Tell API to print error messages ====//
PrintOnErrors()
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800