---
title: Vehicle Functions
summary: The Vehicle group of functions are high-level commands that pertain to the entire OpenVSP model. Click here to return to the main page. 

---

# Vehicle Functions

The Vehicle group of functions are high-level commands that pertain to the entire OpenVSP model. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[Update](Modules/group___vehicle.md#function-update)**(bool update_managers =true) |
| void | **[VSPExit](Modules/group___vehicle.md#function-vspexit)**(int error_code) |
| void | **[VSPCrash](Modules/group___vehicle.md#function-vspcrash)**(int crash_type) |
| int | **[GetAndResetUpdateCount](Modules/group___vehicle.md#function-getandresetupdatecount)**() |
| std::string | **[GetVSPFileName](Modules/group___vehicle.md#function-getvspfilename)**() |
| void | **[ClearVSPModel](Modules/group___vehicle.md#function-clearvspmodel)**() |


## Functions Documentation

### function Update

```
void Update(
    bool update_managers =true
)
```


**Parameters**: 

  * **update_managers** Flag to indicate if managers should be updated 


Update the entire vehicle and all lower level children. An input, which is true by default, is available to specify if managers should be updated as well. The managers are typically updated by their respective GUI, so must be updated through the API as well to avoid unexpected behavior. 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string xsec_surf = GetXSecSurf( fid, 0 );           // Get First (and Only) XSec Surf

int num_xsecs = GetNumXSec( xsec_surf );

//==== Set Tan Angles At Nose/Tail
SetXSecTanAngles( GetXSec( xsec_surf, 0 ), XSEC_BOTH_SIDES, 90 );
SetXSecTanAngles( GetXSec( xsec_surf, num_xsecs - 1 ), XSEC_BOTH_SIDES, -90 );

Update();       // Force Surface Update
```

 \endforcpponly \beginPythonOnly ```py

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

xsec_surf = GetXSecSurf( fid, 0 )           # Get First (and Only) XSec Surf

num_xsecs = GetNumXSec( xsec_surf )

#==== Set Tan Angles At Nose/Tail
SetXSecTanAngles( GetXSec( xsec_surf, 0 ), XSEC_BOTH_SIDES, 90, -1.0e12, -1.0e12, -1.0e12 )
SetXSecTanAngles( GetXSec( xsec_surf, num_xsecs - 1 ), XSEC_BOTH_SIDES, -90, -1.0e12, -1.0e12, -1.0e12 )

Update()       # Force Surface Update
```

  


### function VSPExit

```
void VSPExit(
    int error_code
)
```


**Parameters**: 

  * **error_code** Error code 


Exit the program with a specific error code 


### function VSPCrash

```
void VSPCrash(
    int crash_type
)
```


**Parameters**: 

  * **crash_type** int Type of crash to attempt. 


Cause OpenVSP to crash in a variety of ways. 


### function GetAndResetUpdateCount

```
int GetAndResetUpdateCount()
```


**Return**: int OpenVSP update count 

Return the OpenVSP update count and also reset it to zero.

The OpenVSP update count tracks how many times the GUI has been told to update screens (set to dirty). It provides a simple means of testing whether the OpenVSP state has possibly changed (non-zero returned).


### function GetVSPFileName

```
std::string GetVSPFileName()
```


**Return**: File name for the current OpenVSP project 

Get the file name of the current OpenVSP project 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string fname = "example_fuse.vsp3";

SetVSP3FileName( fname );

Update();

//==== Save Vehicle to File ====//
Print( "\tSaving vehicle file to: ", false );

Print( fname );

WriteVSPFile( GetVSPFileName(), SET_ALL );
```

 \endforcpponly \beginPythonOnly ```py

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

fname = "example_fuse.vsp3"

SetVSP3FileName( fname )

Update()

#==== Save Vehicle to File ====//
print( "\tSaving vehicle file to: ", False )

print( fname )

WriteVSPFile( GetVSPFileName(), SET_ALL )
```

  


### function ClearVSPModel

```
void ClearVSPModel()
```


Clear the current OpenVSP model 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

//==== Reset Geometry ====//
Print( string( "--->Resetting VSP model to blank slate\n" ) );
ClearVSPModel();
```

 \endforcpponly \beginPythonOnly ```py

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

#==== Reset Geometry ====//
print( "--->Resetting VSP model to blank slate\n" )
ClearVSPModel()
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800