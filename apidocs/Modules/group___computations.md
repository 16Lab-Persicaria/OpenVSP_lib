---
title: General Computation Functions
summary: The following group of API functions are available for general computations. In general, it is best practice to perform computations through the the Analysis group instead of calling these functions directly. Click here to return to the main page. 

---

# General Computation Functions

The following group of API functions are available for general computations. In general, it is best practice to perform computations through the the Analysis group instead of calling these functions directly. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::string | **[ComputeMassProps](Modules/group___computations.md#function-computemassprops)**(int set, int num_slices, int idir) |
| std::string | **[ComputeCompGeom](Modules/group___computations.md#function-computecompgeom)**(int set, bool half_mesh, int file_export_types) |
| std::string | **[ComputePlaneSlice](Modules/group___computations.md#function-computeplaneslice)**(int set, int num_slices, const vec3d & norm, bool auto_bnd, double start_bnd =0, double end_bnd =0, bool measureduct =false) |
| void | **[ComputeDegenGeom](Modules/group___computations.md#function-computedegengeom)**(int set, int file_export_types) |


## Functions Documentation

### function ComputeMassProps

```
std::string ComputeMassProps(
    int set,
    int num_slices,
    int idir
)
```


**Parameters**: 

  * **set** Set index (i.e. SET_ALL) 
  * **num_slices** Number of slices 
  * **idir** Direction of slicing for integration 


**See**: [SetAnalysisInputDefaults](Modules/group___analysis.md#function-setanalysisinputdefaults), [PrintAnalysisInputs](Modules/group___analysis.md#function-printanalysisinputs), [ExecAnalysis](Modules/group___analysis.md#function-execanalysis)

**Return**: MeshGeom ID 

Compute mass properties for the components in the set. Alternatively can be run through the Analysis Manager with 'MassProp'. 

//==== Test Mass Props ====//
string pid = AddGeom( "POD", "" );

string mesh_id = ComputeMassProps( SET_ALL, 20, X_DIR );

string mass_res_id = FindLatestResultsID( "Mass_Properties" );

array<double> @double_arr = GetDoubleResults( mass_res_id, "Total_Mass" );

if ( double_arr.size() != 1 )                                    { Print( "---> Error: API ComputeMassProps" ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Test Mass Props ====//
pid = AddGeom( "POD", "" )

mesh_id = ComputeMassProps( SET_ALL, 20, X_DIR )

mass_res_id = FindLatestResultsID( "Mass_Properties" )

double_arr = GetDoubleResults( mass_res_id, "Total_Mass" )

if  len(double_arr) != 1 : print( "---> Error: API ComputeMassProps" )
```

  


### function ComputeCompGeom

```
std::string ComputeCompGeom(
    int set,
    bool half_mesh,
    int file_export_types
)
```


**Parameters**: 

  * **set** Set index (i.e. SET_ALL) 
  * **half_mesh** Flag to ignore surfaces on the negative side of the XZ plane (e.g. symmetry) 
  * **file_export_types** CompGeom file type to export (supports XOR i.e. COMP_GEOM_CSV_TYPE & COMP_GEOM_TXT_TYPE ) 


**See**: [SetAnalysisInputDefaults](Modules/group___analysis.md#function-setanalysisinputdefaults), [PrintAnalysisInputs](Modules/group___analysis.md#function-printanalysisinputs), [ExecAnalysis](Modules/group___analysis.md#function-execanalysis), [COMPUTATION_FILE_TYPE](Modules/group___enumerations.md#enum-computation-file-type)

**Return**: MeshGeom ID 

Mesh, intersect, and trim components in the set. Alternatively can be run through the Analysis Manager with 'CompGeom'. 

//==== Add Pod Geom ====//
string pid = AddGeom( "POD", "" );

//==== Run CompGeom And Get Results ====//
string mesh_id = ComputeCompGeom( SET_ALL, false, 0 );                      // Half Mesh false and no file export

string comp_res_id = FindLatestResultsID( "Comp_Geom" );                    // Find Results ID

array<double> @double_arr = GetDoubleResults( comp_res_id, "Wet_Area" );    // Extract Results
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geom ====//
pid = AddGeom( "POD", "" )

#==== Run CompGeom And Get Results ====//
mesh_id = ComputeCompGeom( SET_ALL, False, 0 )                      # Half Mesh false and no file export

comp_res_id = FindLatestResultsID( "Comp_Geom" )                    # Find Results ID

double_arr = GetDoubleResults( comp_res_id, "Wet_Area" )    # Extract Results
```

  


### function ComputePlaneSlice

```
std::string ComputePlaneSlice(
    int set,
    int num_slices,
    const vec3d & norm,
    bool auto_bnd,
    double start_bnd =0,
    double end_bnd =0,
    bool measureduct =false
)
```


**Parameters**: 

  * **set** Set index (i.e. SET_ALL) 
  * **num_slices** Number of slices 
  * **norm** Normal axis for all slices 
  * **auto_bnd** Flag to automatically set the start and end bound locations 
  * **start_bnd** Location of the first slice along the normal axis (default: 0.0) 
  * **end_bnd** Location of the last slice along the normal axis (default: 0.0) 
  * **measureduct** Flag to measure negative area inside positive area (default: false) 


**See**: [SetAnalysisInputDefaults](Modules/group___analysis.md#function-setanalysisinputdefaults), [PrintAnalysisInputs](Modules/group___analysis.md#function-printanalysisinputs), [ExecAnalysis](Modules/group___analysis.md#function-execanalysis)

**Return**: MeshGeom ID 

Slice and mesh the components in the set. Alternatively can be run through the Analysis Manager with 'PlanarSlice'. 

//==== Add Pod Geom ====//
string pid = AddGeom( "POD", "" );

//==== Test Plane Slice ====//
string slice_mesh_id = ComputePlaneSlice( 0, 6, vec3d( 0.0, 0.0, 1.0 ), true );

string pslice_results = FindLatestResultsID( "Slice" );

array<double> @double_arr = GetDoubleResults( pslice_results, "Slice_Area" );

if ( double_arr.size() != 6 )                                    { Print( "---> Error: API ComputePlaneSlice" ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geom ====//
pid = AddGeom( "POD", "" )

#==== Test Plane Slice ====//
slice_mesh_id = ComputePlaneSlice( 0, 6, vec3d( 0.0, 0.0, 1.0 ), True )

pslice_results = FindLatestResultsID( "Slice" )

double_arr = GetDoubleResults( pslice_results, "Slice_Area" )

if  len(double_arr) != 6 : print( "---> Error: API ComputePlaneSlice" )
```

  


### function ComputeDegenGeom

```
void ComputeDegenGeom(
    int set,
    int file_export_types
)
```


**Parameters**: 

  * **set** int Set index (i.e. SET_ALL) 
  * **file_export_types** int DegenGeom file type to export (supports XOR i.e DEGEN_GEOM_M_TYPE & DEGEN_GEOM_CSV_TYPE) 


**See**: [SetAnalysisInputDefaults](Modules/group___analysis.md#function-setanalysisinputdefaults), [PrintAnalysisInputs](Modules/group___analysis.md#function-printanalysisinputs), [ExecAnalysis](Modules/group___analysis.md#function-execanalysis), [COMPUTATION_FILE_TYPE](Modules/group___enumerations.md#enum-computation-file-type)

Compute the degenerate geometry representation for the components in the set. Alternatively can be run through the Analysis Manager with 'DegenGeom' or 'VSPAERODegenGeom'. 

//==== Set File Name ====//
SetComputationFileName( DEGEN_GEOM_CSV_TYPE, "TestDegenScript.csv" );

//==== Run Degen Geom ====//
ComputeDegenGeom( SET_ALL, DEGEN_GEOM_CSV_TYPE );
```

 \endforcpponly \beginPythonOnly ```py

#==== Set File Name ====//
SetComputationFileName( DEGEN_GEOM_CSV_TYPE, "TestDegenScript.csv" )

#==== Run Degen Geom ====//
ComputeDegenGeom( SET_ALL, DEGEN_GEOM_CSV_TYPE )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800