---
title: BOR Functions
summary: This group of API functions provides capabilities related to the body of revolution (BOR) geometry type in OpenVSP. Click here to return to the main page. 

---

# BOR Functions

This group of API functions provides capabilities related to the body of revolution (BOR) geometry type in OpenVSP. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[ChangeBORXSecShape](Modules/group___b_o_r.md#function-changeborxsecshape)**(const string & bor_id, int type) |
| int | **[GetBORXSecShape](Modules/group___b_o_r.md#function-getborxsecshape)**(const string & bor_id) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[ReadBORFileXSec](Modules/group___b_o_r.md#function-readborfilexsec)**(const std::string & bor_id, const std::string & file_name) |
| void | **[SetBORXSecPnts](Modules/group___b_o_r.md#function-setborxsecpnts)**(const std::string & bor_id, std::vector< [vec3d](Classes/classvec3d.md) > & pnt_vec) |
| [vec3d](Classes/classvec3d.md) | **[ComputeBORXSecPnt](Modules/group___b_o_r.md#function-computeborxsecpnt)**(const std::string & bor_id, double fract) |
| [vec3d](Classes/classvec3d.md) | **[ComputeBORXSecTan](Modules/group___b_o_r.md#function-computeborxsectan)**(const std::string & bor_id, double fract) |
| void | **[ReadBORFileAirfoil](Modules/group___b_o_r.md#function-readborfileairfoil)**(const std::string & bor_id, const std::string & file_name) |
| void | **[SetBORAirfoilUpperPnts](Modules/group___b_o_r.md#function-setborairfoilupperpnts)**(const std::string & bor_id, const std::vector< [vec3d](Classes/classvec3d.md) > & up_pnt_vec) |
| void | **[SetBORAirfoilLowerPnts](Modules/group___b_o_r.md#function-setborairfoillowerpnts)**(const std::string & bor_id, const std::vector< [vec3d](Classes/classvec3d.md) > & low_pnt_vec) |
| void | **[SetBORAirfoilPnts](Modules/group___b_o_r.md#function-setborairfoilpnts)**(const std::string & bor_id, const std::vector< [vec3d](Classes/classvec3d.md) > & up_pnt_vec, const std::vector< [vec3d](Classes/classvec3d.md) > & low_pnt_vec) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetBORAirfoilUpperPnts](Modules/group___b_o_r.md#function-getborairfoilupperpnts)**(const std::string & bor_id) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[GetBORAirfoilLowerPnts](Modules/group___b_o_r.md#function-getborairfoillowerpnts)**(const std::string & bor_id) |
| std::vector< double > | **[GetBORUpperCSTCoefs](Modules/group___b_o_r.md#function-getboruppercstcoefs)**(const std::string & bor_id) |
| std::vector< double > | **[GetBORLowerCSTCoefs](Modules/group___b_o_r.md#function-getborlowercstcoefs)**(const std::string & bor_id) |
| int | **[GetBORUpperCSTDegree](Modules/group___b_o_r.md#function-getboruppercstdegree)**(const std::string & bor_id) |
| int | **[GetBORLowerCSTDegree](Modules/group___b_o_r.md#function-getborlowercstdegree)**(const std::string & bor_id) |
| void | **[SetBORUpperCST](Modules/group___b_o_r.md#function-setboruppercst)**(const std::string & bor_id, int deg, const std::vector< double > & coefs) |
| void | **[SetBORLowerCST](Modules/group___b_o_r.md#function-setborlowercst)**(const std::string & bor_id, int deg, const std::vector< double > & coefs) |
| void | **[PromoteBORCSTUpper](Modules/group___b_o_r.md#function-promoteborcstupper)**(const std::string & bor_id) |
| void | **[PromoteBORCSTLower](Modules/group___b_o_r.md#function-promoteborcstlower)**(const std::string & bor_id) |
| void | **[DemoteBORCSTUpper](Modules/group___b_o_r.md#function-demoteborcstupper)**(const std::string & bor_id) |
| void | **[DemoteBORCSTLower](Modules/group___b_o_r.md#function-demoteborcstlower)**(const std::string & bor_id) |
| void | **[FitBORAfCST](Modules/group___b_o_r.md#function-fitborafcst)**(const std::string & bor_id, int deg) |


## Functions Documentation

### function ChangeBORXSecShape

```
void ChangeBORXSecShape(
    const string & bor_id,
    int type
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **type** int XSec type enum (i.e. XS_ROUNDED_RECTANGLE) 


**See**: [XSEC_CRV_TYPE](Modules/group___enumerations.md#enum-xsec-crv-type)

Set the XSec type for a BOR component 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_ROUNDED_RECTANGLE );

if ( GetBORXSecShape( bor_id ) != XS_ROUNDED_RECTANGLE ) { Print( "ERROR: ChangeBORXSecShape" ); }
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_ROUNDED_RECTANGLE )

if  GetBORXSecShape( bor_id ) != XS_ROUNDED_RECTANGLE : print( "ERROR: ChangeBORXSecShape" )
```

  


### function GetBORXSecShape

```
int GetBORXSecShape(
    const string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**Return**: int XSec type enum (i.e. XS_ROUNDED_RECTANGLE) 

Get the XSec type for a BOR component 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_ROUNDED_RECTANGLE );

if ( GetBORXSecShape( bor_id ) != XS_ROUNDED_RECTANGLE ) { Print( "ERROR: GetBORXSecShape" ); }
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_ROUNDED_RECTANGLE )

if  GetBORXSecShape( bor_id ) != XS_ROUNDED_RECTANGLE : print( "ERROR: GetBORXSecShape" )
```

  


### function ReadBORFileXSec

```
std::vector< vec3d > ReadBORFileXSec(
    const std::string & bor_id,
    const std::string & file_name
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **file_name** string Fuselage XSec file name 


**Return**: vector<vec3d> Array of coordinate points read from the file and set to the XSec 

Set the coordinate points for a specific BOR. The BOR XSecCurve must be of type XS_FILE_FUSE. 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_FUSE );

array< vec3d > @vec_array = ReadBORFileXSec( bor_id, "TestXSec.fxs" );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_FUSE )

vec_array = ReadBORFileXSec( bor_id, "TestXSec.fxs" )
```

  


### function SetBORXSecPnts

```
void SetBORXSecPnts(
    const std::string & bor_id,
    std::vector< vec3d > & pnt_vec
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **pnt_vec** vector<vec3d> Vector of XSec coordinate points 


Set the coordinate points for a specific BOR. The BOR XSecCurve must be of type XS_FILE_FUSE. 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_FUSE );

array< vec3d > @vec_array = ReadBORFileXSec( bor_id, "TestXSec.fxs" );

if ( vec_array.size() > 0 )
{
    vec_array[1] = vec_array[1] * 2.0;
    vec_array[3] = vec_array[3] * 2.0;

    SetBORXSecPnts( bor_id, vec_array );
}
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_FUSE )

vec_array = ReadBORFileXSec( bor_id, "TestXSec.fxs" )

if  len(vec_array) > 0 :
    vec_array[1] = vec_array[1] * 2.0
    vec_array[3] = vec_array[3] * 2.0

    SetBORXSecPnts( bor_id, vec_array )
```

  


### function ComputeBORXSecPnt

```
vec3d ComputeBORXSecPnt(
    const std::string & bor_id,
    double fract
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **fract** double Curve parameter value (range: 0 - 1) 


**Return**: [vec3d](Classes/classvec3d.md) Coordinate point on curve 

Compute 3D coordinate for a point on a BOR XSecCurve given the parameter value (U) along the curve 

//==== Add Geom ====//
// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

double u_fract = 0.25;

vec3d pnt = ComputeBORXSecPnt( bor_id, u_fract );
```

 

#==== Add Geom ====//
# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

u_fract = 0.25

pnt = ComputeBORXSecPnt( bor_id, u_fract )
```

  


### function ComputeBORXSecTan

```
vec3d ComputeBORXSecTan(
    const std::string & bor_id,
    double fract
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **fract** double Curve parameter value (range: 0 - 1) 


**Return**: [vec3d](Classes/classvec3d.md) Tangent vector on curve 

Compute the tangent vector of a point on a BOR XSecCurve given the parameter value (U) along the curve 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

double u_fract = 0.25;

vec3d tan = ComputeBORXSecTan( bor_id, u_fract );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

u_fract = 0.25

tan = ComputeBORXSecTan( bor_id, u_fract )
```

  


### function ReadBORFileAirfoil

```
void ReadBORFileAirfoil(
    const std::string & bor_id,
    const std::string & file_name
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **file_name** string Airfoil XSec file name 


Read in shape from airfoil file and set to the specified BOR XSecCurve. The XSecCurve must be of type XS_FILE_AIRFOIL. Airfoil files may be in Lednicer or Selig format with *.af or *.dat extensions. 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL );

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL )

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" )
```

  


### function SetBORAirfoilUpperPnts

```
void SetBORAirfoilUpperPnts(
    const std::string & bor_id,
    const std::vector< vec3d > & up_pnt_vec
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **up_pnt_vec** vector<vec3d> Vector of points defining the upper surface of the airfoil 


Set the upper points for an airfoil on a BOR. The BOR XSecCurve must be of type XS_FILE_AIRFOIL. 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL );

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" );

array< vec3d > @up_array = GetBORAirfoilUpperPnts( bor_id );

for ( int i = 0 ; i < int( up_array.size() ) ; i++ )
{
    up_array[i].scale_y( 2.0 );
}

SetBORAirfoilUpperPnts( bor_id, up_array );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL )

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" )

up_array = GetBORAirfoilUpperPnts( bor_id )

for i in range(int( len(up_array) )):

    up_array[i].scale_y( 2.0 )

SetBORAirfoilUpperPnts( bor_id, up_array )
```

  


### function SetBORAirfoilLowerPnts

```
void SetBORAirfoilLowerPnts(
    const std::string & bor_id,
    const std::vector< vec3d > & low_pnt_vec
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **low_pnt_vec** vector<vec3d> Vector of points defining the lower surface of the airfoil 


Set the lower points for an airfoil on a BOR. The BOR XSecCurve must be of type XS_FILE_AIRFOIL. 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL );

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" );

array< vec3d > @low_array = GetBORAirfoilLowerPnts( bor_id );

for ( int i = 0 ; i < int( low_array.size() ) ; i++ )
{
    low_array[i].scale_y( 0.5 );
}

SetBORAirfoilLowerPnts( bor_id, low_array );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL )

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" )

low_array = GetBORAirfoilLowerPnts( bor_id )

for i in range(int( len(low_array) )):

    low_array[i].scale_y( 0.5 )

SetBORAirfoilLowerPnts( bor_id, low_array )
```

  


### function SetBORAirfoilPnts

```
void SetBORAirfoilPnts(
    const std::string & bor_id,
    const std::vector< vec3d > & up_pnt_vec,
    const std::vector< vec3d > & low_pnt_vec
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **up_pnt_vec** vector<vec3d> Vector of points defining the upper surface of the airfoil 
  * **low_pnt_vec** vector<_>[vec3d](Classes/classvec3d.md)> Vector of points defining the lower surface of the airfoil 


Set the upper and lower points for an airfoil on a BOR. The BOR XSecCurve must be of type XS_FILE_AIRFOIL. 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL );

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" );

array< vec3d > @up_array = GetBORAirfoilUpperPnts( bor_id );

array< vec3d > @low_array = GetBORAirfoilLowerPnts( bor_id );

for ( int i = 0 ; i < int( up_array.size() ) ; i++ )
{
    up_array[i].scale_y( 2.0 );

    low_array[i].scale_y( 0.5 );
}

SetBORAirfoilPnts( bor_id, up_array, low_array );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL )

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" )

up_array = GetBORAirfoilUpperPnts( bor_id )

low_array = GetBORAirfoilLowerPnts( bor_id )

for i in range(int( len(up_array) )):

    up_array[i].scale_y( 2.0 )

    low_array[i].scale_y( 0.5 )

SetBORAirfoilPnts( bor_id, up_array, low_array )
```

  


### function GetBORAirfoilUpperPnts

```
std::vector< vec3d > GetBORAirfoilUpperPnts(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [SetAirfoilPnts](Modules/group___x_sec.md#function-setairfoilpnts)

**Return**: vector<vec3d> Vector of coordinate points for the upper airfoil surface 

Get the coordinate points for the upper surface of an airfoil on a BOR. The BOR XSecCurve must be of type XS_FILE_AIRFOIL 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL );

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" );

array< vec3d > @up_array = GetBORAirfoilUpperPnts( bor_id );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL )

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" )

up_array = GetBORAirfoilUpperPnts( bor_id )
```

  


### function GetBORAirfoilLowerPnts

```
std::vector< vec3d > GetBORAirfoilLowerPnts(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [SetAirfoilPnts](Modules/group___x_sec.md#function-setairfoilpnts)

**Return**: vector<vec3d> Vector of coordinate points for the lower airfoil surface 

Get the coordinate points for the lower surface of an airfoil of a BOR. The XSecCurve must be of type XS_FILE_AIRFOIL 

// Add Body of Recolution
string bor_id = AddGeom( "BODYOFREVOLUTION", "" );

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL );

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" );

array< vec3d > @low_array = GetBORAirfoilLowerPnts( bor_id );
```

 

# Add Body of Recolution
bor_id = AddGeom( "BODYOFREVOLUTION", "" )

ChangeBORXSecShape( bor_id, XS_FILE_AIRFOIL )

ReadBORFileAirfoil( bor_id, "airfoil/N0012_VSP.af" )

low_array = GetBORAirfoilLowerPnts( bor_id )
```

  


### function GetBORUpperCSTCoefs

```
std::vector< double > GetBORUpperCSTCoefs(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** Body of revolution Geom ID 


**See**: [SetUpperCST](Modules/group___x_sec.md#function-setuppercst)

**Return**: vector<double> Vector of CST coefficients for the upper airfoil surface 

Get the CST coefficients for the upper surface of an airfoil of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function GetBORLowerCSTCoefs

```
std::vector< double > GetBORLowerCSTCoefs(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [SetLowerCST](Modules/group___x_sec.md#function-setlowercst)

**Return**: vector<double> Vector of CST coefficients for the lower airfoil surface 

Get the CST coefficients for the lower surface of an airfoil of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function GetBORUpperCSTDegree

```
int GetBORUpperCSTDegree(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [SetUpperCST](Modules/group___x_sec.md#function-setuppercst)

**Return**: int CST Degree for upper airfoil surface 

Get the CST degree for the upper surface of an airfoil of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function GetBORLowerCSTDegree

```
int GetBORLowerCSTDegree(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [SetLowerCST](Modules/group___x_sec.md#function-setlowercst)

**Return**: int CST Degree for lower airfoil surface 

Get the CST degree for the lower surface of an airfoil of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function SetBORUpperCST

```
void SetBORUpperCST(
    const std::string & bor_id,
    int deg,
    const std::vector< double > & coefs
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **deg** CST degree of upper airfoil surface 
  * **coefs** Array of CST coefficients for the upper airfoil surface 


**See**: [GetUpperCSTDegree](Modules/group___x_sec.md#function-getuppercstdegree), [GetUpperCSTCoefs](Modules/group___x_sec.md#function-getuppercstcoefs)

Set the CST degree and coefficients for the upper surface of an airfoil of a BOR. The number of coefficients should be one more than the CST degree. The XSecCurve must be of type XS_CST_AIRFOIL 


### function SetBORLowerCST

```
void SetBORLowerCST(
    const std::string & bor_id,
    int deg,
    const std::vector< double > & coefs
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **deg** int CST degree of lower airfoil surface 
  * **coefs** vector<double> Vector of CST coefficients for the lower airfoil surface 


**See**: [GetLowerCSTDegree](Modules/group___x_sec.md#function-getlowercstdegree), [GetLowerCSTCoefs](Modules/group___x_sec.md#function-getlowercstcoefs)

Set the CST degree and coefficients for the lower surface of an airfoil of a BOR. The number of coefficients should be one more than the CST degree. The XSecCurve must be of type XS_CST_AIRFOIL 


### function PromoteBORCSTUpper

```
void PromoteBORCSTUpper(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [GetUpperCSTDegree](Modules/group___x_sec.md#function-getuppercstdegree)

Promote the CST for the upper airfoil surface of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function PromoteBORCSTLower

```
void PromoteBORCSTLower(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [GetLowerCSTDegree](Modules/group___x_sec.md#function-getlowercstdegree)

Promote the CST for the lower airfoil surface of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function DemoteBORCSTUpper

```
void DemoteBORCSTUpper(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [GetUpperCSTDegree](Modules/group___x_sec.md#function-getuppercstdegree)

Demote the CST for the upper airfoil surface of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function DemoteBORCSTLower

```
void DemoteBORCSTLower(
    const std::string & bor_id
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 


**See**: [GetLowerCSTDegree](Modules/group___x_sec.md#function-getlowercstdegree)

Demote the CST for the lower airfoil surface of a BOR. The XSecCurve must be of type XS_CST_AIRFOIL 


### function FitBORAfCST

```
void FitBORAfCST(
    const std::string & bor_id,
    int deg
)
```


**Parameters**: 

  * **bor_id** string Body of revolution Geom ID 
  * **deg** int CST degree 


Fit a CST airfoil for an existing airfoil of a BOR of type XS_FOUR_SERIES, XS_SIX_SERIES, XS_FOUR_DIGIT_MOD, XS_FIVE_DIGIT, XS_FIVE_DIGIT_MOD, XS_ONE_SIX_SERIES, or XS_FILE_AIRFOIL. 






-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800