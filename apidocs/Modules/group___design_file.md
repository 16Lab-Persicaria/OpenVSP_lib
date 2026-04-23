---
title: Design File Functions
summary: This group of functions is available for managing Design Variables through the API. Click here to return to the main page. 

---

# Design File Functions

This group of functions is available for managing Design Variables through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[ReadApplyDESFile](Modules/group___design_file.md#function-readapplydesfile)**(const std::string & file_name) |
| void | **[WriteDESFile](Modules/group___design_file.md#function-writedesfile)**(const std::string & file_name) |
| void | **[ReadApplyXDDMFile](Modules/group___design_file.md#function-readapplyxddmfile)**(const std::string & file_name) |
| void | **[WriteXDDMFile](Modules/group___design_file.md#function-writexddmfile)**(const std::string & file_name) |
| int | **[GetNumDesignVars](Modules/group___design_file.md#function-getnumdesignvars)**() |
| void | **[AddDesignVar](Modules/group___design_file.md#function-adddesignvar)**(const std::string & parm_id, int type) |
| void | **[DeleteAllDesignVars](Modules/group___design_file.md#function-deletealldesignvars)**() |
| std::string | **[GetDesignVar](Modules/group___design_file.md#function-getdesignvar)**(int index) |
| int | **[GetDesignVarType](Modules/group___design_file.md#function-getdesignvartype)**(int index) |


## Functions Documentation

### function ReadApplyDESFile

```
void ReadApplyDESFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** *.des input file 


Read in and apply a design file (*.des) to the current OpenVSP project 


### function WriteDESFile

```
void WriteDESFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** *.des output file 


Write all design variables to a design file (*.des) 


### function ReadApplyXDDMFile

```
void ReadApplyXDDMFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** *.xddm input file 


Read in and apply a Cart3D XDDM file (*.xddm) to the current OpenVSP project 


### function WriteXDDMFile

```
void WriteXDDMFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** *.xddm output file 


Write all design variables to a Cart3D XDDM file (*.xddm) 


### function GetNumDesignVars

```
int GetNumDesignVars()
```


**Return**: int Number of design variables 

Get the number of design variables 


### function AddDesignVar

```
void AddDesignVar(
    const std::string & parm_id,
    int type
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **type** XDDM type enum (XDDM_VAR or XDDM_CONST) 


**See**: [XDDM_QUANTITY_TYPE](Modules/group___enumerations.md#enum-xddm-quantity-type)

Add a design variable 


### function DeleteAllDesignVars

```
void DeleteAllDesignVars()
```


Delete all design variables 


### function GetDesignVar

```
std::string GetDesignVar(
    int index
)
```


**Parameters**: 

  * **index** Index of design variable 


**Return**: Parm ID 

Get the Parm ID of the specified design variable 


### function GetDesignVarType

```
int GetDesignVarType(
    int index
)
```


**Parameters**: 

  * **index** Index of design variable 


**See**: [XDDM_QUANTITY_TYPE](Modules/group___enumerations.md#enum-xddm-quantity-type)

**Return**: XDDM type enum (XDDM_VAR or XDDM_CONST) 

Get the XDDM type of the specified design variable 






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800