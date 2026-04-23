---
title: XSec and Airfoil Functions
summary: This group of functions provides API control of cross-sections (XSecs). Airfoils are a type of XSec included in this group as well. API functions for Body of Revolution XSecs are included in the Specialized Geometry group. Click here to return to the main page. 

---

# XSec and Airfoil Functions

This group of functions provides API control of cross-sections (XSecs). Airfoils are a type of XSec included in this group as well. API functions for Body of Revolution XSecs are included in the Specialized Geometry group. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[SetXSecAlias](Modules/group___x_sec.md#function-setxsecalias)**(const string & id, const string & alias) |
| string | **[GetXSecAlias](Modules/group___x_sec.md#function-getxsecalias)**(const string & id) |
| void | **[SetXSecCurveAlias](Modules/group___x_sec.md#function-setxseccurvealias)**(const string & id, const string & alias) |
| string | **[GetXSecCurveAlias](Modules/group___x_sec.md#function-getxseccurvealias)**(const string & id) |
| void | **[CutXSec](Modules/group___x_sec.md#function-cutxsec)**(const std::string & geom_id, int index) |
| void | **[CopyXSec](Modules/group___x_sec.md#function-copyxsec)**(const std::string & geom_id, int index) |
| void | **[PasteXSec](Modules/group___x_sec.md#function-pastexsec)**(const std::string & geom_id, int index) |
| void | **[InsertXSec](Modules/group___x_sec.md#function-insertxsec)**(const std::string & geom_id, int index, int type) |
| int | **[GetXSecShape](Modules/group___x_sec.md#function-getxsecshape)**(const std::string & xsec_id) |
| double | **[GetXSecWidth](Modules/group___x_sec.md#function-getxsecwidth)**(const std::string & xsec_id) |
| double | **[GetXSecHeight](Modules/group___x_sec.md#function-getxsecheight)**(const std::string & xsec_id) |
| void | **[SetXSecWidthHeight](Modules/group___x_sec.md#function-setxsecwidthheight)**(const std::string & xsec_id, double w, double h) |
| void | **[SetXSecWidth](Modules/group___x_sec.md#function-setxsecwidth)**(const std::string & xsec_id, double w) |
| void | **[SetXSecHeight](Modules/group___x_sec.md#function-setxsecheight)**(const std::string & xsec_id, double h) |
| std::vector< std::string > | **[GetXSecParmIDs](Modules/group___x_sec.md#function-getxsecparmids)**(const std::string & xsec_id) |
| std::string | **[GetXSecParm](Modules/group___x_sec.md#function-getxsecparm)**(const std::string & xsec_id, const std::string & name) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[ReadFileXSec](Modules/group___x_sec.md#function-readfilexsec)**(const std::string & xsec_id, const std::string & file_name) |
| void | **[SetXSecPnts](Modules/group___x_sec.md#function-setxsecpnts)**(const std::string & xsec_id, std::vector< [vec3d](Classes/classvec3d.md) > & pnt_vec) |
| [vec3d](Classes/classvec3d.md) | **[ComputeXSecPnt](Modules/group___x_sec.md#function-computexsecpnt)**(const std::string & xsec_id, double fract) |
| [vec3d](Classes/classvec3d.md) | **[ComputeXSecTan](Modules/group___x_sec.md#function-computexsectan)**(const std::string & xsec_id, double fract) |
| void | **[ResetXSecSkinParms](Modules/group___x_sec.md#function-resetxsecskinparms)**(const std::string & xsec_id) |
| void | **[SetXSecContinuity](Modules/group___x_sec.md#function-setxseccontinuity)**(const std::string & xsec_id, int cx) |
| void | **[SetXSecTanAngles](Modules/group___x_sec.md#function-setxsectanangles)**(const std::string & xsec_id, int side, double top, double right, double bottom, double left) |
| void | **[SetXSecTanSlews](Modules/group___x_sec.md#function-setxsectanslews)**(const std::string & xsec_id, int side, double top, double right, double bottom, double left) |
| void | **[SetXSecTanStrengths](Modules/group___x_sec.md#function-setxsectanstrengths)**(const std::string & xsec_id, int side, double top, double right, double bottom, double left) |
| void | **[SetXSecCurvatures](Modules/group___x_sec.md#function-setxseccurvatures)**(const std::string & xsec_id, int side, double top, double right, double bottom, double left) |
| void | **[ReadFileAirfoil](Modules/group___x_sec.md#function-readfileairfoil)**(const std::string & xsec_id, const std::string & file_name) |
| void | **[SetAirfoilUpperPnts](Modules/group___x_sec.md#function-setairfoilupperpnts)**(const std::string & xsec_id, const std::vector< [vec3d](Classes/classvec3d.md) > & up_pnt_vec) |
| void | **[SetAirfoilLowerPnts](Modules/group___x_sec.md#function-setairfoillowerpnts)**(const std::string & xsec_id, const std::vector< [vec3d](Classes/classvec3d.md) > & low_pnt_vec) |
| void | **[SetAirfoilPnts](Modules/group___x_sec.md#function-setairfoilpnts)**(const std::string & xsec_id, const std::vector< [vec3d](Classes/classvec3d.md) > & up_pnt_vec, const std::vector< [vec3d](Classes/classvec3d.md) > & low_pnt_vec) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetHersheyBarLiftDist](Modules/group___x_sec.md#function-gethersheybarliftdist)**(const int & npts, const double & alpha, const double & Vinf, const double & span, bool full_span_flag =false) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetHersheyBarDragDist](Modules/group___x_sec.md#function-gethersheybardragdist)**(const int & npts, const double & alpha, const double & Vinf, const double & span, bool full_span_flag =false) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetVKTAirfoilPnts](Modules/group___x_sec.md#function-getvktairfoilpnts)**(const int & npts, const double & alpha, const double & epsilon, const double & kappa, const double & tau) |
| std::vector< double > | **[GetVKTAirfoilCpDist](Modules/group___x_sec.md#function-getvktairfoilcpdist)**(const double & alpha, const double & epsilon, const double & kappa, const double & tau, const std::vector< [vec3d](Classes/classvec3d.md) > & xyz_data) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetEllipsoidSurfPnts](Modules/group___x_sec.md#function-getellipsoidsurfpnts)**(const [vec3d](Classes/classvec3d.md) & center, const [vec3d](Classes/classvec3d.md) & abc_rad, int u_npts =20, int w_npts =20) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetFeatureLinePnts](Modules/group___x_sec.md#function-getfeaturelinepnts)**(const string & geom_id) |
| std::vector< double > | **[GetEllipsoidCpDist](Modules/group___x_sec.md#function-getellipsoidcpdist)**(const std::vector< [vec3d](Classes/classvec3d.md) > & surf_pnt_vec, const [vec3d](Classes/classvec3d.md) & abc_rad, const [vec3d](Classes/classvec3d.md) & V_inf) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetAirfoilUpperPnts](Modules/group___x_sec.md#function-getairfoilupperpnts)**(const std::string & xsec_id) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetAirfoilLowerPnts](Modules/group___x_sec.md#function-getairfoillowerpnts)**(const std::string & xsec_id) |
| std::vector< double > | **[GetUpperCSTCoefs](Modules/group___x_sec.md#function-getuppercstcoefs)**(const std::string & xsec_id) |
| std::vector< double > | **[GetLowerCSTCoefs](Modules/group___x_sec.md#function-getlowercstcoefs)**(const std::string & xsec_id) |
| int | **[GetUpperCSTDegree](Modules/group___x_sec.md#function-getuppercstdegree)**(const std::string & xsec_id) |
| int | **[GetLowerCSTDegree](Modules/group___x_sec.md#function-getlowercstdegree)**(const std::string & xsec_id) |
| void | **[SetUpperCST](Modules/group___x_sec.md#function-setuppercst)**(const std::string & xsec_id, int deg, const std::vector< double > & coefs) |
| void | **[SetLowerCST](Modules/group___x_sec.md#function-setlowercst)**(const std::string & xsec_id, int deg, const std::vector< double > & coefs) |
| void | **[PromoteCSTUpper](Modules/group___x_sec.md#function-promotecstupper)**(const std::string & xsec_id) |
| void | **[PromoteCSTLower](Modules/group___x_sec.md#function-promotecstlower)**(const std::string & xsec_id) |
| void | **[DemoteCSTUpper](Modules/group___x_sec.md#function-demotecstupper)**(const std::string & xsec_id) |
| void | **[DemoteCSTLower](Modules/group___x_sec.md#function-demotecstlower)**(const std::string & xsec_id) |
| void | **[FitAfCST](Modules/group___x_sec.md#function-fitafcst)**(const std::string & xsec_surf_id, int xsec_index, int deg) |
| void | **[WriteBezierAirfoil](Modules/group___x_sec.md#function-writebezierairfoil)**(const std::string & file_name, const std::string & geom_id, const double & foilsurf_u) |
| void | **[WriteSeligAirfoil](Modules/group___x_sec.md#function-writeseligairfoil)**(const std::string & file_name, const std::string & geom_id, const double & foilsurf_u) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetAirfoilCoordinates](Modules/group___x_sec.md#function-getairfoilcoordinates)**(const std::string & geom_id, const double & foilsurf_u) |


## Functions Documentation

### function SetXSecAlias

```
void SetXSecAlias(
    const string & id,
    const string & alias
)
```


**Parameters**: 

  * **id** XSec ID 
  * **alias** Xsec alias 


Set XSec Alias by ID 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Set Alias and verify alias match
string alias = "XSec_One_Alias";

SetXSecAlias( xsec_1, alias );

string get_alias = GetXSecAlias( xsec_1 );

if ( alias != get_alias )
{
    Print("SetXSecAlias/GetXSecAlias error!");
    __failure++;
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Set Alias and verify alias match
alias = "XSec_One_Alias"

SetXSecAlias( xsec_1, alias )

get_alias = GetXSecAlias( xsec_1 )

if alias != get_alias:
    print("SetXSecAlias/GetXSecAlias error!")
```

  


### function GetXSecAlias

```
string GetXSecAlias(
    const string & id
)
```


**Parameters**: 

  * **id** XSec ID 


**Return**: Xsec alias 

Get XSec Alias by ID 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Set Alias and verify alias match
string alias = "XSec_One_Alias";

SetXSecAlias( xsec_1, alias );

string get_alias = GetXSecAlias( xsec_1 );

if ( alias != get_alias )
{
    Print("SetXSecAlias/GetXSecAlias error!");
    __failure++;
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Set Alias and verify alias match
alias = "XSec_One_Alias"

SetXSecAlias( xsec_1, alias )

get_alias = GetXSecAlias( xsec_1 )

if alias != get_alias:
    print("SetXSecAlias/GetXSecAlias error!")
```

  


### function SetXSecCurveAlias

```
void SetXSecCurveAlias(
    const string & id,
    const string & alias
)
```


**Parameters**: 

  * **id** XSec ID 
  * **alias** XsecCurve alias 


Set XSecCurve Alias by XSec ID 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Set Alias and verify alias match
string alias = "XSecCurve_One_Alias";

SetXSecCurveAlias( xsec_1, alias );

string get_alias = GetXSecCurveAlias( xsec_1 );

if ( alias != get_alias )
{
    Print("SetXSecCurveAlias/GetXSecCurveAlias error!");
    __failure++;
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Set Alias and verify alias match
alias = "XSecCurve_One_Alias"

SetXSecCurveAlias( xsec_1, alias )

get_alias = GetXSecCurveAlias( xsec_1 )

if alias != get_alias:
    print("SetXSecCurveAlias/GetXSecCurveAlias error!")
```

  


### function GetXSecCurveAlias

```
string GetXSecCurveAlias(
    const string & id
)
```


**Parameters**: 

  * **id** XSec ID 


Get XSecCurve Alias by XSec ID 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 1
string xsec_1 = GetXSec( xsec_surf, 1 );

// Set Alias and verify alias match
string alias = "XSecCurve_One_Alias";

SetXSecCurveAlias( xsec_1, alias );

string get_alias = GetXSecCurveAlias( xsec_1 );

if ( alias != get_alias )
{
    Print("SetXSecCurveAlias/GetXSecCurveAlias error!");
    __failure++;
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 1
xsec_1 = GetXSec( xsec_surf, 1 )

# Set Alias and verify alias match
alias = "XSecCurve_One_Alias"

SetXSecCurveAlias( xsec_1, alias )

get_alias = GetXSecCurveAlias( xsec_1 )

if alias != get_alias:
    print("SetXSecCurveAlias/GetXSecCurveAlias error!")
```

  


### function CutXSec

```
void CutXSec(
    const std::string & geom_id,
    int index
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **index** XSec index 


**See**: [PasteXSec](Modules/group___x_sec.md#function-pastexsec)

Cut a cross-section from the specified geometry and maintain it in memory 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

//==== Insert, Cut, Paste Example ====//
InsertXSec( fid, 1, XS_ROUNDED_RECTANGLE );         // Insert A Cross-Section

CopyXSec( fid, 2 );                                 // Copy Just Created XSec To Clipboard

PasteXSec( fid, 1 );                                // Paste Clipboard

CutXSec( fid, 2 );                                  // Cut Created XSec
```

 

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

#==== Insert, Cut, Paste Example ====//
InsertXSec( fid, 1, XS_ROUNDED_RECTANGLE )         # Insert A Cross-Section

CopyXSec( fid, 2 )                                 # Copy Just Created XSec To Clipboard

PasteXSec( fid, 1 )                                # Paste Clipboard

CutXSec( fid, 2 )                                  # Cut Created XSec
```

  


### function CopyXSec

```
void CopyXSec(
    const std::string & geom_id,
    int index
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **index** XSec index 


**See**: [PasteXSec](Modules/group___x_sec.md#function-pastexsec)

Copy a cross-section from the specified geometry and maintain it in memory 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Copy XSec To Clipboard
CopyXSec( sid, 1 );

// Paste To XSec 3
PasteXSec( sid, 3 );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Copy XSec To Clipboard
CopyXSec( sid, 1 )

# Paste To XSec 3
PasteXSec( sid, 3 )
```

  


### function PasteXSec

```
void PasteXSec(
    const std::string & geom_id,
    int index
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **index** XSec index 


**See**: [CutXSec](Modules/group___x_sec.md#function-cutxsec), [CopyXSec](Modules/group___x_sec.md#function-copyxsec)

Paste the cross-section currently held in memory to the specified geometry 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Copy XSec To Clipboard
CopyXSec( sid, 1 );

// Paste To XSec 3
PasteXSec( sid, 3 );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Copy XSec To Clipboard
CopyXSec( sid, 1 )

# Paste To XSec 3
PasteXSec( sid, 3 )
```

  


### function InsertXSec

```
void InsertXSec(
    const std::string & geom_id,
    int index,
    int type
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **index** XSec index 
  * **type** XSec type enum (i.e. XS_GENERAL_FUSE) 


**See**: [XSEC_CRV_TYPE](Modules/group___enumerations.md#enum-xsec-crv-type)

Insert a cross-section of particular type to the specified geometry after the given index 

string wing_id = AddGeom( "WING" );

//===== Add XSec ====//
InsertXSec( wing_id, 1, XS_SIX_SERIES );
```

 

wing_id = AddGeom( "WING" )

#===== Add XSec ====//
InsertXSec( wing_id, 1, XS_SIX_SERIES )
```

  


### function GetXSecShape

```
int GetXSecShape(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [XSEC_CRV_TYPE](Modules/group___enumerations.md#enum-xsec-crv-type)

**Return**: XSec type enum (i.e. XS_ELLIPSE) 

Get the shape of an XSec 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE );

string xsec = GetXSec( xsec_surf, 1 );

if ( GetXSecShape( xsec ) != XS_EDIT_CURVE ) { Print( "ERROR: GetXSecShape" ); }
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_EDIT_CURVE )

xsec = GetXSec( xsec_surf, 1 )

if  GetXSecShape( xsec ) != XS_EDIT_CURVE : print( "ERROR: GetXSecShape" )
```

  


### function GetXSecWidth

```
double GetXSecWidth(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [SetXSecWidth](Modules/group___x_sec.md#function-setxsecwidth)

**Return**: Xsec width 

Get the width of an XSec. Note that POINT type XSecs have a width and height of 0, regardless of what width and height it is set to. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 2 ); // Get 2nd to last XSec

SetXSecWidthHeight( xsec, 3.0, 6.0 );

if ( abs( GetXSecWidth( xsec ) - 3.0 ) > 1e-6 )        { Print( "---> Error: API Get/Set Width " ); }
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 2 ) # Get 2nd to last XSec

SetXSecWidthHeight( xsec, 3.0, 6.0 )

if  abs( GetXSecWidth( xsec ) - 3.0 ) > 1e-6 : print( "---> Error: API Get/Set Width " )
```

  


### function GetXSecHeight

```
double GetXSecHeight(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [SetXSecHeight](Modules/group___x_sec.md#function-setxsecheight)

**Return**: Xsec height 

Get the height of an XSec. Note that POINT type XSecs have a width and height of 0, regardless of what width and height it is set to. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 2 ); // Get 2nd to last XSec

SetXSecWidthHeight( xsec, 3.0, 6.0 );

if ( abs( GetXSecHeight( xsec ) - 6.0 ) > 1e-6 )        { Print( "---> Error: API Get/Set Width " ); }
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 2 ) # Get 2nd to last XSec

SetXSecWidthHeight( xsec, 3.0, 6.0 )

if  abs( GetXSecHeight( xsec ) - 6.0 ) > 1e-6 : print( "---> Error: API Get/Set Width " )
```

  


### function SetXSecWidthHeight

```
void SetXSecWidthHeight(
    const std::string & xsec_id,
    double w,
    double h
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **w** Xsec width 
  * **h** Xsec height 


**See**: [SetXSecWidth](Modules/group___x_sec.md#function-setxsecwidth), [SetXSecHeight](Modules/group___x_sec.md#function-setxsecheight)

Set the width and height of an XSec. Note, if the XSec is an EDIT_CURVE type and PreserveARFlag is true, the input width value will be ignored and instead set from on the input height and aspect ratio. Use SetXSecWidth and SetXSecHeight directly to avoid this. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

SetXSecWidthHeight( xsec_2, 1.5, 1.5 );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

SetXSecWidthHeight( xsec_2, 1.5, 1.5 )
```

  


### function SetXSecWidth

```
void SetXSecWidth(
    const std::string & xsec_id,
    double w
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **w** Xsec width 


**See**: [GetXSecWidth](Modules/group___x_sec.md#function-getxsecwidth)

Set the width of an XSec. Note that POINT type XSecs have a width and height of 0, regardless of what is input to SetXSecWidth. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

SetXSecWidth( xsec_2, 1.5 );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

SetXSecWidth( xsec_2, 1.5 )
```

  


### function SetXSecHeight

```
void SetXSecHeight(
    const std::string & xsec_id,
    double h
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **h** Xsec height 


**See**: [GetXSecHeight](Modules/group___x_sec.md#function-getxsecheight)

Set the height of an XSec. Note that POINT type XSecs have a width and height of 0, regardless of what is input to SetXSecHeight. 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Identify XSec 2
string xsec_2 = GetXSec( xsec_surf, 2 );

SetXSecHeight( xsec_2, 1.5 );
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

# Identify XSec 2
xsec_2 = GetXSec( xsec_surf, 2 )

SetXSecHeight( xsec_2, 1.5 )
```

  


### function GetXSecParmIDs

```
std::vector< std::string > GetXSecParmIDs(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**Return**: Array of Parm IDs 

Get all Parm IDs for specified XSec Parm Container 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

array< string > @parm_array = GetXSecParmIDs( xsec );

if ( parm_array.size() < 1 )                        { Print( "---> Error: API GetXSecParmIDs " ); }
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

parm_array = GetXSecParmIDs( xsec )

if  len(parm_array) < 1 : print( "---> Error: API GetXSecParmIDs " )
```

  


### function GetXSecParm

```
std::string GetXSecParm(
    const std::string & xsec_id,
    const std::string & name
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **name** Parm name 


**Return**: Parm ID 

Get a specific Parm ID from an Xsec 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

if ( !ValidParm( wid ) )                            { Print( "---> Error: API GetXSecParm " ); }
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

if  not ValidParm( wid ) : print( "---> Error: API GetXSecParm " )
```

  


### function ReadFileXSec

```
std::vector< vec3d > ReadFileXSec(
    const std::string & xsec_id,
    const std::string & file_name
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **file_name** Fuselage XSec file name 


**Return**: Array of coordinate points read from the file and set to the XSec 

Read in XSec shape from fuselage (*.fsx) file and set to the specified XSec. The XSec must be of type XS_FILE_FUSE. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 2, XS_FILE_FUSE );

string xsec = GetXSec( xsec_surf, 2 );

array< vec3d > @vec_array = ReadFileXSec( xsec, "TestXSec.fxs" );
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 2, XS_FILE_FUSE )

xsec = GetXSec( xsec_surf, 2 )

vec_array = ReadFileXSec(xsec, "TestXSec.fxs")
```

  


### function SetXSecPnts

```
void SetXSecPnts(
    const std::string & xsec_id,
    std::vector< vec3d > & pnt_vec
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 
  * **pnt_vec** vector<vec3d> Vector of XSec coordinate points 


Set the coordinate points for a specific XSec. The XSec must be of type XS_FILE_FUSE. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 2, XS_FILE_FUSE );

string xsec = GetXSec( xsec_surf, 2 );

array< vec3d > @vec_array = ReadFileXSec( xsec, "TestXSec.fxs" );

if ( vec_array.size() > 0 )
{
    vec_array[1] = vec_array[1] * 2.0;
    vec_array[3] = vec_array[3] * 2.0;

    SetXSecPnts( xsec, vec_array );
}
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 2, XS_FILE_FUSE )

xsec = GetXSec( xsec_surf, 2 )

vec_array = ReadFileXSec(xsec, "TestXSec.fxs")


if  len(vec_array) > 0 :
    vec_array[1] = vec_array[1] * 2.0
    vec_array[3] = vec_array[3] * 2.0

    SetXSecPnts( xsec, vec_array )
```

  


### function ComputeXSecPnt

```
vec3d ComputeXSecPnt(
    const std::string & xsec_id,
    double fract
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 
  * **fract** double Curve parameter value (range: 0 - 1) 


**Return**: [vec3d](Classes/classvec3d.md) 3D coordinate point 

Compute 3D coordinate for a point on an XSec curve given the parameter value (U) along the curve 

//==== Add Geom ====//
string stack_id = AddGeom( "STACK" );

//==== Get The XSec Surf ====//
string xsec_surf = GetXSecSurf( stack_id, 0 );

string xsec = GetXSec( xsec_surf, 2 );

double u_fract = 0.25;

vec3d pnt = ComputeXSecPnt( xsec, u_fract );
```

 

#==== Add Geom ====//
stack_id = AddGeom( "STACK" )

#==== Get The XSec Surf ====//
xsec_surf = GetXSecSurf( stack_id, 0 )

xsec = GetXSec( xsec_surf, 2 )

u_fract = 0.25

pnt = ComputeXSecPnt(xsec, u_fract)
```

  


### function ComputeXSecTan

```
vec3d ComputeXSecTan(
    const std::string & xsec_id,
    double fract
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 
  * **fract** double Curve parameter value (range: 0 - 1) 


**Return**: [vec3d](Classes/classvec3d.md) Tangent vector 

Compute the tangent vector of a point on an XSec curve given the parameter value (U) along the curve 

//==== Add Geom ====//
string stack_id = AddGeom( "STACK" );

//==== Get The XSec Surf ====//
string xsec_surf = GetXSecSurf( stack_id, 0 );

string xsec = GetXSec( xsec_surf, 2 );

double u_fract = 0.25;

vec3d tan = ComputeXSecTan( xsec, u_fract );
```

 

#==== Add Geom ====//
stack_id = AddGeom( "STACK" )

#==== Get The XSec Surf ====//
xsec_surf = GetXSecSurf( stack_id, 0 )

xsec = GetXSec( xsec_surf, 2 )

u_fract = 0.25

tan = ComputeXSecTan( xsec, u_fract )
```

  


### function ResetXSecSkinParms

```
void ResetXSecSkinParms(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 


Reset all skinning Parms for a specified XSec. Set top, bottom, left, and right strengths, slew, angle, and curvature to 0. Set all symmetry and equality conditions to false. 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string xsec_surf = GetXSecSurf( fid, 0 );           // Get First (and Only) XSec Surf

int num_xsecs = GetNumXSec( xsec_surf );

string xsec = GetXSec( xsec_surf, 1 );

SetXSecTanAngles( xsec, XSEC_BOTH_SIDES, 0.0 );       // Set Tangent Angles At Cross Section
SetXSecContinuity( xsec, 1 );                       // Set Continuity At Cross Section

ResetXSecSkinParms( xsec );
```

 

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

xsec_surf = GetXSecSurf( fid, 0 )           # Get First (and Only) XSec Surf

num_xsecs = GetNumXSec( xsec_surf )

xsec = GetXSec( xsec_surf, 1 )

SetXSecTanAngles( xsec, XSEC_BOTH_SIDES, 0.0, -1.0e12, -1.0e12, -1.0e12 )       # Set Tangent Angles At Cross Section
SetXSecContinuity( xsec, 1 )                       # Set Continuity At Cross Section

ResetXSecSkinParms( xsec )
```

  


### function SetXSecContinuity

```
void SetXSecContinuity(
    const std::string & xsec_id,
    int cx
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 
  * **cx** int Continuity level (0, 1, or 2) 


Set C-type continuity enforcement for a particular XSec 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string xsec_surf = GetXSecSurf( fid, 0 );           // Get First (and Only) XSec Surf

int num_xsecs = GetNumXSec( xsec_surf );

for ( int i = 0 ; i < num_xsecs ; i++ )
{
    string xsec = GetXSec( xsec_surf, i );

    SetXSecContinuity( xsec, 1 );                       // Set Continuity At Cross Section
}
```

 

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

xsec_surf = GetXSecSurf( fid, 0 )           # Get First (and Only) XSec Surf

num_xsecs = GetNumXSec( xsec_surf )

for i in range(num_xsecs):

    xsec = GetXSec( xsec_surf, i )

    SetXSecContinuity( xsec, 1 )                       # Set Continuity At Cross Section
```

  


### function SetXSecTanAngles

```
void SetXSecTanAngles(
    const std::string & xsec_id,
    int side,
    double top,
    double right,
    double bottom,
    double left
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 
  * **side** int Side type enum (i.e. XSEC_BOTH_SIDES) 
  * **top** double Top angle (degrees) 
  * **right** double Right angle (degrees) 
  * **bottom** double Bottom angle (degrees) 
  * **left** double Left angle (degrees) 


**See**: [XSEC_SIDES_TYPE](Modules/group___enumerations.md#enum-xsec-sides-type)

Set the tangent angles for the specified XSec 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

int num_xsecs = GetNumXSec( xsec_surf );

for ( int i = 0 ; i < num_xsecs ; i++ )
{
    string xsec = GetXSec( xsec_surf, i );

    SetXSecTanAngles( xsec, XSEC_BOTH_SIDES, 10.0 );       // Set Tangent Angles At Cross Section
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

num_xsecs = GetNumXSec( xsec_surf )

for i in range(num_xsecs):

    xsec = GetXSec( xsec_surf, i )

    SetXSecTanAngles( xsec, XSEC_BOTH_SIDES, 10.0, -1.0e12, -1.0e12, -1.0e12 )       # Set Tangent Angles At Cross Section
```

  


### function SetXSecTanSlews

```
void SetXSecTanSlews(
    const std::string & xsec_id,
    int side,
    double top,
    double right,
    double bottom,
    double left
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **side** Side type enum (i.e. XSEC_BOTH_SIDES) 
  * **top** Top angle (degrees) 
  * **right** Right angle (degrees) 
  * **bottom** Bottom angle (degrees) 
  * **left** Left angle (degrees) 


**See**: [XSEC_SIDES_TYPE](Modules/group___enumerations.md#enum-xsec-sides-type)

Set the tangent slew angles for the specified XSec 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

int num_xsecs = GetNumXSec( xsec_surf );

for ( int i = 0 ; i < num_xsecs ; i++ )
{
    string xsec = GetXSec( xsec_surf, i );

    SetXSecTanSlews( xsec, XSEC_BOTH_SIDES, 5.0 );       // Set Tangent Slews At Cross Section
}
```

 

# Add Stack
sid = AddGeom( "STACK", "" )

# Get First (and Only) XSec Surf
xsec_surf = GetXSecSurf( sid, 0 )

num_xsecs = GetNumXSec( xsec_surf )

for i in range(num_xsecs):

    xsec = GetXSec( xsec_surf, i )

    SetXSecTanSlews( xsec, XSEC_BOTH_SIDES, 5.0, -1.0e12, -1.0e12, -1.0e12 )       # Set Tangent Slews At Cross Section
```

  


### function SetXSecTanStrengths

```
void SetXSecTanStrengths(
    const std::string & xsec_id,
    int side,
    double top,
    double right,
    double bottom,
    double left
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **side** Side type enum (i.e. XSEC_BOTH_SIDES) 
  * **top** Top strength 
  * **right** Right strength 
  * **bottom** Bottom strength 
  * **left** Left strength 


**See**: [XSEC_SIDES_TYPE](Modules/group___enumerations.md#enum-xsec-sides-type)

Set the tangent strengths for the specified XSec 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Flatten ends
int num_xsecs = GetNumXSec( xsec_surf );

for ( int i = 0 ; i < num_xsecs ; i++ )
{
    string xsec = GetXSec( xsec_surf, i );

    SetXSecTanStrengths( xsec, XSEC_BOTH_SIDES, 0.8 );  // Set Tangent Strengths At Cross Section
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

    SetXSecTanStrengths( xsec, XSEC_BOTH_SIDES, 0.8, -1.0e12, -1.0e12, -1.0e12 )  # Set Tangent Strengths At Cross Section
```

  


### function SetXSecCurvatures

```
void SetXSecCurvatures(
    const std::string & xsec_id,
    int side,
    double top,
    double right,
    double bottom,
    double left
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **side** Side type enum (i.e. XSEC_BOTH_SIDES) 
  * **top** Top curvature 
  * **right** Right curvature 
  * **bottom** Bottom curvature 
  * **left** Left curvature 


**See**: [XSEC_SIDES_TYPE](Modules/group___enumerations.md#enum-xsec-sides-type)

Set curvatures for the specified XSec 

// Add Stack
string sid = AddGeom( "STACK", "" );

// Get First (and Only) XSec Surf
string xsec_surf = GetXSecSurf( sid, 0 );

// Flatten ends
int num_xsecs = GetNumXSec( xsec_surf );

for ( int i = 0 ; i < num_xsecs ; i++ )
{
    string xsec = GetXSec( xsec_surf, i );

    SetXSecCurvatures( xsec, XSEC_BOTH_SIDES, 0.2 );  // Set Tangent Strengths At Cross Section
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

    SetXSecCurvatures( xsec, XSEC_BOTH_SIDES, 0.2, -1.0e12, -1.0e12, -1.0e12 )  # Set Tangent Strengths At Cross Section
```

  


### function ReadFileAirfoil

```
void ReadFileAirfoil(
    const std::string & xsec_id,
    const std::string & file_name
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **file_name** Airfoil XSec file name 


Read in XSec shape from airfoil file and set to the specified XSec. The XSec must be of type XS_FILE_AIRFOIL. Airfoil files may be in Lednicer or Selig format with *.af or *.dat extensions. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL );

string xsec = GetXSec( xsec_surf, 1 );

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" );
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL )

xsec = GetXSec( xsec_surf, 1 )

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" )
```

  


### function SetAirfoilUpperPnts

```
void SetAirfoilUpperPnts(
    const std::string & xsec_id,
    const std::vector< vec3d > & up_pnt_vec
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **up_pnt_vec** Array of points defining the upper surface of the airfoil 


Set the upper points for an airfoil. The XSec must be of type XS_FILE_AIRFOIL. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL );

string xsec = GetXSec( xsec_surf, 1 );

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" );

array< vec3d > @up_array = GetAirfoilUpperPnts( xsec );

for ( int i = 0 ; i < int( up_array.size() ) ; i++ )
{
    up_array[i].scale_y( 2.0 );
}

SetAirfoilUpperPnts( xsec, up_array );
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL )

xsec = GetXSec( xsec_surf, 1 )

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" )

up_array = GetAirfoilUpperPnts( xsec )

for i in range(int( len(up_array) )):

    up_array[i].scale_y( 2.0 )

SetAirfoilUpperPnts( xsec, up_array )
```

  


### function SetAirfoilLowerPnts

```
void SetAirfoilLowerPnts(
    const std::string & xsec_id,
    const std::vector< vec3d > & low_pnt_vec
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **low_pnt_vec** Array of points defining the lower surface of the airfoil 


Set the lower points for an airfoil. The XSec must be of type XS_FILE_AIRFOIL. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL );

string xsec = GetXSec( xsec_surf, 1 );

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" );

array< vec3d > @low_array = GetAirfoilLowerPnts( xsec );

for ( int i = 0 ; i < int( low_array.size() ) ; i++ )
{
    low_array[i].scale_y( 0.5 );
}

SetAirfoilUpperPnts( xsec, low_array );
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL )

xsec = GetXSec( xsec_surf, 1 )

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" )

low_array = GetAirfoilLowerPnts( xsec )

for i in range(int( len(low_array) )):

    low_array[i].scale_y( 0.5 )

SetAirfoilUpperPnts( xsec, low_array )
```

  


### function SetAirfoilPnts

```
void SetAirfoilPnts(
    const std::string & xsec_id,
    const std::vector< vec3d > & up_pnt_vec,
    const std::vector< vec3d > & low_pnt_vec
)
```


**Parameters**: 

  * **xsec_id** XSec ID 
  * **up_pnt_vec** Array of points defining the upper surface of the airfoil 
  * **low_pnt_vec** Array of points defining the lower surface of the airfoil 


Set the upper and lower points for an airfoil. The XSec must be of type XS_FILE_AIRFOIL. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL );

string xsec = GetXSec( xsec_surf, 1 );

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" );

array< vec3d > @up_array = GetAirfoilUpperPnts( xsec );

array< vec3d > @low_array = GetAirfoilLowerPnts( xsec );

for ( int i = 0 ; i < int( up_array.size() ) ; i++ )
{
    up_array[i].scale_y( 2.0 );

    low_array[i].scale_y( 0.5 );
}

SetAirfoilPnts( xsec, up_array, low_array );
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL )

xsec = GetXSec( xsec_surf, 1 )

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" )

up_array = GetAirfoilUpperPnts( xsec )

low_array = GetAirfoilLowerPnts( xsec )

for i in range(int( len(up_array) )):

    up_array[i].scale_y( 2.0 )

    low_array[i].scale_y( 0.5 )

SetAirfoilPnts( xsec, up_array, low_array )
```

  


### function GetHersheyBarLiftDist

```
std::vector< vec3d > GetHersheyBarLiftDist(
    const int & npts,
    const double & alpha,
    const double & Vinf,
    const double & span,
    bool full_span_flag =false
)
```


**Parameters**: 

  * **npts** Number of points along the span to assess 
  * **alpha** Wing angle of attack (Radians) 
  * **Vinf** Freestream velocity 
  * **span** Hershey Bar full-span. Note, only half is used in the calculation 
  * **full_span_flag** Flag to apply symmetry to results 


**Return**: Theoretical coefficient of lift distribution array (size = 2*npts if full_span_flag = true) 

Get the theoretical lift (Cl) distribution for a Hershey Bar wing with unit chord length using Glauert's Method. This function was initially created to compare VSPAERO results to Lifting Line Theory. If full_span_flag is set to true symmetry is applied to the results. 

// Compute theoretical lift and drag distributions using 100 points
double Vinf = 100;

double halfAR = 20;

double alpha_deg = 10;

int n_pts = 100;

array<vec3d> cl_dist_theo = GetHersheyBarLiftDist( int( n_pts ), Deg2Rad( alpha_deg ), Vinf, ( 2 * halfAR ), false );

array<vec3d> cd_dist_theo = GetHersheyBarDragDist( int( n_pts ), Deg2Rad( alpha_deg ), Vinf, ( 2 * halfAR ), false );
```

 

pi = 3.14159265358979323846
# Compute theoretical lift and drag distributions using 100 points
Vinf = 100

halfAR = 20

alpha_deg = 10

n_pts = 100

cl_dist_theo = GetHersheyBarLiftDist( int( n_pts ), alpha_deg*pi/180, Vinf, ( 2 * halfAR ), False )

cd_dist_theo = GetHersheyBarDragDist( int( n_pts ), alpha_deg*pi/180, Vinf, ( 2 * halfAR ), False )
```

  


### function GetHersheyBarDragDist

```
std::vector< vec3d > GetHersheyBarDragDist(
    const int & npts,
    const double & alpha,
    const double & Vinf,
    const double & span,
    bool full_span_flag =false
)
```


**Parameters**: 

  * **npts** Number of points along the span to assess 
  * **alpha** Wing angle of attack (Radians) 
  * **Vinf** Freestream velocity 
  * **span** Hershey Bar full-span. Note, only half is used in the calculation 
  * **full_span_flag** Flag to apply symmetry to results (default: false) 


**Return**: Theoretical coefficient of drag distribution array (size = 2*npts if full_span_flag = true) 

Get the theoretical drag (Cd) distribution for a Hershey Bar wing with unit chord length using Glauert's Method. This function was initially created to compare VSPAERO results to Lifting Line Theory. If full_span_flag is set to true symmetry is applied to the results. 

// Compute theoretical lift and drag distributions using 100 points
double Vinf = 100;

double halfAR = 20;

double alpha_deg = 10;

int n_pts = 100;

array<vec3d> cl_dist_theo = GetHersheyBarLiftDist( int( n_pts ), Deg2Rad( alpha_deg ), Vinf, ( 2 * halfAR ), false );

array<vec3d> cd_dist_theo = GetHersheyBarDragDist( int( n_pts ), Deg2Rad( alpha_deg ), Vinf, ( 2 * halfAR ), false );
```

 

pi = 3.14159265358979323846
# Compute theoretical lift and drag distributions using 100 points
Vinf = 100

halfAR = 20

alpha_deg = 10

n_pts = 100

cl_dist_theo = GetHersheyBarLiftDist( int( n_pts ), alpha_deg*pi/180, Vinf, ( 2 * halfAR ), False )

cd_dist_theo = GetHersheyBarDragDist( int( n_pts ), alpha_deg*pi/180, Vinf, ( 2 * halfAR ), False )
```

  


### function GetVKTAirfoilPnts

```
std::vector< vec3d > GetVKTAirfoilPnts(
    const int & npts,
    const double & alpha,
    const double & epsilon,
    const double & kappa,
    const double & tau
)
```


**Parameters**: 

  * **npts** Number of points along the airfoil to return 
  * **alpha** Airfoil angle of attack (Radians) 
  * **epsilon** Airfoil thickness 
  * **kappa** Airfoil camber 
  * **tau** Airfoil trailing edge angle (Radians) 


**Return**: Array of points on the VKT airfoil (size = npts) 

Get the 2D coordinates an input number of points along a Von K�rm�n-Trefftz airfoil of specified shape 

const double pi = 3.14159265358979323846;

const int npts = 122;

const double alpha = 0.0;

const double epsilon = 0.1;

const double kappa = 0.1;

const double tau = 10;

array<vec3d> xyz_airfoil = GetVKTAirfoilPnts(npts, alpha, epsilon, kappa, tau*(pi/180) );

array<double> cp_dist = GetVKTAirfoilCpDist( alpha, epsilon, kappa, tau*(pi/180), xyz_airfoil );
```

 

pi = 3.14159265358979323846

npts = 122

alpha = 0.0

epsilon = 0.1

kappa = 0.1

tau = 10

xyz_airfoil = GetVKTAirfoilPnts(npts, alpha, epsilon, kappa, tau*(pi/180) )

cp_dist = GetVKTAirfoilCpDist( alpha, epsilon, kappa, tau*(pi/180), xyz_airfoil )
```

  


### function GetVKTAirfoilCpDist

```
std::vector< double > GetVKTAirfoilCpDist(
    const double & alpha,
    const double & epsilon,
    const double & kappa,
    const double & tau,
    const std::vector< vec3d > & xyz_data
)
```


**Parameters**: 

  * **alpha** double Airfoil angle of attack (Radians) 
  * **epsilon** double Airfoil thickness 
  * **kappa** double Airfoil camber 
  * **tau** double Airfoil trailing edge angle (Radians) 
  * **xyz_data** vector<vec3d> Vector of points on the airfoil to evaluate 


**See**: [GetVKTAirfoilPnts](Modules/group___x_sec.md#function-getvktairfoilpnts)

**Return**: vector<double> Vector of Cp values for each point in xydata 

Get the pressure coefficient (Cp) along a Von Kármán-Trefftz airfoil of specified shape at specified points along the airfoil 

const double pi = 3.14159265358979323846;

const int npts = 122;

const double alpha = 0.0;

const double epsilon = 0.1;

const double kappa = 0.1;

const double tau = 10;

array<vec3d> xyz_airfoil = GetVKTAirfoilPnts(npts, alpha, epsilon, kappa, tau*(pi/180) );

array<double> cp_dist = GetVKTAirfoilCpDist( alpha, epsilon, kappa, tau*(pi/180), xyz_airfoil );
```

 

pi = 3.14159265358979323846

npts = 122

alpha = 0.0

epsilon = 0.1

kappa = 0.1

tau = 10

xyz_airfoil = GetVKTAirfoilPnts(npts, alpha, epsilon, kappa, tau*(pi/180) )

cp_dist = GetVKTAirfoilCpDist( alpha, epsilon, kappa, tau*(pi/180), xyz_airfoil )
```

  


### function GetEllipsoidSurfPnts

```
std::vector< vec3d > GetEllipsoidSurfPnts(
    const vec3d & center,
    const vec3d & abc_rad,
    int u_npts =20,
    int w_npts =20
)
```


**Parameters**: 

  * **center** 3D location of the ellipsoid center 
  * **abc_rad** Radius along the A (X), B (Y), and C (Z) axes 
  * **u_npts** Number of points in the U direction 
  * **w_npts** Number of points in the W direction 


**See**: [GetVKTAirfoilPnts](Modules/group___x_sec.md#function-getvktairfoilpnts)

**Return**: Array of coordinates describing the ellipsoid surface 

Generate the surface coordinate points for a ellipsoid at specified center of input radius along each axis. Based on the MATLAB function ellipsoid ([https://in.mathworks.com/help/matlab/ref/ellipsoid.html](https://in.mathworks.com/help/matlab/ref/ellipsoid.html)). 


### function GetFeatureLinePnts

```
std::vector< vec3d > GetFeatureLinePnts(
    const string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: Array of points along the Geom's feature lines 

Get the points along the feature lines of a particular Geom 


### function GetEllipsoidCpDist

```
std::vector< double > GetEllipsoidCpDist(
    const std::vector< vec3d > & surf_pnt_vec,
    const vec3d & abc_rad,
    const vec3d & V_inf
)
```


**Parameters**: 

  * **surf_pnt_vec** vector<vec3d> Vector of points on the ellipsoid surface to assess 
  * **abc_rad** [vec3d](Classes/classvec3d.md) Radius along the A (X), B (Y), and C (Z) axes 
  * **V_inf** [vec3d](Classes/classvec3d.md) 3D components of freestream velocity 


**See**: [GetEllipsoidSurfPnts](Modules/group___x_sec.md#function-getellipsoidsurfpnts)

**Return**: vector<double> Vector of Cp results corresponding to each point in surf_pnt_arr 

Generate Analytical Solution for Potential Flow for specified ellipsoid shape at input surface points for input velocity vector. Based on Munk, M. M., 'Remarks on the Pressure Distribution over the Surface of an Ellipsoid, Moving Translationally Through a Perfect Fluid,' NACA TN-196, June 1924. Function initially created to compare VSPAERO results to theory. 

const double pi = 3.14159265358979323846;

const int npts = 101;

const vec3d abc_rad = vec3d(1.0, 2.0, 3.0);

const double alpha = 5; // deg

const double beta = 5; // deg

const double V_inf = 100.0;

array < vec3d > x_slice_pnt_vec(npts);
array<double> theta_vec(npts);

theta_vec[0] = 0;

for ( int i = 1; i < npts; i++ )
{
    theta_vec[i] = theta_vec[i-1] + (2 * pi / ( npts - 1) );
}

for ( int i = 0; i < npts; i++ )
{
    x_slice_pnt_vec[i] = vec3d( 0, abc_rad[1] * cos( theta_vec[i] ), abc_rad[2] *sin( theta_vec[i] ) );
}

vec3d V_vec = vec3d( ( V_inf * cos( Deg2Rad( alpha ) ) * cos( Deg2Rad( beta ) ) ), ( V_inf * sin( Deg2Rad( beta ) ) ), ( V_inf * sin( Deg2Rad( alpha ) ) * cos( Deg2Rad( beta ) ) ) );

array < double > cp_dist = GetEllipsoidCpDist( x_slice_pnt_vec, abc_rad, V_vec );
```

 

import math
pi = 3.14159265358979323846

npts = 101

abc_rad = vec3d(1.0, 2.0, 3.0)

alpha = 5 # deg

beta = 5 # deg

V_inf = 100.0

x_slice_pnt_vec = [None]*npts
theta_vec = [None]*npts

theta_vec[0] = 0

for i in range(1, npts):
    theta_vec[i] = theta_vec[i-1] + (2 * pi / (npts - 1))


for i in range(npts):

    x_slice_pnt_vec[i] = vec3d( 0, abc_rad.y() * math.cos( theta_vec[i] ), abc_rad.z() * math.sin( theta_vec[i] ) )

V_vec = vec3d( ( V_inf * math.cos( alpha*pi/180 ) * math.cos( beta*pi/180 ) ), ( V_inf * math.sin( beta*pi/180 ) ), ( V_inf * math.sin( alpha*pi/180 ) * math.cos( beta*pi/180 ) ) )

cp_dist = GetEllipsoidCpDist( x_slice_pnt_vec, abc_rad, V_vec )
```

  


### function GetAirfoilUpperPnts

```
std::vector< vec3d > GetAirfoilUpperPnts(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 


**See**: [SetAirfoilPnts](Modules/group___x_sec.md#function-setairfoilpnts)

**Return**: vector<vec3d> VectorArray of coordinate points for the upper airfoil surface 

Get the coordinate points for the upper surface of an airfoil. The XSec must be of type XS_FILE_AIRFOIL 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL );

string xsec = GetXSec( xsec_surf, 1 );

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" );

array< vec3d > @up_array = GetAirfoilUpperPnts( xsec );
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL )

xsec = GetXSec( xsec_surf, 1 )

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" )

up_array = GetAirfoilUpperPnts( xsec )
```

  


### function GetAirfoilLowerPnts

```
std::vector< vec3d > GetAirfoilLowerPnts(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 


**See**: [SetAirfoilPnts](Modules/group___x_sec.md#function-setairfoilpnts)

**Return**: vector<vec3d> Vector of coordinate points for the lower airfoil surface 

Get the coordinate points for the lower surface of an airfoil. The XSec must be of type XS_FILE_AIRFOIL 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL );

string xsec = GetXSec( xsec_surf, 1 );

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" );

array< vec3d > @low_array = GetAirfoilLowerPnts( xsec );
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, 1, XS_FILE_AIRFOIL )

xsec = GetXSec( xsec_surf, 1 )

ReadFileAirfoil( xsec, "airfoil/N0012_VSP.af" )

low_array = GetAirfoilLowerPnts( xsec )
```

  


### function GetUpperCSTCoefs

```
std::vector< double > GetUpperCSTCoefs(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 


**See**: [SetUpperCST](Modules/group___x_sec.md#function-setuppercst)

**Return**: vector<double> Vector of CST coefficients for the upper airfoil surface 

Get the CST coefficients for the upper surface of an airfoil. The XSec must be of type XS_CST_AIRFOIL 


### function GetLowerCSTCoefs

```
std::vector< double > GetLowerCSTCoefs(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 


**See**: [SetLowerCST](Modules/group___x_sec.md#function-setlowercst)

**Return**: vector<double> Vector of CST coefficients for the lower airfoil surface 

Get the CST coefficients for the lower surface of an airfoil. The XSec must be of type XS_CST_AIRFOIL 


### function GetUpperCSTDegree

```
int GetUpperCSTDegree(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 


**See**: [SetUpperCST](Modules/group___x_sec.md#function-setuppercst)

**Return**: int CST Degree for upper airfoil surface 

Get the CST degree for the upper surface of an airfoil. The XSec must be of type XS_CST_AIRFOIL 


### function GetLowerCSTDegree

```
int GetLowerCSTDegree(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [SetLowerCST](Modules/group___x_sec.md#function-setlowercst)

**Return**: int CST Degree for lower airfoil surface 

Get the CST degree for the lower surface of an airfoil. The XSec must be of type XS_CST_AIRFOIL 


### function SetUpperCST

```
void SetUpperCST(
    const std::string & xsec_id,
    int deg,
    const std::vector< double > & coefs
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 
  * **deg** int CST degree of upper airfoil surface 
  * **coefs** vector<double> Vector of CST coefficients for the upper airfoil surface 


**See**: [GetUpperCSTDegree](Modules/group___x_sec.md#function-getuppercstdegree), [GetUpperCSTCoefs](Modules/group___x_sec.md#function-getuppercstcoefs)

Set the CST degree and coefficients for the upper surface of an airfoil. The number of coefficients should be one more than the CST degree. The XSec must be of type XS_CST_AIRFOIL 


### function SetLowerCST

```
void SetLowerCST(
    const std::string & xsec_id,
    int deg,
    const std::vector< double > & coefs
)
```


**Parameters**: 

  * **xsec_id** string XSec ID 
  * **deg** int CST degree of lower airfoil surface 
  * **coefs** vector<double> Vector of CST coefficients for the lower airfoil surface 


**See**: [GetLowerCSTDegree](Modules/group___x_sec.md#function-getlowercstdegree), [GetLowerCSTCoefs](Modules/group___x_sec.md#function-getlowercstcoefs)

Set the CST degree and coefficients for the lower surface of an airfoil. The number of coefficients should be one more than the CST degree. The XSec must be of type XS_CST_AIRFOIL 


### function PromoteCSTUpper

```
void PromoteCSTUpper(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [GetUpperCSTDegree](Modules/group___x_sec.md#function-getuppercstdegree)

Promote the CST for the upper airfoil surface. The XSec must be of type XS_CST_AIRFOIL 


### function PromoteCSTLower

```
void PromoteCSTLower(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [GetLowerCSTDegree](Modules/group___x_sec.md#function-getlowercstdegree)

Promote the CST for the lower airfoil surface. The XSec must be of type XS_CST_AIRFOIL 


### function DemoteCSTUpper

```
void DemoteCSTUpper(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [GetUpperCSTDegree](Modules/group___x_sec.md#function-getuppercstdegree)

Demote the CST for the upper airfoil surface. The XSec must be of type XS_CST_AIRFOIL 


### function DemoteCSTLower

```
void DemoteCSTLower(
    const std::string & xsec_id
)
```


**Parameters**: 

  * **xsec_id** XSec ID 


**See**: [GetLowerCSTDegree](Modules/group___x_sec.md#function-getlowercstdegree)

Demote the CST for the lower airfoil surface. The XSec must be of type XS_CST_AIRFOIL 


### function FitAfCST

```
void FitAfCST(
    const std::string & xsec_surf_id,
    int xsec_index,
    int deg
)
```


**Parameters**: 

  * **xsec_surf_id** XsecSurf ID 
  * **xsec_index** XSec index 
  * **deg** CST degree 


Fit a CST airfoil for an existing airfoil of type XS_FOUR_SERIES, XS_SIX_SERIES, XS_FOUR_DIGIT_MOD, XS_FIVE_DIGIT, XS_FIVE_DIGIT_MOD, XS_ONE_SIX_SERIES, or XS_FILE_AIRFOIL. 


### function WriteBezierAirfoil

```
void WriteBezierAirfoil(
    const std::string & file_name,
    const std::string & geom_id,
    const double & foilsurf_u
)
```


**Parameters**: 

  * **file_name** Airfoil (*.bz) output file name 
  * **geom_id** string Geom ID 
  * **foilsurf_u** U location (range: 0 - 1) along the surface. The foil surface does not include root and tip caps (i.e. 2 section wing -> XSec0 @ u=0, XSec1 @ u=0.5, XSec2 @ u=1.0) 


Write out the untwisted unit-length 2D Bezier curve for the specified airfoil in custom *.bz format. The output will describe the analytical shape of the airfoil. See BezierAirfoilExample.m and BezierCtrlToCoordPnts.m for examples of discretizing the Bezier curve and generating a Selig airfoil file. 

//==== Add Wing Geometry and Set Parms ====//
string wing_id = AddGeom( "WING", "" );

const double u = 0.5; // export airfoil at mid span location

//==== Write Bezier Airfoil File ====//
WriteBezierAirfoil( "Example_Bezier.bz", wing_id, u );
```

 

#==== Add Wing Geometry and Set Parms ====//
wing_id = AddGeom( "WING", "" )

u = 0.5 # export airfoil at mid span location

#==== Write Bezier Airfoil File ====//
WriteBezierAirfoil( "Example_Bezier.bz", wing_id, u )
```

  


### function WriteSeligAirfoil

```
void WriteSeligAirfoil(
    const std::string & file_name,
    const std::string & geom_id,
    const double & foilsurf_u
)
```


**Parameters**: 

  * **file_name** Airfoil (*.dat) output file name 
  * **geom_id** string Geom ID 
  * **foilsurf_u** U location (range: 0 - 1) along the surface. The foil surface does not include root and tip caps (i.e. 2 section wing -> XSec0 @ u=0, XSec1 @ u=0.5, XSec2 @ u=1.0) 


**See**: [GetAirfoilCoordinates](Modules/group___x_sec.md#function-getairfoilcoordinates)

Write out the untwisted unit-length 2D coordinate points for the specified airfoil in Selig format. Coordinate points follow the on-screen wire frame W tessellation. 

//==== Add Wing Geometry and Set Parms ====//
string wing_id = AddGeom( "WING", "" );

const double u = 0.5; // export airfoil at mid span location

//==== Write Selig Airfoil File ====//
WriteSeligAirfoil( "Example_Selig.dat", wing_id, u );
```

 

#==== Add Wing Geometry and Set Parms ====//
wing_id = AddGeom( "WING", "" )

u = 0.5 # export airfoil at mid span location

#==== Write Selig Airfoil File ====//
WriteSeligAirfoil( "Example_Selig.dat", wing_id, u )
```

  


### function GetAirfoilCoordinates

```
std::vector< vec3d > GetAirfoilCoordinates(
    const std::string & geom_id,
    const double & foilsurf_u
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **foilsurf_u** U location (range: 0 - 1) along the surface. The foil surface does not include root and tip caps (i.e. 2 section wing -> XSec0 @ u=0, XSec1 @ u=0.5, XSec2 @ u=1.0) 


**See**: [WriteSeligAirfoil](Modules/group___x_sec.md#function-writeseligairfoil)

Get the untwisted unit-length 2D coordinate points for the specified airfoil 






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800