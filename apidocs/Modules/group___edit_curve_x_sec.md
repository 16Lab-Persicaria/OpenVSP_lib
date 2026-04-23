---
title: Edit Curve XSec Functions
summary: Functions for modifying XSecs of type XS_EDIT_CURVE are defined here. Click here to return to the main page. 

---

# Edit Curve XSec Functions

Functions for modifying XSecs of type XS_EDIT_CURVE are defined here. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[EditXSecInitShape](Modules/group___edit_curve_x_sec.md#function-editxsecinitshape)**(const std::string & xsec_id) |
| void | **[EditXSecConvertTo](Modules/group___edit_curve_x_sec.md#function-editxsecconvertto)**(const std::string & xsec_id, const int & newtype) |
| std::vector< double > | **[GetEditXSecUVec](Modules/group___edit_curve_x_sec.md#function-geteditxsecuvec)**(const std::string & xsec_id) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetEditXSecCtrlVec](Modules/group___edit_curve_x_sec.md#function-geteditxsecctrlvec)**(const std::string & xsec_id, bool non_dimensional =true) |
| void | **[SetEditXSecPnts](Modules/group___edit_curve_x_sec.md#function-seteditxsecpnts)**(const std::string & xsec_id, const std::vector< double > & u_vec, const std::vector< [vec3d](Classes/classvec3d.md) > & control_pts, const std::vector< double > & r_vec) |
| void | **[EditXSecDelPnt](Modules/group___edit_curve_x_sec.md#function-editxsecdelpnt)**(const std::string & xsec_id, const int & indx) |
| int | **[EditXSecSplit01](Modules/group___edit_curve_x_sec.md#function-editxsecsplit01)**(const std::string & xsec_id, const double & u) |
| void | **[MoveEditXSecPnt](Modules/group___edit_curve_x_sec.md#function-moveeditxsecpnt)**(const std::string & xsec_id, const int & indx, const [vec3d](Classes/classvec3d.md) & new_pnt) |
| void | **[ConvertXSecToEdit](Modules/group___edit_curve_x_sec.md#function-convertxsectoedit)**(const std::string & geom_id, const int & indx =0) |
| std::vector< bool > | **[GetEditXSecFixedUVec](Modules/group___edit_curve_x_sec.md#function-geteditxsecfixeduvec)**(const std::string & xsec_id) |
| void | **[SetEditXSecFixedUVec](Modules/group___edit_curve_x_sec.md#function-seteditxsecfixeduvec)**(const std::string & xsec_id, std::vector< bool > fixed_u_vec) |
| void | **[ReparameterizeEditXSec](Modules/group___edit_curve_x_sec.md#function-reparameterizeeditxsec)**(const std::string & xsec_id) |


## Functions Documentation

### function EditXSecInitShape

```
void EditXSecInitShape(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [INIT_EDIT_XSEC_TYPE](Modules/group___enumerations.md#enum-init-edit-xsec-type)

Initialize the EditCurveXSec to the current value of m_ShapeType (i.e. EDIT_XSEC_ELLIPSE) 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

// Set XSec 2 to linear
EditXSecConvertTo( xsec_2, LINEAR );

EditXSecInitShape( xsec_2 ); // Change back to default ellipse
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

# Set XSec 2 to linear
EditXSecConvertTo( xsec_2, LINEAR )

EditXSecInitShape( xsec_2 ) # Change back to default ellipse
```

  


### function EditXSecConvertTo

```
void EditXSecConvertTo(
    const std::string & xsec_id,
    const int & newtype
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **newtype** New curve type enum (i.e. CEDIT) 


**See**: [PCURV_TYPE](Modules/group___enumerations.md#enum-pcurv-type)

Convert the EditCurveXSec curve type to the specified new type. Note, EditCurveXSec uses the same enumerations for PCurve to identify curve type, but APPROX_CEDIT is not supported at this time. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Set XSec 1 to Linear
EditXSecConvertTo( xsec_1, LINEAR );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Set XSec 1 to Linear
EditXSecConvertTo( xsec_1, LINEAR )
```

  


### function GetEditXSecUVec

```
std::vector< double > GetEditXSecUVec(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**Return**: Array of U parameter values 

Get the U parameter vector for an EditCurveXSec. The vector will be in increasing order with a range of 0 - 1. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

// Set XSec 2 to linear
EditXSecConvertTo( xsec_2, LINEAR );

array < double > u_vec = GetEditXSecUVec( xsec_2 );

if ( u_vec[1] - 0.25 > 1e-6 )
{
    Print( "Error: GetEditXSecUVec" );
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

# Set XSec 2 to linear
EditXSecConvertTo( xsec_2, LINEAR )

u_vec = GetEditXSecUVec( xsec_2 )

if  u_vec[1] - 0.25 > 1e-6 :
    print( "Error: GetEditXSecUVec" )
```

  


### function GetEditXSecCtrlVec

```
std::vector< vec3d > GetEditXSecCtrlVec(
    const std::string & xsec_id,
    bool non_dimensional =true
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **non_dimensional** True to get the points non-dimensionalized, False to get them scaled by m_Width and m_Height 


**Return**: Array of control points 

Get the control point vector for an EditCurveXSec. Note, the returned array of [vec3d](Classes/classvec3d.md) values will be represented in 2D with Z set to 0. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Get the control points for the default shape
array < vec3d > xsec1_pts = GetEditXSecCtrlVec( xsec_1, true ); // The returned control points will not be scaled by width and height

Print( "Normalized Bottom Point of XSecCurve: " + xsec1_pts[3].x() + ", " + xsec1_pts[3].y() + ", " + xsec1_pts[3].z() );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Get the control points for the default shape
xsec1_pts = GetEditXSecCtrlVec( xsec_1, True ) # The returned control points will not be scaled by width and height

print( f"Normalized Bottom Point of XSecCurve: {xsec1_pts[3].x()}, {xsec1_pts[3].y()}, {xsec1_pts[3].z()}" )
```

  


### function SetEditXSecPnts

```
void SetEditXSecPnts(
    const std::string & xsec_id,
    const std::vector< double > & u_vec,
    const std::vector< vec3d > & control_pts,
    const std::vector< double > & r_vec
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **u_vec** Array of U parameter values 
  * **r_vec** Array of R parameter values 
  * **control_pts** Nondimensionalized array of control points 


Set the U parameter vector and the control point vector for an EditCurveXSec. The arrays must be of equal length, with the values for U defined in increasing order and range 0 - 1. The input control points to SetEditXSecPnts must be nondimensionalized in the approximate range of [-0.5, 0.5]. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

// Set XSec 2 to linear
EditXSecConvertTo( xsec_2, LINEAR );

// Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_2, "SymType"), SYM_NONE );

// Define a square
array < vec3d > xsec2_pts(5);

xsec2_pts[0] = vec3d( 0.5, 0.5, 0.0 );
xsec2_pts[1] = vec3d( 0.5, -0.5, 0.0 );
xsec2_pts[2] = vec3d( -0.5, -0.5, 0.0 );
xsec2_pts[3] = vec3d( -0.5, 0.5, 0.0 );
xsec2_pts[4] = vec3d( 0.5, 0.5, 0.0 );

// u vec must start at 0.0 and end at 1.0
array < double > u_vec(5);

u_vec[0] = 0.0;
u_vec[1] = 0.25;
u_vec[2] = 0.5;
u_vec[3] = 0.75;
u_vec[4] = 1.0;

array < double > r_vec(5);

r_vec[0] = 0.0;
r_vec[1] = 0.0;
r_vec[2] = 0.0;
r_vec[3] = 0.0;
r_vec[4] = 0.0;

SetEditXSecPnts( xsec_2, u_vec, xsec2_pts, r_vec ); // Note: points are unscaled by the width and height parms

array < vec3d > new_pnts = GetEditXSecCtrlVec( xsec_2, true ); // The returned control points will not be scaled by width and height

if ( dist( new_pnts[3], xsec2_pts[3] ) > 1e-6 )
{
    Print( "Error: SetEditXSecPnts");
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

# Set XSec 2 to linear
EditXSecConvertTo( xsec_2, LINEAR )

# Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_2, "SymType"), SYM_NONE )

# Define a square
xsec2_pts = [vec3d(0.5, 0.5, 0.0),
         vec3d(0.5, -0.5, 0.0),
         vec3d(-0.5, -0.5, 0.0),
         vec3d(-0.5, 0.5, 0.0),
         vec3d(0.5, 0.5, 0.0)]

# u vec must start at 0.0 and end at 1.0
u_vec = [0.0, 0.25, 0.5, 0.75, 1.0]

r_vec = [0.0, 0.0, 0.0, 0.0, 0.0]

SetEditXSecPnts( xsec_2, u_vec, xsec2_pts, r_vec ) # Note: points are unscaled by the width and height parms

new_pnts = GetEditXSecCtrlVec( xsec_2, True ) # The returned control points will not be scaled by width and height

if  dist( new_pnts[3], xsec2_pts[3] ) > 1e-6 :
    print( "Error: SetEditXSecPnts")
```

  


### function EditXSecDelPnt

```
void EditXSecDelPnt(
    const std::string & xsec_id,
    const int & indx
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **indx** Control point index 


Delete an EditCurveXSec control point. Note, cubic Bezier intermediate control points (those not on the curve) cannot be deleted. The previous and next Bezier control point will be deleted along with the point on the curve. Regardless of curve type, the first and last points may not be deleted. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

// Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_2, "SymType"), SYM_NONE );

array < vec3d > old_pnts = GetEditXSecCtrlVec( xsec_2, true ); // The returned control points will not be scaled by width and height

EditXSecDelPnt( xsec_2, 3 ); // Remove control point at bottom of circle

array < vec3d > new_pnts = GetEditXSecCtrlVec( xsec_2, true ); // The returned control points will not be scaled by width and height

if ( old_pnts.size() - new_pnts.size() != 3  )
{
    Print( "Error: EditXSecDelPnt");
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

# Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_2, "SymType"), SYM_NONE )

old_pnts = GetEditXSecCtrlVec( xsec_2, True ) # The returned control points will not be scaled by width and height

EditXSecDelPnt( xsec_2, 3 ) # Remove control point at bottom of circle

new_pnts = GetEditXSecCtrlVec( xsec_2, True ) # The returned control points will not be scaled by width and height

if  len(old_pnts) - len(new_pnts) != 3  :
    print( "Error: EditXSecDelPnt")
```

  


### function EditXSecSplit01

```
int EditXSecSplit01(
    const std::string & xsec_id,
    const double & u
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **u** U value to split the curve at (0 - 1) 


**Return**: Index of the point added from the split 

Split the EditCurveXSec at the specified U value 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

// Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_2, "SymType"), SYM_NONE );

array < vec3d > old_pnts = GetEditXSecCtrlVec( xsec_2, true ); // The returned control points will not be scaled by width and height

int new_pnt_ind = EditXSecSplit01( xsec_2, 0.375 );

array < vec3d > new_pnts = GetEditXSecCtrlVec( xsec_2, true ); // The returned control points will not be scaled by width and height

if ( new_pnts.size() - old_pnts.size() != 3  )
{
    Print( "Error: EditXSecSplit01");
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 2, XS_EDIT_CURVE )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

# Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_2, "SymType"), SYM_NONE )

old_pnts = GetEditXSecCtrlVec( xsec_2, True ) # The returned control points will not be scaled by width and height

new_pnt_ind = EditXSecSplit01( xsec_2, 0.375 )

new_pnts = GetEditXSecCtrlVec( xsec_2, True ) # The returned control points will not be scaled by width and height

if  len(new_pnts) - len(old_pnts) != 3  :
    print( "Error: EditXSecSplit01")
```

  


### function MoveEditXSecPnt

```
void MoveEditXSecPnt(
    const std::string & xsec_id,
    const int & indx,
    const vec3d & new_pnt
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **indx** Control point index 
  * **new_pnt** Coordinate of the new point 


Move an EditCurveXSec control point. The XSec points are nondimensionalized by m_Width and m_Height and defined in 2D, so the Z value of the new coordinate point will be ignored. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_1, "SymType"), SYM_NONE );

// Get the control points for the default shape
array < vec3d > xsec1_pts = GetEditXSecCtrlVec( xsec_1, true ); // The returned control points will not be scaled by width and height

// Identify a control point that lies on the curve and shift it in Y
int move_pnt_ind = 3;

vec3d new_pnt = vec3d( xsec1_pts[move_pnt_ind].x(), 2 * xsec1_pts[move_pnt_ind].y(), 0.0 );

// Move the control point
MoveEditXSecPnt( xsec_1, move_pnt_ind, new_pnt );

array < vec3d > new_pnts = GetEditXSecCtrlVec( xsec_1, true ); // The returned control points will not be scaled by width and height

if ( dist( new_pnt, new_pnts[move_pnt_ind] ) > 1e-6 )
{
    Print( "Error: MoveEditXSecPnt" );
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Turn off R/L symmetry
SetParmVal( GetXSecParm( xsec_1, "SymType"), SYM_NONE )

# Get the control points for the default shape
xsec1_pts = GetEditXSecCtrlVec( xsec_1, True ) # The returned control points will not be scaled by width and height

# Identify a control point that lies on the curve and shift it in Y
move_pnt_ind = 3

new_pnt = vec3d( xsec1_pts[move_pnt_ind].x(), 2 * xsec1_pts[move_pnt_ind].y(), 0.0 )

# Move the control point
MoveEditXSecPnt( xsec_1, move_pnt_ind, new_pnt )

new_pnts = GetEditXSecCtrlVec( xsec_1, True ) # The returned control points will not be scaled by width and height

if  dist( new_pnt, new_pnts[move_pnt_ind] ) > 1e-6 :
    print( "Error: MoveEditXSecPnt" )
```

  


### function ConvertXSecToEdit

```
void ConvertXSecToEdit(
    const std::string & geom_id,
    const int & indx =0
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **indx** XSec index 


Convert any XSec type into an EditCurveXSec. This function will work for BOR Geoms, in which case the input XSec index is ignored. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_ROUNDED_RECTANGLE );

// Convert Rounded Rectangle to Edit Curve type XSec
ConvertXSecToEdit( sid, 1 );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Get the control points for the default shape
array < vec3d > xsec1_pts = GetEditXSecCtrlVec( xsec_1, true ); // The returned control points will not be scaled by width and height
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_ROUNDED_RECTANGLE )

# Convert Rounded Rectangle to Edit Curve type XSec
ConvertXSecToEdit( sid, 1 )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Get the control points for the default shape
xsec1_pts = GetEditXSecCtrlVec( xsec_1, True ) # The returned control points will not be scaled by width and height
```

  


### function GetEditXSecFixedUVec

```
std::vector< bool > GetEditXSecFixedUVec(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [SetEditXSecFixedUVec](Modules/group___edit_curve_x_sec.md#function-seteditxsecfixeduvec), [ReparameterizeEditXSec](Modules/group___edit_curve_x_sec.md#function-reparameterizeeditxsec)

**Return**: Array of bool values for each control point 

Get the vector of fixed U flags for each control point in an EditCurveXSec. The fixed U flag is used to hold the U parameter of the control point constant when performing an equal arc length reparameterization of the curve. 

// Add Wing
string wid = AddGeom( "WING" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( wid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

array < bool > @ fixed_u_vec = GetEditXSecFixedUVec( xsec_1 );

fixed_u_vec[3] = true; // change a flag

SetEditXSecFixedUVec( xsec_1, fixed_u_vec );

ReparameterizeEditXSec( xsec_1 );
```

 

# Add Wing
wid = AddGeom( "WING" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( wid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

fixed_u_vec = list(GetEditXSecFixedUVec( xsec_1 ))

fixed_u_vec[3] = True # change a flag

SetEditXSecFixedUVec( xsec_1, fixed_u_vec )

ReparameterizeEditXSec( xsec_1 )
```

  


### function SetEditXSecFixedUVec

```
void SetEditXSecFixedUVec(
    const std::string & xsec_id,
    std::vector< bool > fixed_u_vec
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **fixed_u_vec** Array of fixed U flags 


**See**: [GetEditXSecFixedUVec](Modules/group___edit_curve_x_sec.md#function-geteditxsecfixeduvec), [ReparameterizeEditXSec](Modules/group___edit_curve_x_sec.md#function-reparameterizeeditxsec)

Set the vector of fixed U flags for each control point in an EditCurveXSec. The fixed U flag is used to hold the U parameter of the control point constant when performing an equal arc length reparameterization of the curve. 

// Add Wing
string wid = AddGeom( "WING" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( wid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

array < bool > @ fixed_u_vec = GetEditXSecFixedUVec( xsec_1 );

fixed_u_vec[3] = true; // change a flag

SetEditXSecFixedUVec( xsec_1, fixed_u_vec );

ReparameterizeEditXSec( xsec_1 );
```

 

# Add Wing
wid = AddGeom( "WING" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( wid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

fixed_u_vec = list(GetEditXSecFixedUVec( xsec_1 ))

fixed_u_vec[3] = True # change a flag

SetEditXSecFixedUVec( xsec_1, fixed_u_vec )

ReparameterizeEditXSec( xsec_1 )
```

  


### function ReparameterizeEditXSec

```
void ReparameterizeEditXSec(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [SetEditXSecFixedUVec](Modules/group___edit_curve_x_sec.md#function-seteditxsecfixeduvec), [GetEditXSecFixedUVec](Modules/group___edit_curve_x_sec.md#function-geteditxsecfixeduvec)

Perform an equal arc length repareterization on an EditCurveXSec. The reparameterization is performed between specific U values if the Fixed U flag is true. This allows corners, such as at 0.25, 0.5, and 0.75 U, to be held constant while everything between them is reparameterized. 

// Add Wing
string wid = AddGeom( "WING" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( wid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

array < bool > @ fixed_u_vec = GetEditXSecFixedUVec( xsec_1 );

fixed_u_vec[3] = true; // change a flag

SetEditXSecFixedUVec( xsec_1, fixed_u_vec );

ReparameterizeEditXSec( xsec_1 );
```

 

# Add Wing
wid = AddGeom( "WING" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( wid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

fixed_u_vec = list(GetEditXSecFixedUVec( xsec_1 ))

fixed_u_vec[3] = True # change a flag

SetEditXSecFixedUVec( xsec_1, fixed_u_vec )

ReparameterizeEditXSec( xsec_1 )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800