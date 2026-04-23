---
title: Results Manager Functions
summary: This group is for functions included in the Results Manager. The Results Manager stores analysis results and provides methods to get, print, and export them. Click here to return to the main page. 

---

# Results Manager Functions

This group is for functions included in the Results Manager. The Results Manager stores analysis results and provides methods to get, print, and export them. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::vector< std::string > | **[GetAllResultsNames](Modules/group___results.md#function-getallresultsnames)**() |
| std::vector< std::string > | **[GetAllDataNames](Modules/group___results.md#function-getalldatanames)**(const std::string & results_id) |
| int | **[GetNumResults](Modules/group___results.md#function-getnumresults)**(const std::string & name) |
| std::string | **[GetResultsName](Modules/group___results.md#function-getresultsname)**(const std::string & results_id) |
| std::string | **[GetResultsSetDoc](Modules/group___results.md#function-getresultssetdoc)**(const std::string & results_id) |
| std::string | **[FindResultsID](Modules/group___results.md#function-findresultsid)**(const std::string & name, int index =0) |
| std::string | **[FindLatestResultsID](Modules/group___results.md#function-findlatestresultsid)**(const std::string & name) |
| int | **[GetNumData](Modules/group___results.md#function-getnumdata)**(const std::string & results_id, const std::string & data_name) |
| int | **[GetResultsType](Modules/group___results.md#function-getresultstype)**(const std::string & results_id, const std::string & data_name) |
| const std::vector< int > & | **[GetIntResults](Modules/group___results.md#function-getintresults)**(const std::string & id, const std::string & name, int index =0) |
| const std::vector< double > & | **[GetDoubleResults](Modules/group___results.md#function-getdoubleresults)**(const std::string & id, const std::string & name, int index =0) |
| const std::vector< std::vector< double > > & | **[GetDoubleMatResults](Modules/group___results.md#function-getdoublematresults)**(const std::string & id, const std::string & name, int index =0) |
| const std::vector< std::string > & | **[GetStringResults](Modules/group___results.md#function-getstringresults)**(const std::string & id, const std::string & name, int index =0) |
| const std::vector< [vec3d](Classes/classvec3d.md) > & | **[GetVec3dResults](Modules/group___results.md#function-getvec3dresults)**(const std::string & id, const std::string & name, int index =0) |
| std::string | **[CreateGeomResults](Modules/group___results.md#function-creategeomresults)**(const std::string & geom_id, const std::string & name) |
| void | **[DeleteAllResults](Modules/group___results.md#function-deleteallresults)**() |
| void | **[DeleteResult](Modules/group___results.md#function-deleteresult)**(const std::string & id) |
| void | **[WriteResultsCSVFile](Modules/group___results.md#function-writeresultscsvfile)**(const std::string & id, const std::string & file_name) |
| void | **[PrintResults](Modules/group___results.md#function-printresults)**(const std::string & results_id) |
| void | **[PrintResultsDocs](Modules/group___results.md#function-printresultsdocs)**(const std::string & results_id) |
| void | **[WriteTestResults](Modules/group___results.md#function-writetestresults)**() |


## Functions Documentation

### function GetAllResultsNames

```
std::vector< std::string > GetAllResultsNames()
```


**Return**: Array of result names 

Get the name of all results in the Results Manager 

//==== Write Some Fake Test Results =====//
WriteTestResults();

array< string > @results_array = GetAllResultsNames();

for ( int i = 0; i < int( results_array.size() ); i++ )
{
    string resid = FindLatestResultsID( results_array[i] );
    PrintResults( resid );
}
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

results_array = GetAllResultsNames()

for i in range(int( len(results_array) )):

    resid = FindLatestResultsID( results_array[i] )
    PrintResults( resid )
```

  


### function GetAllDataNames

```
std::vector< std::string > GetAllDataNames(
    const std::string & results_id
)
```


**Parameters**: 

  * **results_id** Result ID 


**Return**: Array of result names 

Get all data names for a particular result 

//==== Write Some Fake Test Results =====//
WriteTestResults();

string res_id = FindResultsID( "Test_Results" );

array< string > @data_names = GetAllDataNames( res_id );

if ( data_names.size() != 5 )                            { Print( "---> Error: API GetAllDataNames" ); }
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

res_id = FindResultsID( "Test_Results" )

data_names = GetAllDataNames( res_id )

if  len(data_names) != 5 : print( "---> Error: API GetAllDataNames" )
```

  


### function GetNumResults

```
int GetNumResults(
    const std::string & name
)
```


**Parameters**: 

  * **name** Input name 


**Return**: Number of results 

Get the number of results for a particular result name 

//==== Write Some Fake Test Results =====//
WriteTestResults();

if ( GetNumResults( "Test_Results" ) != 2 )                { Print( "---> Error: API GetNumResults" ); }
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

if ( GetNumResults( "Test_Results" ) != 2 ): print( "---> Error: API GetNumResults" )
```

  


### function GetResultsName

```
std::string GetResultsName(
    const std::string & results_id
)
```


**Parameters**: 

  * **results_id** Result ID 


**Return**: Result name 

Get the name of a result given its ID 

//==== Analysis: VSPAero Compute Geometry ====//
string analysis_name = "VSPAEROComputeGeometry";

// Set defaults
SetAnalysisInputDefaults( analysis_name );

string res_id = ( ExecAnalysis( analysis_name ) );

Print( "Results Name: ", false );

Print( GetResultsName( res_id ) );
```

 

#==== Analysis: VSPAero Compute Geometry ====//
analysis_name = "VSPAEROComputeGeometry"

# Set defaults
SetAnalysisInputDefaults( analysis_name )

res_id = ( ExecAnalysis( analysis_name ) )

print( "Results Name: ", False )

print( GetResultsName( res_id ) )
```

  


### function GetResultsSetDoc

```
std::string GetResultsSetDoc(
    const std::string & results_id
)
```


**Parameters**: 

  * **results_id** Result ID 


**Return**: Result documentation string 

Get the documentation string for a result given its ID 

//==== Analysis: VSPAero Compute Geometry ====//
string analysis_name = "VSPAEROComputeGeometry";

// Set defaults
SetAnalysisInputDefaults( analysis_name );

string res_id = ( ExecAnalysis( analysis_name ) );

Print( "Results doc: ", false );

Print( GetResultsSetDoc( res_id ) );
```

 

#==== Analysis: VSPAero Compute Geometry ====//
analysis_name = "VSPAEROComputeGeometry"

# Set defaults
SetAnalysisInputDefaults( analysis_name )

res_id = ( ExecAnalysis( analysis_name ) )

print( "Results doc: ", False )

print( GetResultsSetDoc( res_id ) )
```

  


### function FindResultsID

```
std::string FindResultsID(
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **name** Result name 
  * **index** Result index 


**Return**: Result ID 

Find a results ID given its name and index 

//==== Write Some Fake Test Results =====//
WriteTestResults();

string res_id = FindResultsID( "Test_Results" );

if ( res_id.size() == 0 )                                { Print( "---> Error: API FindResultsID" ); }
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

res_id = FindResultsID( "Test_Results" )

if  len(res_id) == 0 : print( "---> Error: API FindResultsID" )
```

  


### function FindLatestResultsID

```
std::string FindLatestResultsID(
    const std::string & name
)
```


**Parameters**: 

  * **name** Result name 


**Return**: Result ID 

Find the latest results ID for particular result name 

//==== Write Some Fake Test Results =====//
WriteTestResults();

array< string > @results_array = GetAllResultsNames();

for ( int i = 0; i < int( results_array.size() ); i++ )
{
    string resid = FindLatestResultsID( results_array[i] );
    PrintResults( resid );
}
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

results_array = GetAllResultsNames()

for i in range(int( len(results_array) )):

    resid = FindLatestResultsID( results_array[i] )
    PrintResults( resid )
```

  


### function GetNumData

```
int GetNumData(
    const std::string & results_id,
    const std::string & data_name
)
```


**Parameters**: 

  * **results_id** Result ID 
  * **data_name** Data name 


**Return**: Number of data values 

Get the number of data values for a given result ID and data name 

//==== Write Some Fake Test Results =====//
WriteTestResults();

string res_id = FindResultsID( "Test_Results" );

if ( GetNumData( res_id, "Test_Int" ) != 2 )            { Print( "---> Error: API GetNumData " ); }

array<int> @int_arr = GetIntResults( res_id, "Test_Int", 0 );

if ( int_arr[0] != 1 )                                    { Print( "---> Error: API GetIntResults" ); }

int_arr = GetIntResults( res_id, "Test_Int", 1 );

if ( int_arr[0] != 2 )                                    { Print( "---> Error: API GetIntResults" ); }
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

res_id = FindResultsID( "Test_Results" )

if ( GetNumData( res_id, "Test_Int" ) != 2 ): print( "---> Error: API GetNumData " )

int_arr = GetIntResults( res_id, "Test_Int", 0 )

if  int_arr[0] != 1 : print( "---> Error: API GetIntResults" )

int_arr = GetIntResults( res_id, "Test_Int", 1 )

if  int_arr[0] != 2 : print( "---> Error: API GetIntResults" )
```

  


### function GetResultsType

```
int GetResultsType(
    const std::string & results_id,
    const std::string & data_name
)
```


**Parameters**: 

  * **results_id** Result ID 
  * **data_name** Data name 


**See**: [RES_DATA_TYPE](Modules/group___enumerations.md#enum-res-data-type)

**Return**: Data type enum (i.e. DOUBLE_DATA) 

Get the data type for a given result ID and data name 

//==== Write Some Fake Test Results =====//
WriteTestResults();

string res_id = FindResultsID( "Test_Results" );

array < string > @ res_array = GetAllDataNames( res_id );

for ( int j = 0; j < int( res_array.size() ); j++ )
{
    int typ = GetResultsType( res_id, res_array[j] );
}
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

res_id = FindResultsID( "Test_Results" )

res_array = GetAllDataNames( res_id )

for j in range(int( len(res_array) )):

    typ = GetResultsType( res_id, res_array[j] )
```

  


### function GetIntResults

```
const std::vector< int > & GetIntResults(
    const std::string & id,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **id** Result ID 
  * **name** Data name 
  * **index** Data index 


**Return**: Array of data values 

Get all integer values for a particular result, name, and index 

//==== Write Some Fake Test Results =====//
WriteTestResults();

string res_id = FindResultsID( "Test_Results" );

if ( GetNumData( res_id, "Test_Int" ) != 2 )            { Print( "---> Error: API GetNumData " ); }

array<int> @int_arr = GetIntResults( res_id, "Test_Int", 0 );

if ( int_arr[0] != 1 )                                    { Print( "---> Error: API GetIntResults" ); }

int_arr = GetIntResults( res_id, "Test_Int", 1 );

if ( int_arr[0] != 2 )                                    { Print( "---> Error: API GetIntResults" ); }
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

res_id = FindResultsID( "Test_Results" )

if ( GetNumData( res_id, "Test_Int" ) != 2 ): print( "---> Error: API GetNumData " )

int_arr = GetIntResults( res_id, "Test_Int", 0 )

if  int_arr[0] != 1 : print( "---> Error: API GetIntResults" )

int_arr = GetIntResults( res_id, "Test_Int", 1 )

if  int_arr[0] != 2 : print( "---> Error: API GetIntResults" )
```

  


### function GetDoubleResults

```
const std::vector< double > & GetDoubleResults(
    const std::string & id,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **id** Result ID 
  * **name** Data name 
  * **index** Data index 


**Return**: Array of data values 

Get all double values for a particular result, name, and index 

//==== Add Pod Geom ====//
string pid = AddGeom( "POD", "" );

//==== Run CompGeom And View Results ====//
string mesh_id = ComputeCompGeom( SET_ALL, false, 0 );                      // Half Mesh false and no file export

string comp_res_id = FindLatestResultsID( "Comp_Geom" );                    // Find Results ID

array<double> @double_arr = GetDoubleResults( comp_res_id, "Wet_Area" );    // Extract Results
```

 

#==== Add Pod Geom ====//
pid = AddGeom( "POD", "" )

#==== Run CompGeom And View Results ====//
mesh_id = ComputeCompGeom( SET_ALL, False, 0 )                      # Half Mesh false and no file export

comp_res_id = FindLatestResultsID( "Comp_Geom" )                    # Find Results ID

double_arr = GetDoubleResults( comp_res_id, "Wet_Area" )    # Extract Results
```

  


### function GetDoubleMatResults

```
const std::vector< std::vector< double > > & GetDoubleMatResults(
    const std::string & id,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **id** Result ID 
  * **name** Data name 
  * **index** Data index 


**Return**: 2D array of data values 

Get all matrix (vector<vector<double>>) values for a particular result, name, and index 


### function GetStringResults

```
const std::vector< std::string > & GetStringResults(
    const std::string & id,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **id** Result ID 
  * **name** Data name 
  * **index** Data index 


**Return**: Array of data values 

Get all string values for a particular result, name, and index 

//==== Write Some Fake Test Results =====//
WriteTestResults();

string res_id = FindResultsID( "Test_Results" );

array<string> @str_arr = GetStringResults( res_id, "Test_String" );

if ( str_arr[0] != "This Is A Test" )                    { Print( "---> Error: API GetStringResults" ); }
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

res_id = FindResultsID( "Test_Results" )

str_arr = GetStringResults( res_id, "Test_String" )

if ( str_arr[0] != "This Is A Test" ): print( "---> Error: API GetStringResults" )
```

  


### function GetVec3dResults

```
const std::vector< vec3d > & GetVec3dResults(
    const std::string & id,
    const std::string & name,
    int index =0
)
```


**Parameters**: 

  * **id** Result ID 
  * **name** Data name 
  * **index** Data index 


**Return**: Array of data values 

Get all [vec3d](Classes/classvec3d.md) values for a particular result, name, and index 

//==== Write Some Fake Test Results =====//

double tol = 0.00001;

WriteTestResults();

string res_id = FindLatestResultsID( "Test_Results" );

array<vec3d> @vec3d_vec = GetVec3dResults( res_id, "Test_Vec3d" );

Print( "X: ", false );
Print( vec3d_vec[0].x(), false );

Print( "\tY: ", false );
Print( vec3d_vec[0].y(), false );

Print( "\tZ: ", false );
Print( vec3d_vec[0].z() );
```

 

#==== Write Some Fake Test Results =====//

tol = 0.00001

WriteTestResults()

res_id = FindLatestResultsID( "Test_Results" )

vec3d_vec = GetVec3dResults( res_id, "Test_Vec3d" )

print( "X: ", False )
print( vec3d_vec[0].x(), False )

print( "\tY: ", False )
print( vec3d_vec[0].y(), False )

print( "\tZ: ", False )
print( vec3d_vec[0].z() )
```

  


### function CreateGeomResults

```
std::string CreateGeomResults(
    const std::string & geom_id,
    const std::string & name
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **name** Result name 


**Return**: Result ID 

Create a new result for a Geom 

//==== Test Comp Geom ====//
string gid1 = AddGeom( "POD", "" );

string mesh_id = ComputeCompGeom( 0, false, 0 );

//==== Test Comp Geom Mesh Results ====//
string mesh_geom_res_id = CreateGeomResults( mesh_id, "Comp_Mesh" );

array<int> @int_arr = GetIntResults( mesh_geom_res_id, "Num_Tris" );

if ( int_arr[0] < 4 )                                            { Print( "---> Error: API CreateGeomResults" ); }
```

 

#==== Test Comp Geom ====//
gid1 = AddGeom( "POD", "" )

mesh_id = ComputeCompGeom( 0, False, 0 )

#==== Test Comp Geom Mesh Results ====//
mesh_geom_res_id = CreateGeomResults( mesh_id, "Comp_Mesh" )

int_arr = GetIntResults( mesh_geom_res_id, "Num_Tris" )

if  int_arr[0] < 4 : print( "---> Error: API CreateGeomResults" )
```

  


### function DeleteAllResults

```
void DeleteAllResults()
```


Delete all results 

//==== Test Comp Geom ====//
string gid1 = AddGeom( "POD", "" );

string mesh_id = ComputeCompGeom( 0, false, 0 );

//==== Test Comp Geom Mesh Results ====//
string mesh_geom_res_id = CreateGeomResults( mesh_id, "Comp_Mesh" );

DeleteAllResults();

if ( GetNumResults( "Comp_Mesh" ) != 0 )                { Print( "---> Error: API DeleteAllResults" ); }
```

 

#==== Test Comp Geom ====//
gid1 = AddGeom( "POD", "" )

mesh_id = ComputeCompGeom( 0, False, 0 )

#==== Test Comp Geom Mesh Results ====//
mesh_geom_res_id = CreateGeomResults( mesh_id, "Comp_Mesh" )

DeleteAllResults()

if ( GetNumResults( "Comp_Mesh" ) != 0 ): print( "---> Error: API DeleteAllResults" )
```

  


### function DeleteResult

```
void DeleteResult(
    const std::string & id
)
```


**Parameters**: 

  * **id** Result ID 


Delete a particular result 

//==== Test Comp Geom ====//
string gid1 = AddGeom( "POD", "" );

string mesh_id = ComputeCompGeom( 0, false, 0 );

//==== Test Comp Geom Mesh Results ====//
string mesh_geom_res_id = CreateGeomResults( mesh_id, "Comp_Mesh" );

DeleteResult( mesh_geom_res_id );

if ( GetNumResults( "Comp_Mesh" ) != 0 )                { Print( "---> Error: API DeleteResult" ); }
```

 

#==== Test Comp Geom ====//
gid1 = AddGeom( "POD", "" )

mesh_id = ComputeCompGeom( 0, False, 0 )

#==== Test Comp Geom Mesh Results ====//
mesh_geom_res_id = CreateGeomResults( mesh_id, "Comp_Mesh" )

DeleteResult( mesh_geom_res_id )

if ( GetNumResults( "Comp_Mesh" ) != 0 ): print( "---> Error: API DeleteResult" )
```

  


### function WriteResultsCSVFile

```
void WriteResultsCSVFile(
    const std::string & id,
    const std::string & file_name
)
```


**Parameters**: 

  * **id** Rsult ID 
  * **file_name** CSV output file name 


Export a result to CSV 

// Add Pod Geom
string pid = AddGeom( "POD" );

string analysis_name = "VSPAEROComputeGeometry";

string rid = ExecAnalysis( analysis_name );

WriteResultsCSVFile( rid, "CompGeomRes.csv" );
```

 

# Add Pod Geom
pid = AddGeom( "POD" )

analysis_name = "VSPAEROComputeGeometry"

rid = ExecAnalysis( analysis_name )

WriteResultsCSVFile( rid, "CompGeomRes.csv" )
```

  


### function PrintResults

```
void PrintResults(
    const std::string & results_id
)
```


**Parameters**: 

  * **results_id** string Result ID 


Print a result's name value pairs to stdout 

// Add Pod Geom
string pid = AddGeom( "POD" );

string analysis_name = "VSPAEROComputeGeometry";

string rid = ExecAnalysis( analysis_name );

// Get & Display Results
PrintResults( rid );
```

 

# Add Pod Geom
pid = AddGeom( "POD" )

analysis_name = "VSPAEROComputeGeometry"

rid = ExecAnalysis( analysis_name )

# Get & Display Results
PrintResults( rid )
```

  


### function PrintResultsDocs

```
void PrintResultsDocs(
    const std::string & results_id
)
```


**Parameters**: 

  * **results_id** string Result ID 


Print a result's names and documentation to stdout 

// Add Pod Geom
string pid = AddGeom( "POD" );

string analysis_name = "VSPAEROComputeGeometry";

string rid = ExecAnalysis( analysis_name );

// Get & Display Results Docs
PrintResultsDoc( rid );
```

 

# Add Pod Geom
pid = AddGeom( "POD" )

analysis_name = "VSPAEROComputeGeometry"

rid = ExecAnalysis( analysis_name )

# Get & Display Results Docs
PrintResultsDocs( rid )
```

  


### function WriteTestResults

```
void WriteTestResults()
```


Generate some example results for testing. 

//==== Write Some Fake Test Results =====//
WriteTestResults();

array< string > @results_array = GetAllResultsNames();

for ( int i = 0; i < int( results_array.size() ); i++ )
{
    string resid = FindLatestResultsID( results_array[i] );
    PrintResults( resid );
}
```

 

#==== Write Some Fake Test Results =====//
WriteTestResults()

results_array = GetAllResultsNames()

for i in range( len( results_array ) ):
    resid = FindLatestResultsID( results_array[i] )
    PrintResults( resid )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800