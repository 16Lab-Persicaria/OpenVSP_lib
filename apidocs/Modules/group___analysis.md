---
title: Analysis Manager Functions
summary: This group is for functions included in the Analysis Manager. The Analysis Manager allows for OpenVSP analyses to be setup and run through the API without having to modify Parms directly. Examples are available for every available analysis type. The results of running an analysis can be accessed through the functions defined in the Results group. Click here to return to the main page. 

---

# Analysis Manager Functions

This group is for functions included in the Analysis Manager. The Analysis Manager allows for OpenVSP analyses to be setup and run through the API without having to modify Parms directly. Examples are available for every available analysis type. The results of running an analysis can be accessed through the functions defined in the Results group. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| int | **[GetNumAnalysis](Modules/group___analysis.md#function-getnumanalysis)**() |
| std::vector< std::string > | **[ListAnalysis](Modules/group___analysis.md#function-listanalysis)**() |
| std::vector< std::string > | **[GetAnalysisInputNames](Modules/group___analysis.md#function-getanalysisinputnames)**(const std::string & analysis) |
| std::string | **[GetAnalysisDoc](Modules/group___analysis.md#function-getanalysisdoc)**(const std::string & analysis) |
| std::string | **[GetAnalysisInputDoc](Modules/group___analysis.md#function-getanalysisinputdoc)**(const std::string & analysis, const std::string & name) |
| std::string | **[ExecAnalysis](Modules/group___analysis.md#function-execanalysis)**(const std::string & analysis) |
| int | **[GetNumAnalysisInputData](Modules/group___analysis.md#function-getnumanalysisinputdata)**(const std::string & analysis, const std::string & name) |
| int | **[GetAnalysisInputType](Modules/group___analysis.md#function-getanalysisinputtype)**(const std::string & analysis, const std::string & name) |
| const std::vector< int > & | **[GetIntAnalysisInput](Modules/group___analysis.md#function-getintanalysisinput)**(const std::string & analysis, const std::string & name, int index =0) |
| const std::vector< double > & | **[GetDoubleAnalysisInput](Modules/group___analysis.md#function-getdoubleanalysisinput)**(const std::string & analysis, const std::string & name, int index =0) |
| const std::vector< std::string > & | **[GetStringAnalysisInput](Modules/group___analysis.md#function-getstringanalysisinput)**(const std::string & analysis, const std::string & name, int index =0) |
| const std::vector< vec3d > & | **[GetVec3dAnalysisInput](Modules/group___analysis.md#function-getvec3danalysisinput)**(const std::string & analysis, const std::string & name, int index =0) |
| void | **[SetAnalysisInputDefaults](Modules/group___analysis.md#function-setanalysisinputdefaults)**(const std::string & analysis) |
| void | **[SetIntAnalysisInput](Modules/group___analysis.md#function-setintanalysisinput)**(const std::string & analysis, const std::string & name, const std::vector< int > & indata, int index =0) |
| void | **[SetDoubleAnalysisInput](Modules/group___analysis.md#function-setdoubleanalysisinput)**(const std::string & analysis, const std::string & name, const std::vector< double > & indata, int index =0) |
| void | **[SetStringAnalysisInput](Modules/group___analysis.md#function-setstringanalysisinput)**(const std::string & analysis, const std::string & name, const std::vector< std::string > & indata, int index =0) |
| void | **[SetVec3dAnalysisInput](Modules/group___analysis.md#function-setvec3danalysisinput)**(const std::string & analysis, const std::string & name, const std::vector< vec3d > & indata, int index =0) |
| void | **[PrintAnalysisInputs](Modules/group___analysis.md#function-printanalysisinputs)**(const std::string & analysis_name) |
| void | **[PrintAnalysisDocs](Modules/group___analysis.md#function-printanalysisdocs)**(const std::string & analysis_name) |


## Functions Documentation

### function GetNumAnalysis

```
int GetNumAnalysis()
```


**Return**: Number of analyses 

Get the number of analysis types available in the Analysis Manager 

int nanalysis = GetNumAnalysis();

Print( "Number of registered analyses: " + nanalysis );
```

 \endforcpponly \beginPythonOnly ```py

nanalysis = GetNumAnalysis()

print( f"Number of registered analyses: {nanalysis}" )
```

  


### function ListAnalysis

```
std::vector< std::string > ListAnalysis()
```


**Return**: Array of analysis names 

Get the name of every available analysis in the Analysis Manager 

array< string > @analysis_array = ListAnalysis();

Print( "List of Available Analyses: " );

for ( int i = 0; i < int( analysis_array.size() ); i++ )
{
    Print( "    " + analysis_array[i] );
}
```

 \endforcpponly \beginPythonOnly ```py

analysis_array = ListAnalysis()

print( "List of Available Analyses: " )

for i in range(int( len(analysis_array) )):

    print( "    " + analysis_array[i] )
```

  


### function GetAnalysisInputNames

```
std::vector< std::string > GetAnalysisInputNames(
    const std::string & analysis
)
```


**Parameters**: 

  * **analysis** Analysis name 


**Return**: Array of input names 

Get the name of every available input for a particular analysis 

string analysis_name = "VSPAEROComputeGeometry";

array<string>@ in_names =  GetAnalysisInputNames( analysis_name );

Print("Analysis Inputs: ");

for ( int i = 0; i < int( in_names.size() ); i++)
{
    Print( ( "\t" + in_names[i] + "\n" ) );
}
```

 \endforcpponly \beginPythonOnly ```py

analysis_name = "VSPAEROComputeGeometry"

in_names =  GetAnalysisInputNames( analysis_name )

print("Analysis Inputs: ")

for i in range(int( len(in_names) )):

    print( ( "\t" + in_names[i] + "\n" ) )
```

  


### function GetAnalysisDoc

```
std::string GetAnalysisDoc(
    const std::string & analysis
)
```


**Parameters**: 

  * **analysis** Analysis name 


**Return**: Documentation string 

Get the analysis documentation string 

string analysis_name = "VSPAEROComputeGeometry";

string doc = GetAnalysisDoc( analysis_name );
```

 \endforcpponly \beginPythonOnly ```py

analysis_name = "VSPAEROComputeGeometry"

doc = GetAnalysisDoc( analysis_name )
```

  


### function GetAnalysisInputDoc

```
std::string GetAnalysisInputDoc(
    const std::string & analysis,
    const std::string & name
)
```


**Parameters**: 

  * **analysis** Analysis name 
  * **name** Input name 


**Return**: Documentation string 

Get the documentation string for the particular analysis and input \forcpponly

\endforcpponly \beginPythonOnly

 


### function ExecAnalysis

```
std::string ExecAnalysis(
    const std::string & analysis
)
```


**Parameters**: 

  * **analysis** Analysis name 


**Return**: Result ID 

Execute an analysis through the Analysis Manager 

string analysis_name = "VSPAEROComputeGeometry";

string res_id = ExecAnalysis( analysis_name );
```

 \endforcpponly \beginPythonOnly ```py

analysis_name = "VSPAEROComputeGeometry"

res_id = ExecAnalysis( analysis_name )
```

  


### function GetNumAnalysisInputData

```
int GetNumAnalysisInputData(
    const std::string & analysis,
    const std::string & name
)
```


**Parameters**: 

  * **analysis** Analysis name 
  * **name** Input name 


**Return**: Documentation string 

Get the documentation string for the particular analysis and input 


### function GetAnalysisInputType

```
int GetAnalysisInputType(
    const std::string & analysis,
    const std::string & name
)
```


**Parameters**: 

  * **analysis** Analysis name 
  * **name** Input name 


**See**: [RES_DATA_TYPE](Modules/group___enumerations.md#enum-res-data-type)

**Return**: int Data type enum (i.e. DOUBLE_DATA) 

Get the data type for a particulat analysis type and input 

string analysis = "VSPAEROComputeGeometry";

array < string > @ inp_array = GetAnalysisInputNames( analysis );

for ( int j = 0; j < int( inp_array.size() ); j++ )
{
    int typ = GetAnalysisInputType( analysis, inp_array[j] );
}
```

 \endforcpponly \beginPythonOnly ```py

analysis = "VSPAEROComputeGeometry"

inp_array = GetAnalysisInputNames( analysis )

for j in range(int( len(inp_array) )):

    typ = GetAnalysisInputType( analysis, inp_array[j] )
```

  


### function GetIntAnalysisInput

```
const std::vector< int > & GetIntAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **index** int Data index 


**See**: [RES_DATA_TYPE](Modules/group___enumerations.md#enum-res-data-type), [SetIntAnalysisInput](Modules/group___analysis.md#function-setintanalysisinput)

**Return**: vector<int> Array of analysis input values 

Get the current integer values for the particular analysis, input, and data index 

//==== Analysis: VSPAero Compute Geometry ====//
string analysis_name = "VSPAEROComputeGeometry";

// Set to panel method
array< int > thick_set = GetIntAnalysisInput( analysis_name, "GeomSet" );
array< int > thin_set = GetIntAnalysisInput( analysis_name, "ThinGeomSet" );

thick_set[0] = ( SET_TYPE::SET_NONE );
thin_set[0] = ( SET_TYPE::SET_ALL );

SetIntAnalysisInput( analysis_name, "GeomSet", thick_set, 0);
SetIntAnalysisInput( analysis_name, "ThinGeomSet", thin_set, 0);
```

 \endforcpponly \beginPythonOnly ```py

#==== Analysis: VSPAero Compute Geometry ====//
analysis_name = "VSPAEROComputeGeometry"

# Set to panel method
thick_set = GetIntAnalysisInput( analysis_name, "GeomSet" )
thin_set = GetIntAnalysisInput( analysis_name, "ThinGeomSet" )

thick_set = [vsp.SET_NONE]
thin_set = [vsp.SET_ALL]

SetIntAnalysisInput( analysis_name, "GeomSet", thick_set )
SetIntAnalysisInput( analysis_name, "ThinGeomSet", thin_set )
```

  


### function GetDoubleAnalysisInput

```
const std::vector< double > & GetDoubleAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **index** int Data index 


**See**: [RES_DATA_TYPE](Modules/group___enumerations.md#enum-res-data-type), [SetDoubleAnalysisInput](Modules/group___analysis.md#function-setdoubleanalysisinput)

**Return**: vector<double> Array of analysis input values 

Get the current double values for the particular analysis, input, and data index 

array<double> vinfFCinput = GetDoubleAnalysisInput( "ParasiteDrag", "Vinf" );

vinfFCinput[0] = 629;

SetDoubleAnalysisInput( "ParasiteDrag", "Vinf", vinfFCinput );
```

 \endforcpponly \beginPythonOnly ```py

vinfFCinput = list( GetDoubleAnalysisInput( "ParasiteDrag", "Vinf" ) )

vinfFCinput[0] = 629

SetDoubleAnalysisInput( "ParasiteDrag", "Vinf", vinfFCinput )
```

  


### function GetStringAnalysisInput

```
const std::vector< std::string > & GetStringAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **index** int Data index 


**See**: [RES_DATA_TYPE](Modules/group___enumerations.md#enum-res-data-type), [SetStringAnalysisInput](Modules/group___analysis.md#function-setstringanalysisinput)

**Return**: vector<string> Array of analysis input values 

Get the current string values for the particular analysis, input, and data index 

array<string> fileNameInput = GetStringAnalysisInput( "ParasiteDrag", "FileName" );

fileNameInput[0] = "ParasiteDragExample";

SetStringAnalysisInput( "ParasiteDrag", "FileName", fileNameInput );
```

 \endforcpponly \beginPythonOnly ```py

fileNameInput = GetStringAnalysisInput( "ParasiteDrag", "FileName" )

fileNameInput = ["ParasiteDragExample"]

SetStringAnalysisInput( "ParasiteDrag", "FileName", fileNameInput )
```

  


### function GetVec3dAnalysisInput

```
const std::vector< vec3d > & GetVec3dAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **index** int Data index 


**See**: [RES_DATA_TYPE](Modules/group___enumerations.md#enum-res-data-type), [SetVec3dAnalysisInput](Modules/group___analysis.md#function-setvec3danalysisinput)

**Return**: vector<vec3d> Array of analysis input values 

Get the current vec3d values for the particular analysis, input, and data index 

// PlanarSlice
array<vec3d> norm = GetVec3dAnalysisInput( "PlanarSlice", "Norm" );

norm[0].set_xyz( 0.23, 0.6, 0.15 );

SetVec3dAnalysisInput( "PlanarSlice", "Norm", norm );
```

 \endforcpponly \beginPythonOnly ```py

# PlanarSlice
norm = GetVec3dAnalysisInput( "PlanarSlice", "Norm" )

norm[0].set_xyz( 0.23, 0.6, 0.15 )

SetVec3dAnalysisInput( "PlanarSlice", "Norm", norm )
```

  


### function SetAnalysisInputDefaults

```
void SetAnalysisInputDefaults(
    const std::string & analysis
)
```


**Parameters**: 

  * **analysis** Analysis name 


Set all input values to their defaults for a specific analysis 

//==== Analysis: VSPAero Compute Geometry ====//
string analysis_name = "VSPAEROComputeGeometry";

// Set defaults
SetAnalysisInputDefaults( analysis_name );
```

 \endforcpponly \beginPythonOnly ```py

#==== Analysis: VSPAero Compute Geometry ====//
analysis_name = "VSPAEROComputeGeometry"

# Set defaults
SetAnalysisInputDefaults( analysis_name )
```

  


### function SetIntAnalysisInput

```
void SetIntAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    const std::vector< int > & indata,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **indata** vector<int> Array of integer values to set the input to 
  * **index** int Data index 


**See**: [GetIntAnalysisInput](Modules/group___analysis.md#function-getintanalysisinput)

Set the value of a particular analysis input of integer type 

//==== Analysis: VSPAero Compute Geometry ====//
string analysis_name = "VSPAEROComputeGeometry";

// Set to panel method
array< int > thick_set = GetIntAnalysisInput( analysis_name, "GeomSet" );
array< int > thin_set = GetIntAnalysisInput( analysis_name, "ThinGeomSet" );

thick_set[0] = ( SET_TYPE::SET_NONE );
thin_set[0] = ( SET_TYPE::SET_ALL );

SetIntAnalysisInput( analysis_name, "GeomSet", thick_set, 0);
SetIntAnalysisInput( analysis_name, "ThinGeomSet", thin_set, 0);
```

 \endforcpponly \beginPythonOnly ```py

#==== Analysis: VSPAero Compute Geometry ====//
analysis_name = "VSPAEROComputeGeometry"

# Set to panel method
thick_set = GetIntAnalysisInput( analysis_name, "GeomSet" )
thin_set = GetIntAnalysisInput( analysis_name, "ThinGeomSet" )

thick_set = [vsp.SET_NONE]
thin_set = [vsp.SET_ALL]

SetIntAnalysisInput( analysis_name, "GeomSet", thick_set )
SetIntAnalysisInput( analysis_name, "ThinGeomSet", thin_set )
```

  


### function SetDoubleAnalysisInput

```
void SetDoubleAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    const std::vector< double > & indata,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **indata** vector<double> Array of double values to set the input to 
  * **index** int Data index 


**See**: [GetDoubleAnalysisInput](Modules/group___analysis.md#function-getdoubleanalysisinput)

Set the value of a particular analysis input of double type 

//==== Analysis: CpSlicer ====//
string analysis_name = "CpSlicer";

// Setup cuts
array < double > ycuts;
ycuts.push_back( 2.0 );
ycuts.push_back( 4.5 );
ycuts.push_back( 8.0 );

SetDoubleAnalysisInput( analysis_name, "YSlicePosVec", ycuts, 0 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Analysis: CpSlicer ====//
analysis_name = "CpSlicer"

# Setup cuts
ycuts = []
ycuts.append( 2.0 )
ycuts.append( 4.5 )
ycuts.append( 8.0 )

SetDoubleAnalysisInput( analysis_name, "YSlicePosVec", ycuts, 0 )
```

  


### function SetStringAnalysisInput

```
void SetStringAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    const std::vector< std::string > & indata,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **indata** vector<string> Array of string values to set the input to 
  * **index** int Data index 


**See**: [GetStringAnalysisInput](Modules/group___analysis.md#function-getstringanalysisinput)

Set the value of a particular analysis input of string type 

array<string> fileNameInput = GetStringAnalysisInput( "ParasiteDrag", "FileName" );

fileNameInput[0] = "ParasiteDragExample";

SetStringAnalysisInput( "ParasiteDrag", "FileName", fileNameInput );
```

 \endforcpponly \beginPythonOnly ```py

fileNameInput = GetStringAnalysisInput( "ParasiteDrag", "FileName" )

fileNameInput = ["ParasiteDragExample"]

SetStringAnalysisInput( "ParasiteDrag", "FileName", fileNameInput )
```

  


### function SetVec3dAnalysisInput

```
void SetVec3dAnalysisInput(
    const std::string & analysis,
    const std::string & name,
    const std::vector< vec3d > & indata,
    int index =0
)
```


**Parameters**: 

  * **analysis** string Analysis name 
  * **name** string Input name 
  * **indata** vector<vec3d> Array of vec3d values to set the input to 
  * **index** int Data index 


**See**: [GetVec3dAnalysisInput](Modules/group___analysis.md#function-getvec3danalysisinput)

Set the value of a particular analysis input of vec3d type 

// PlanarSlice
array<vec3d> norm = GetVec3dAnalysisInput( "PlanarSlice", "Norm" );

norm[0].set_xyz( 0.23, 0.6, 0.15 );

SetVec3dAnalysisInput( "PlanarSlice", "Norm", norm );
```

 \endforcpponly \beginPythonOnly ```py

# PlanarSlice
norm = GetVec3dAnalysisInput( "PlanarSlice", "Norm" )

norm[0].set_xyz( 0.23, 0.6, 0.15 )

SetVec3dAnalysisInput( "PlanarSlice", "Norm", norm )
```

  


### function PrintAnalysisInputs

```
void PrintAnalysisInputs(
    const std::string & analysis_name
)
```


**Parameters**: 

  * **analysis_name** string Name of analysis 


Print to stdout all current input values for a specific analysis 

//==== Analysis: VSPAero Compute Geometry ====//
string analysis_name = "VSPAEROComputeGeometry";

// list inputs, type, and current values
PrintAnalysisInputs( analysis_name );
```

 \endforcpponly \beginPythonOnly ```py

#==== Analysis: VSPAero Compute Geometry ====//
analysis_name = "VSPAEROComputeGeometry"

# list inputs, type, and current values
PrintAnalysisInputs( analysis_name )
```

  


### function PrintAnalysisDocs

```
void PrintAnalysisDocs(
    const std::string & analysis_name
)
```


**Parameters**: 

  * **analysis_name** string Name of analysis 


Print to stdout all current input documentation for a specific analysis 

//==== Analysis: VSPAero Compute Geometry ====//
string analysis_name = "VSPAEROComputeGeometry";

// list inputs, type, and documentation
PrintAnalysisDocs( analysis_name );
```

 \endforcpponly \beginPythonOnly ```py

#==== Analysis: VSPAero Compute Geometry ====//
analysis_name = "VSPAEROComputeGeometry"

# list inputs, type, and documentation
PrintAnalysisDocs( analysis_name )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800