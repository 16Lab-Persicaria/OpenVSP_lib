---
title: Parasite Drag Functions
summary: This group of API functions is supplemental to performing a Paraste Drag analysis through the Analysis Manager. They include functions to write out Parasite Drag Tool equations, calculate atmospheric properties, and control excrescences. Click here to return to the main page. 

---

# Parasite Drag Functions

This group of API functions is supplemental to performing a Paraste Drag analysis through the Analysis Manager. They include functions to write out Parasite Drag Tool equations, calculate atmospheric properties, and control excrescences. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[AddExcrescence](Modules/group___parasite_drag.md#function-addexcrescence)**(const std::string & excresName, const int & excresType, const double & excresVal) |
| void | **[DeleteExcrescence](Modules/group___parasite_drag.md#function-deleteexcrescence)**(const int & index) |
| void | **[UpdateParasiteDrag](Modules/group___parasite_drag.md#function-updateparasitedrag)**() |
| void | **[WriteAtmosphereCSVFile](Modules/group___parasite_drag.md#function-writeatmospherecsvfile)**(const std::string & file_name, const int & atmos_type) |
| void | **[CalcAtmosphere](Modules/group___parasite_drag.md#function-calcatmosphere)**(const double & alt, const double & delta_temp, const int & atmos_type, double & temp, double & pres, double & pres_ratio, double & rho_ratio) |
| void | **[WriteBodyFFCSVFile](Modules/group___parasite_drag.md#function-writebodyffcsvfile)**(const std::string & file_name) |
| void | **[WriteWingFFCSVFile](Modules/group___parasite_drag.md#function-writewingffcsvfile)**(const std::string & file_name) |
| void | **[WriteCfEqnCSVFile](Modules/group___parasite_drag.md#function-writecfeqncsvfile)**(const std::string & file_name) |
| void | **[WritePartialCfMethodCSVFile](Modules/group___parasite_drag.md#function-writepartialcfmethodcsvfile)**(const std::string & file_name) |


## Functions Documentation

### function AddExcrescence

```
void AddExcrescence(
    const std::string & excresName,
    const int & excresType,
    const double & excresVal
)
```


**Parameters**: 

  * **excresName** Name of the Excressence 
  * **excresType** Excressence type enum (i.e. EXCRESCENCE_PERCENT_GEOM) 
  * **excresVal** Excressence value 


**See**: [EXCRES_TYPE](Modules/group___enumerations.md#enum-excres-type)

Add an Excresence to the Parasite Drag Tool 

AddExcrescence( "Miscellaneous", EXCRESCENCE_COUNT, 8.5 );

AddExcrescence( "Cowl Boattail", EXCRESCENCE_CD, 0.0003 );
```

 \endforcpponly \beginPythonOnly ```py

AddExcrescence( "Miscellaneous", EXCRESCENCE_COUNT, 8.5 )

AddExcrescence( "Cowl Boattail", EXCRESCENCE_CD, 0.0003 )
```

  


### function DeleteExcrescence

```
void DeleteExcrescence(
    const int & index
)
```


**Parameters**: 

  * **index** int Index of the Excressence to delete 


Delete an Excresence from the Parasite Drag Tool 

AddExcrescence( "Miscellaneous", EXCRESCENCE_COUNT, 8.5 );

AddExcrescence( "Cowl Boattail", EXCRESCENCE_CD, 0.0003 );

AddExcrescence( "Percentage Example", EXCRESCENCE_PERCENT_GEOM, 5 );

DeleteExcrescence( 2 ); // Last Index
```

 \endforcpponly \beginPythonOnly ```py

AddExcrescence( "Miscellaneous", EXCRESCENCE_COUNT, 8.5 )

AddExcrescence( "Cowl Boattail", EXCRESCENCE_CD, 0.0003 )

AddExcrescence( "Percentage Example", EXCRESCENCE_PERCENT_GEOM, 5 )

DeleteExcrescence( 2 ) # Last Index
```

  


### function UpdateParasiteDrag

```
void UpdateParasiteDrag()
```


Update any reference geometry, atmospheric properties, excressences, etc. in the Parasite Drag Tool 


### function WriteAtmosphereCSVFile

```
void WriteAtmosphereCSVFile(
    const std::string & file_name,
    const int & atmos_type
)
```


**Parameters**: 

  * **file_name** Output CSV file 
  * **atmos_type** Atmospheric model enum (i.e. ATMOS_TYPE_HERRINGTON_1966) 


**See**: [ATMOS_TYPE](Modules/group___enumerations.md#enum-atmos-type)

Calculate the atmospheric properties determined by a specified model for a preset array of altitudes ranging from 0 to 90000 m and write the results to a CSV output file 

Print( "Starting USAF Atmosphere 1966 Table Creation. \n" );

WriteAtmosphereCSVFile( "USAFAtmosphere1966Data.csv", ATMOS_TYPE_HERRINGTON_1966 );
```

 \endforcpponly \beginPythonOnly ```py

print( "Starting USAF Atmosphere 1966 Table Creation. \n" )

WriteAtmosphereCSVFile( "USAFAtmosphere1966Data.csv", ATMOS_TYPE_HERRINGTON_1966 )
```

  


### function CalcAtmosphere

```
void CalcAtmosphere(
    const double & alt,
    const double & delta_temp,
    const int & atmos_type,
    double & temp,
    double & pres,
    double & pres_ratio,
    double & rho_ratio
)
```


**Parameters**: 

  * **alt** Altitude 
  * **delta_temp** Deviation in temperature from the value specified in the atmospheric model 
  * **atmos_type** Atmospheric model enum (i.e. ATMOS_TYPE_HERRINGTON_1966) 
  * **temp** output Temperature 
  * **pres** output Pressure 
  * **pres_ratio** Output pressure ratio 
  * **rho_ratio** Output density ratio 


**See**: [ATMOS_TYPE](Modules/group___enumerations.md#enum-atmos-type)

Calculate the atmospheric properties determined by a specified model at input altitude and temperature deviation. This function may not be used for any manual atmospheric model types (i.e. ATMOS_TYPE_MANUAL_P_T). This function assumes freestream units are metric, temperature units are Kelvin, and pressure units are kPA. 

double temp, pres, pres_ratio, rho_ratio;

double alt = 4000;

double delta_temp = 0;

CalcAtmosphere( alt, delta_temp, ATMOS_TYPE_US_STANDARD_1976, temp, pres, pres_ratio, rho_ratio );
```

 \endforcpponly \beginPythonOnly ```py

alt = 4000

delta_temp = 0

temp, pres, pres_ratio, rho_ratio = CalcAtmosphere( alt, delta_temp, ATMOS_TYPE_US_STANDARD_1976)
```

  


### function WriteBodyFFCSVFile

```
void WriteBodyFFCSVFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** Output CSV file 


Calculate the form factor from each body FF equation (i.e. Hoerner Streamlined Body) and write the results to a CSV output file 

Print( "Starting Body Form Factor Data Creation. \n" );
WriteBodyFFCSVFile( "BodyFormFactorData.csv" );
```

 \endforcpponly \beginPythonOnly ```py

print( "Starting Body Form Factor Data Creation. \n" )
WriteBodyFFCSVFile( "BodyFormFactorData.csv" )
```

  


### function WriteWingFFCSVFile

```
void WriteWingFFCSVFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** Output CSV file 


Calculate the form factor from each wing FF equation (i.e. Schemensky 4 Series Airfoil) and write the results to a CSV output file 

Print( "Starting Wing Form Factor Data Creation. \n" );
WriteWingFFCSVFile( "WingFormFactorData.csv" );
```

 \endforcpponly \beginPythonOnly ```py

print( "Starting Wing Form Factor Data Creation. \n" )
WriteWingFFCSVFile( "WingFormFactorData.csv" )
```

  


### function WriteCfEqnCSVFile

```
void WriteCfEqnCSVFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** Output CSV file 


Calculate the coefficient of friction from each Cf equation (i.e. Power Law Blasius) and write the results to a CSV output file 

Print( "Starting Turbulent Friciton Coefficient Data Creation. \n" );
WriteCfEqnCSVFile( "FrictionCoefficientData.csv" );
```

 \endforcpponly \beginPythonOnly ```py

print( "Starting Turbulent Friciton Coefficient Data Creation. \n" )
WriteCfEqnCSVFile( "FrictionCoefficientData.csv" )
```

  


### function WritePartialCfMethodCSVFile

```
void WritePartialCfMethodCSVFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** Output CSV file 


Calculate the partial coefficient of friction and write the results to a CSV output file 

Print( "Starting Partial Friction Method Data Creation. \n" );
WritePartialCfMethodCSVFile( "PartialFrictionMethodData.csv" );
```

 \endforcpponly \beginPythonOnly ```py

print( "Starting Partial Friction Method Data Creation. \n" )
WritePartialCfMethodCSVFile( "PartialFrictionMethodData.csv" )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800