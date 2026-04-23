---
title: General API Utility Functions
summary: This group of functions is provided for general API utilities, such as printing to stdout, performing basic math functions, and identifying basic OpenVSP information. Click here to return to the main page. 

---

# General API Utility Functions

This group of functions is provided for general API utilities, such as printing to stdout, performing basic math functions, and identifying basic OpenVSP information. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[VSPCheckSetup](Modules/group___a_p_i_utilities.md#function-vspchecksetup)**() |
| void | **[VSPRenew](Modules/group___a_p_i_utilities.md#function-vsprenew)**() |
| std::string | **[GetVSPVersion](Modules/group___a_p_i_utilities.md#function-getvspversion)**() |
| int | **[GetVSPVersionMajor](Modules/group___a_p_i_utilities.md#function-getvspversionmajor)**() |
| int | **[GetVSPVersionMinor](Modules/group___a_p_i_utilities.md#function-getvspversionminor)**() |
| int | **[GetVSPVersionChange](Modules/group___a_p_i_utilities.md#function-getvspversionchange)**() |
| std::string | **[GetVSPExePath](Modules/group___a_p_i_utilities.md#function-getvspexepath)**() |
| bool | **[SetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-setvspaeropath)**(const std::string & path) |
| std::string | **[GetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-getvspaeropath)**() |
| bool | **[CheckForVSPAERO](Modules/group___a_p_i_utilities.md#function-checkforvspaero)**(const std::string & path) |
| bool | **[SetVSPHelpPath](Modules/group___a_p_i_utilities.md#function-setvsphelppath)**(const std::string & path) |
| std::string | **[GetVSPHelpPath](Modules/group___a_p_i_utilities.md#function-getvsphelppath)**() |
| bool | **[CheckForVSPHelp](Modules/group___a_p_i_utilities.md#function-checkforvsphelp)**(const std::string & path) |


## Functions Documentation

### function VSPCheckSetup

```
void VSPCheckSetup()
```


Check if OpenVSP has been initialized successfully. If not, the OpenVSP instance will be exited. This call should be placed at the beginning of all API scripts. 

VSPCheckSetup();

// Continue to do things...
```

 

VSPCheckSetup()

# Continue to do things...
```

  


### function VSPRenew

```
void VSPRenew()
```


Clear and reinitialize OpenVSP to all default settings 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

SetParmVal( pod_id, "Y_Rel_Location", "XForm", 2.0 );

VSPRenew();

if ( FindGeoms().size() != 0 ) { Print( "ERROR: VSPRenew" ); }
```

 

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

SetParmVal( pod_id, "Y_Rel_Location", "XForm", 2.0 )

VSPRenew()

if  len(FindGeoms()) != 0 : print( "ERROR: VSPRenew" )
```

  


### function GetVSPVersion

```
std::string GetVSPVersion()
```


**Return**: OpenVSP version string (i.e. "OpenVSP 3.17.1") 

Get the version of the OpenVSP instance currently running 

Print( "The current OpenVSP version is: ", false );

Print( GetVSPVersion() );
```

 

print( "The current OpenVSP version is: ", False )

print( GetVSPVersion() )
```

  


### function GetVSPVersionMajor

```
int GetVSPVersionMajor()
```


**Return**: OpenVSP major version number (i.e. 3 in 3.X.Y) 

Get the major version of the OpenVSP instance currently running as an integer 

Print( "The current OpenVSP version is: ", false );

int major = GetVSPVersionMajor();
int minor = GetVSPVersionMinor();
int change = GetVSPVersionChange();

Print( formatInt(major) + "." + formatInt(minor) + "." + formatInt(change) );
```

 

print( "The current OpenVSP version is: ", False )

major = GetVSPVersionMajor()
minor = GetVSPVersionMinor()
change = GetVSPVersionChange()

print( f"{major}.{minor}.{change}" )
```

  


### function GetVSPVersionMinor

```
int GetVSPVersionMinor()
```


**Return**: OpenVSP minor version number (i.e. X in 3.X.Y) 

Get the minor version of the OpenVSP instance currently running as an integer 

Print( "The current OpenVSP version is: ", false );

int major = GetVSPVersionMajor();
int minor = GetVSPVersionMinor();
int change = GetVSPVersionChange();

Print( formatInt(major) + "." + formatInt(minor) + "." + formatInt(change) );
```

 

print( "The current OpenVSP version is: ", False )

major = GetVSPVersionMajor()
minor = GetVSPVersionMinor()
change = GetVSPVersionChange()

print( f"{major}.{minor}.{change}" )
```

  


### function GetVSPVersionChange

```
int GetVSPVersionChange()
```


**Return**: OpenVSP change version number (i.e. Y in 3.X.Y) 

Get the change version of the OpenVSP instance currently running as an integer 

Print( "The current OpenVSP version is: ", false );

int major = GetVSPVersionMajor();
int minor = GetVSPVersionMinor();
int change = GetVSPVersionChange();

Print( formatInt(major) + "." + formatInt(minor) + "." + formatInt(change) );
```

 

print( "The current OpenVSP version is: ", False )

major = GetVSPVersionMajor()
minor = GetVSPVersionMinor()
change = GetVSPVersionChange()

print( f"{major}.{minor}.{change}" )
```

  


### function GetVSPExePath

```
std::string GetVSPExePath()
```


**See**: [SetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-setvspaeropath), [CheckForVSPAERO](Modules/group___a_p_i_utilities.md#function-checkforvspaero), [GetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-getvspaeropath)

**Return**: Path to the OpenVSP executable 

Get the path to the OpenVSP executable. OpenVSP will assume that the VSPAERO, VSPSLICER, and VSPVIEWER are in the same directory unless instructed otherwise. 

Print( "The current VSP executable path is: ", false );

Print( GetVSPExePath() );
```

 

print( "The current VSP executable path is: ", False )

print( GetVSPExePath() )
```

  


### function SetVSPAEROPath

```
bool SetVSPAEROPath(
    const std::string & path
)
```


**Parameters**: 

  * **path** Absolute path to directory containing VSPAERO executable 


**See**: [GetVSPExePath](Modules/group___a_p_i_utilities.md#function-getvspexepath), [CheckForVSPAERO](Modules/group___a_p_i_utilities.md#function-checkforvspaero), [GetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-getvspaeropath)

**Return**: Flag that indicates whether or not the path was set correctly 

Set the path to the VSPAERO executables (Solver, Viewer, and Slicer). By default, OpenVSP will assume that the VSPAERO executables are in the same directory as the VSP executable. However, this may need to be changed when using certain API languages like MATLAB and Python. For example, Python may treat the location of the Python executable as the VSP executable path, so either the VSPAERO executable needs to be moved to the same directory or this function can be called to tell Python where to look for VSPAERO. 

if ( !CheckForVSPAERO( GetVSPExePath() ) )
{
    string vspaero_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5";
    SetVSPAEROPath( vspaero_path );
}
```

 

if  not CheckForVSPAERO( GetVSPExePath() ) :
    vspaero_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5"
    SetVSPAEROPath( vspaero_path )
```

  


### function GetVSPAEROPath

```
std::string GetVSPAEROPath()
```


**See**: [GetVSPExePath](Modules/group___a_p_i_utilities.md#function-getvspexepath), [CheckForVSPAERO](Modules/group___a_p_i_utilities.md#function-checkforvspaero), [SetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-setvspaeropath)

**Return**: Path OpenVSP will look for VSPAERO 

Get the path that OpenVSP will use to look for all VSPAERO executables (Solver, Slicer, and Viewer) when attempting to execute VSPAERO. If the VSPAERO executables are not in this location, they must either be copied there or the VSPAERO path must be set using SetVSPAEROPath. 

if ( !CheckForVSPAERO( GetVSPAEROPath() ) )
{
    Print( "VSPAERO is not where OpenVSP thinks it is. I should move the VSPAERO executable or call SetVSPAEROPath." );
}
```

 

if  not CheckForVSPAERO( GetVSPAEROPath() ) :
    print( "VSPAERO is not where OpenVSP thinks it is. I should move the VSPAERO executable or call SetVSPAEROPath." )
```

  


### function CheckForVSPAERO

```
bool CheckForVSPAERO(
    const std::string & path
)
```


**Parameters**: 

  * **path** Absolute path to check for VSPAERO executables 


**See**: [GetVSPExePath](Modules/group___a_p_i_utilities.md#function-getvspexepath), [GetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-getvspaeropath), [SetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-setvspaeropath)

**Return**: Flag that indicates if all VSPAERO executables are found or not 

Check if all VSPAERO executables (Solver, Viewer, and Slicer) are in a given directory. Note that this function will return false if only one or two VSPAERO executables are found. An error message will indicate the executables that are missing. This may be acceptable, as only the Solver is needed in all cases. The Viewer and Slicer may not be needed. 

string vspaero_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5";

if ( CheckForVSPAERO( vspaero_path ) )
{
    SetVSPAEROPath( vspaero_path );
}
```

 

vspaero_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5"

if  CheckForVSPAERO( vspaero_path ) :
    SetVSPAEROPath( vspaero_path )
```

  


### function SetVSPHelpPath

```
bool SetVSPHelpPath(
    const std::string & path
)
```


**Parameters**: 

  * **path** Absolute path to directory containing OpenVSP help files 


**See**: [GetVSPExePath](Modules/group___a_p_i_utilities.md#function-getvspexepath), [CheckForVSPHelp](Modules/group___a_p_i_utilities.md#function-checkforvsphelp), [GetVSPHelpPath](Modules/group___a_p_i_utilities.md#function-getvsphelppath)

**Return**: Flag that indicates whether or not the path was set correctly 

Set the path to the OpenVSP help files. By default, OpenVSP will assume that the OpenVSP help directory is in the same directory as the VSP executable. However, this may need to be changed when using certain API languages like MATLAB and Python. For example, Python may treat the location of the Python executable as the VSP executable path, so either the VSPAERO executable needs to be moved to the same directory or this function can be called to tell Python where to look for help. 

if ( !CheckForVSPHelp( GetVSPExePath() ) )
{
    string vsphelp_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5/help";
    SetVSPHelpPath( vsphelp_path );
}
```

 

if  not CheckForVSPHelp( GetVSPExePath() ) :
    vsphelp_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5/help"
    SetVSPHelpPath( vsphelp_path )
```

  


### function GetVSPHelpPath

```
std::string GetVSPHelpPath()
```


**See**: [GetVSPExePath](Modules/group___a_p_i_utilities.md#function-getvspexepath), [CheckForVSPHelp](Modules/group___a_p_i_utilities.md#function-checkforvsphelp), [SetVSPHelpPath](Modules/group___a_p_i_utilities.md#function-setvsphelppath)

**Return**: Path OpenVSP will look for help files 

Get the path that OpenVSP will use to look for all OpenVSP help files. If the OpenVSP help files are not in this location, they must either be copied there or the VSPHelp path must be set using SetVSPHelpPath. 

if ( !CheckForVSPHelp( GetVSPHelpPath() ) )
{
    Print( "VSPAERO is not where OpenVSP thinks it is. I should move the VSPAERO executable or call SetVSPAEROPath." );
}
```

 

if  not CheckForVSPHelp( GetVSPHelpPath() ) :
    print( "VSPAERO is not where OpenVSP thinks it is. I should move the VSPAERO executable or call SetVSPAEROPath." )
```

  


### function CheckForVSPHelp

```
bool CheckForVSPHelp(
    const std::string & path
)
```


**Parameters**: 

  * **path** Absolute path to check for VSPAERO executables 


**See**: [GetVSPExePath](Modules/group___a_p_i_utilities.md#function-getvspexepath), [GetVSPAEROPath](Modules/group___a_p_i_utilities.md#function-getvspaeropath), [SetVSPHelpPath](Modules/group___a_p_i_utilities.md#function-setvsphelppath)

**Return**: Flag that indicates if OpenVSP help files are found or not 

Check if all OpenVSP help files are in a given directory. 

string vsphelp_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5/help";

if ( CheckForVSPHelp( vsphelp_path ) )
{
    SetVSPHelpPath( vsphelp_path );
}
```

 

vsphelp_path = "C:/Users/example_user/Documents/OpenVSP_3.4.5/help"

if  CheckForVSPHelp( vsphelp_path ) :
    SetVSPHelpPath( vsphelp_path )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800