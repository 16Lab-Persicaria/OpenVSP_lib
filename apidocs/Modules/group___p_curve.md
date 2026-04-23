---
title: Propeller Blade Curve Functions
summary: The following group of API functions may be used to control parametric propeller blade curves (PCurves). Click here to return to the main page. 

---

# Propeller Blade Curve Functions

The following group of API functions may be used to control parametric propeller blade curves (PCurves). Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[SetPCurve](Modules/group___p_curve.md#function-setpcurve)**(const std::string & geom_id, const int & pcurveid, const std::vector< double > & tvec, const std::vector< double > & valvec, const int & newtype) |
| void | **[PCurveConvertTo](Modules/group___p_curve.md#function-pcurveconvertto)**(const std::string & geom_id, const int & pcurveid, const int & newtype) |
| int | **[PCurveGetType](Modules/group___p_curve.md#function-pcurvegettype)**(const std::string & geom_id, const int & pcurveid) |
| std::vector< double > | **[PCurveGetTVec](Modules/group___p_curve.md#function-pcurvegettvec)**(const std::string & geom_id, const int & pcurveid) |
| std::vector< double > | **[PCurveGetValVec](Modules/group___p_curve.md#function-pcurvegetvalvec)**(const std::string & geom_id, const int & pcurveid) |
| void | **[PCurveDeletePt](Modules/group___p_curve.md#function-pcurvedeletept)**(const std::string & geom_id, const int & pcurveid, const int & indx) |
| int | **[PCurveSplit](Modules/group___p_curve.md#function-pcurvesplit)**(const std::string & geom_id, const int & pcurveid, const double & tsplit) |
| void | **[ApproximateAllPropellerPCurves](Modules/group___p_curve.md#function-approximateallpropellerpcurves)**(const std::string & geom_id) |
| void | **[ResetPropellerThicknessCurve](Modules/group___p_curve.md#function-resetpropellerthicknesscurve)**(const std::string & geom_id) |


## Functions Documentation

### function SetPCurve

```
void SetPCurve(
    const std::string & geom_id,
    const int & pcurveid,
    const std::vector< double > & tvec,
    const std::vector< double > & valvec,
    const int & newtype
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pcurveid** P Curve index 
  * **tvec** Array of parameter values 
  * **valvec** Array of values 
  * **newtype** Curve type enum (i.e. CEDIT) 


**See**: [PCURV_TYPE](Modules/group___enumerations.md#enum-pcurv-type)

Set the parameters, values, and curve type of a propeller blade curve (P Curve) 


### function PCurveConvertTo

```
void PCurveConvertTo(
    const std::string & geom_id,
    const int & pcurveid,
    const int & newtype
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pcurveid** P Curve index 
  * **newtype** Curve type enum (i.e. CEDIT) 


**See**: [PCURV_TYPE](Modules/group___enumerations.md#enum-pcurv-type)

Change the type of a propeller blade curve (P Curve) 


### function PCurveGetType

```
int PCurveGetType(
    const std::string & geom_id,
    const int & pcurveid
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pcurveid** P Curve index 


**See**: [PCURV_TYPE](Modules/group___enumerations.md#enum-pcurv-type)

**Return**: Curve type enum (i.e. CEDIT) 

Get the type of a propeller blade curve (P Curve) 


### function PCurveGetTVec

```
std::vector< double > PCurveGetTVec(
    const std::string & geom_id,
    const int & pcurveid
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pcurveid** P Curve index 


**Return**: Array of parameters 

Get the parameters of a propeller blade curve (P Curve). Each parameter is a fraction of propeller radius. 


### function PCurveGetValVec

```
std::vector< double > PCurveGetValVec(
    const std::string & geom_id,
    const int & pcurveid
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pcurveid** P Curve index 


**Return**: Array of values 

Get the values of a propeller blade curve (P Curve). What the values represent id dependent on the curve type (i.e. twist, chord, etc.). 


### function PCurveDeletePt

```
void PCurveDeletePt(
    const std::string & geom_id,
    const int & pcurveid,
    const int & indx
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pcurveid** P Curve index 
  * **indx** Point index 


Delete a propeller blade curve (P Curve) point 


### function PCurveSplit

```
int PCurveSplit(
    const std::string & geom_id,
    const int & pcurveid,
    const double & tsplit
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pcurveid** P Curve index 
  * **tsplit** 1D parameter split location 


**Return**: Index of new control point 

Split a propeller blade curve (P Curve) at the specified 1D parameter 


### function ApproximateAllPropellerPCurves

```
void ApproximateAllPropellerPCurves(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


Approximate all propeller blade curves with cubic Bezier curves. 

// Add Propeller
string prop = AddGeom( "PROP", "" );

ApproximateAllPropellerPCurves( prop );
```

 \endforcpponly \beginPythonOnly ```py

# Add Propeller
prop = AddGeom( "PROP", "" )

ApproximateAllPropellerPCurves( prop )
```

  


### function ResetPropellerThicknessCurve

```
void ResetPropellerThicknessCurve(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


Reset propeller T/C curve to match basic thickness of file-type airfoils. Typically only used for a propeller that has been constructed with file-type airfoils across the blade. The new thickness curve will be a PCHIP curve with t/c matching the propeller's XSecs &ndash; unless it is a file XSec, then the Base thickness is used. 

// Add Propeller
string prop = AddGeom( "PROP", "" );

ResetPropellerThicknessCurve( prop );
```

 \endforcpponly \beginPythonOnly ```py

# Add Propeller
prop = AddGeom( "PROP", "" )

ResetPropellerThicknessCurve( prop )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800