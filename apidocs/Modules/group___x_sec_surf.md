---
title: XSecSurf Functions
summary: This group of API functions provides capabilities related to the XSecSurf class in OpenVSP. Click here to return to the main page. 

---

# XSecSurf Functions

This group of API functions provides capabilities related to the XSecSurf class in OpenVSP. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| int | **[GetNumXSecSurfs](Modules/group___x_sec_surf.md#function-getnumxsecsurfs)**(const std::string & geom_id) |
| std::string | **[GetXSecSurf](Modules/group___x_sec_surf.md#function-getxsecsurf)**(const std::string & geom_id, int index) |
| int | **[GetNumXSec](Modules/group___x_sec_surf.md#function-getnumxsec)**(const std::string & xsec_surf_id) |
| std::string | **[GetXSec](Modules/group___x_sec_surf.md#function-getxsec)**(const std::string & xsec_surf_id, int xsec_index) |
| void | **[ChangeXSecShape](Modules/group___x_sec_surf.md#function-changexsecshape)**(const std::string & xsec_surf_id, int xsec_index, int type) |
| void | **[SetXSecSurfGlobalXForm](Modules/group___x_sec_surf.md#function-setxsecsurfglobalxform)**(const std::string & xsec_surf_id, const [Matrix4d](Classes/class_matrix4d.md) & mat) |
| [Matrix4d](Classes/class_matrix4d.md) | **[GetXSecSurfGlobalXForm](Modules/group___x_sec_surf.md#function-getxsecsurfglobalxform)**(const std::string & xsec_surf_id) |


## Functions Documentation

### function GetNumXSecSurfs

```
int GetNumXSecSurfs(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: int Number of XSecSurfs 

Get the number of XSecSurfs for the specified Geom 

//==== Add Fuselage Geometry ====//
string fuseid = AddGeom( "FUSELAGE", "" );

int num_xsec_surfs = GetNumXSecSurfs( fuseid );

if ( num_xsec_surfs != 1 )                { Print( "---> Error: API GetNumXSecSurfs  " ); }
```

 

#==== Add Fuselage Geometry ====//
fuseid = AddGeom( "FUSELAGE", "" )

num_xsec_surfs = GetNumXSecSurfs( fuseid )

if  num_xsec_surfs != 1 : print( "---> Error: API GetNumXSecSurfs  " )
```

  


### function GetXSecSurf

```
std::string GetXSecSurf(
    const std::string & geom_id,
    int index
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **index** XSecSurf index 


**Return**: XSecSurf ID 

Get the XSecSurf ID for a particular Geom and XSecSurf index 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )
```

  


### function GetNumXSec

```
int GetNumXSec(
    const std::string & xsec_surf_id
)
```


**Parameters**: 

  * **xsec_surf_id** XSecSurf ID 


**Return**: Number of XSecs 

Get number of XSecs in an XSecSurf 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Flatten ends
int num_xsecs = GetNumXSec( xsec_surf );

for ( int i = 0 ; i < num_xsecs ; i++ )
{
    string xsec = GetXSec( xsec_surf, i );

    SetXSecTanAngles( xsec, XSEC_BOTH_SIDES, 0 );       // Set Tangent Angles At Cross Section

    SetXSecTanStrengths( xsec, XSEC_BOTH_SIDES, 0.0 );  // Set Tangent Strengths At Cross Section
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Flatten ends
num_xsecs = GetNumXSec( xsec_surf )

for i in range(num_xsecs):

    xsec = GetXSec( xsec_surf, i )

    SetXSecTanAngles( xsec, XSEC_BOTH_SIDES, 0, -1.0e12, -1.0e12, -1.0e12 )       # Set Tangent Angles At Cross Section

    SetXSecTanStrengths( xsec, XSEC_BOTH_SIDES, 0.0, -1.0e12, -1.0e12, -1.0e12 )  # Set Tangent Strengths At Cross Section
```

  


### function GetXSec

```
std::string GetXSec(
    const std::string & xsec_surf_id,
    int xsec_index
)
```


**Parameters**: 

  * **xsec_surf_id** XSecSurf ID 
  * **xsec_index** Xsec index 


**Return**: Xsec ID 

Get Xsec ID for a particular XSecSurf at given index 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )
```

  


### function ChangeXSecShape

```
void ChangeXSecShape(
    const std::string & xsec_surf_id,
    int xsec_index,
    int type
)
```


**Parameters**: 

  * **xsec_surf_id** XSecSurf ID 
  * **xsec_index** Xsec index 
  * **type** Xsec type enum (i.e. XS_ELLIPSE) 


**See**: [XSEC_CRV_TYPE](Modules/group___enumerations.md#enum-xsec-crv-type)

Change the shape of a particular XSec, identified by an XSecSurf ID and XSec index 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Set XSec 1 & 2 to Edit Curve type
ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );
ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE );

string xsec_2 = GetXSec( xsec_surf, 2 );

if ( GetXSecShape( xsec_2 ) != XS_EDIT_CURVE )
{
    Print( "Error: ChangeXSecShape" );
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Set XSec 1 & 2 to Edit Curve type
ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )
ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE )

xsec_2 = GetXSec( xsec_surf, 2 )

if  GetXSecShape( xsec_2 ) != XS_EDIT_CURVE :
    print( "Error: ChangeXSecShape" )
```

  


### function SetXSecSurfGlobalXForm

```
void SetXSecSurfGlobalXForm(
    const std::string & xsec_surf_id,
    const Matrix4d & mat
)
```


**Parameters**: 

  * **xsec_surf_id** XSecSurf ID 
  * **mat** Transformation matrix 


Set the global surface transform matrix for given XSecSurf 


### function GetXSecSurfGlobalXForm

```
Matrix4d GetXSecSurfGlobalXForm(
    const std::string & xsec_surf_id
)
```


**Parameters**: 

  * **xsec_surf_id** XSecSurf ID 


**Return**: Transformation matrix 

Get the global surface transform matrix for given XSecSurf 






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800