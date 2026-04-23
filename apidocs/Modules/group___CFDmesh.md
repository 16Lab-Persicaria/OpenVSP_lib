---
title: CFD Mesh Functions
summary: This group of functions is used to setup and run the CFD Mesh tool through the API. Click here to return to the main page. 

---

# CFD Mesh Functions

This group of functions is used to setup and run the CFD Mesh tool through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[SetComputationFileName](Modules/group___c_f_d_mesh.md#function-setcomputationfilename)**(int file_type, const std::string & file_name) |
| void | **[ComputeCFDMesh](Modules/group___c_f_d_mesh.md#function-computecfdmesh)**(int set, int degenset, int file_export_types) |
| void | **[SetCFDMeshVal](Modules/group___c_f_d_mesh.md#function-setcfdmeshval)**(int type, double val) |
| void | **[SetCFDWakeFlag](Modules/group___c_f_d_mesh.md#function-setcfdwakeflag)**(const std::string & geom_id, bool flag) |
| void | **[DeleteAllCFDSources](Modules/group___c_f_d_mesh.md#function-deleteallcfdsources)**() |
| void | **[AddDefaultSources](Modules/group___c_f_d_mesh.md#function-adddefaultsources)**() |
| void | **[AddCFDSource](Modules/group___c_f_d_mesh.md#function-addcfdsource)**(int type, const std::string & geom_id, int surf_index, double l1, double r1, double u1, double w1, double l2 =0, double r2 =0, double u2 =0, double w2 =0) |


## Functions Documentation

### function SetComputationFileName

```
void SetComputationFileName(
    int file_type,
    const std::string & file_name
)
```


**Parameters**: 

  * **file_type** File type enum (i.e. CFD_TRI_TYPE, COMP_GEOM_TXT_TYPE) 
  * **file_name** File name 


**See**: [COMPUTATION_FILE_TYPE](Modules/group___enumerations.md#enum-computation-file-type), [SetFeaMeshFileName](Modules/group___f_e_a_mesh.md#function-setfeameshfilename)

Get the file name of a specified file type. Note, this function cannot be used to set FEA Mesh file names. 

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

  


### function ComputeCFDMesh

```
void ComputeCFDMesh(
    int set,
    int degenset,
    int file_export_types
)
```


**Parameters**: 

  * **set** int Set index (i.e. SET_ALL) 
  * **degenset** int DegenSet index (i.e. SET_NONE) 
  * **file_export_types** int CFD Mesh file type to export (supports XOR i.e CFD_SRF_TYPE & CFD_STL_TYPE) 


**See**: [COMPUTATION_FILE_TYPE](Modules/group___enumerations.md#enum-computation-file-type)

Create a CFD Mesh for the components in the set. This analysis cannot be run through the Analysis Manager. 

 //==== CFDMesh Method Facet Export =====//
 SetComputationFileName( CFD_FACET_TYPE, "TestCFDMeshFacet_API.facet" );

Print( "\tComputing CFDMesh..." );

 ComputeCFDMesh( SET_ALL, SET_NONE, CFD_FACET_TYPE );
```

 \endforcpponly \beginPythonOnly ```py

 #==== CFDMesh Method Facet Export =====//
 SetComputationFileName( CFD_FACET_TYPE, "TestCFDMeshFacet_API.facet" )

print( "\tComputing CFDMesh..." )

 ComputeCFDMesh( SET_ALL, SET_NONE, CFD_FACET_TYPE )
```

  


### function SetCFDMeshVal

```
void SetCFDMeshVal(
    int type,
    double val
)
```


**Parameters**: 

  * **type** int CFD Mesh control type enum (i.e. CFD_GROWTH_RATIO) 
  * **val** double Value to set 


**See**: [CFD_CONTROL_TYPE](Modules/group___enumerations.md#enum-cfd-control-type)

Set the value of a specific CFD Mesh option 

SetCFDMeshVal( CFD_MIN_EDGE_LEN, 1.0 );
```

 \endforcpponly \beginPythonOnly ```py

SetCFDMeshVal( CFD_MIN_EDGE_LEN, 1.0 )
```

  


### function SetCFDWakeFlag

```
void SetCFDWakeFlag(
    const std::string & geom_id,
    bool flag
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **flag** True to activate, false to deactivate 


**See**: [SetParmVal](Modules/group___parm.md#function-setparmval), [SetParmValUpdate](Modules/group___parm.md#function-setparmvalupdate)

Activate or deactivate the CFD Mesh wake for a particular Geom. Note, the wake flag is only applicable for wing-type surfaces. Also, this function is simply an alternative to setting the value of the Parm with the available Parm setting API functions. 

//==== Add Wing Geom ====//
string wid = AddGeom( "WING", "" );

SetCFDWakeFlag( wid, true );
// This is equivalent to SetParmValUpdate( wid, "Wake", "Shape", 1.0 );
// To change the scale: SetParmValUpdate( wid, "WakeScale", "WakeSettings", 10.0 );
// To change the angle: SetParmValUpdate( wid, "WakeAngle", "WakeSettings", -5.0 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geom ====//
wid = AddGeom( "WING", "" )

SetCFDWakeFlag( wid, True )
# This is equivalent to SetParmValUpdate( wid, "Wake", "Shape", 1.0 )
# To change the scale: SetParmValUpdate( wid, "WakeScale", "WakeSettings", 10.0 )
# To change the angle: SetParmValUpdate( wid, "WakeAngle", "WakeSettings", -5.0 )
```

  


### function DeleteAllCFDSources

```
void DeleteAllCFDSources()
```


Delete all CFD Mesh sources for all Geoms 

//==== Add Pod Geom ====//
string pid = AddGeom( "POD", "" );

AddCFDSource( POINT_SOURCE, pid, 0, 0.25, 2.0, 0.5, 0.5 );      // Add A Point Source

DeleteAllCFDSources();
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geom ====//
pid = AddGeom( "POD", "" )

AddCFDSource( POINT_SOURCE, pid, 0, 0.25, 2.0, 0.5, 0.5 )      # Add A Point Source

DeleteAllCFDSources()
```

  


### function AddDefaultSources

```
void AddDefaultSources()
```


Add default CFD Mesh sources for all Geoms 

//==== Add Pod Geom ====//
string pid = AddGeom( "POD", "" );

AddDefaultSources(); // 3 Sources: Def_Fwd_PS, Def_Aft_PS, Def_Fwd_Aft_LS
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geom ====//
pid = AddGeom( "POD", "" )

AddDefaultSources() # 3 Sources: Def_Fwd_PS, Def_Aft_PS, Def_Fwd_Aft_LS
```

  


### function AddCFDSource

```
void AddCFDSource(
    int type,
    const std::string & geom_id,
    int surf_index,
    double l1,
    double r1,
    double u1,
    double w1,
    double l2 =0,
    double r2 =0,
    double u2 =0,
    double w2 =0
)
```


**Parameters**: 

  * **type** CFD Mesh source type( i.e.BOX_SOURCE ) 
  * **geom_id** string Geom ID 
  * **surf_index** Main surface index 
  * **l1** Source first edge length 
  * **r1** Source first radius 
  * **u1** Source first U location 
  * **w1** Source first W location 
  * **l2** Source second edge length 
  * **r2** Source second radius 
  * **u2** Source second U location 
  * **w2** Source second W location 


**See**: [CFD_MESH_SOURCE_TYPE](Modules/group___enumerations.md#enum-cfd-mesh-source-type)

Add a CFD Mesh default source for the indicated Geom. Note, certain input params may not be used depending on the source type 

//==== Add Pod Geom ====//
string pid = AddGeom( "POD", "" );

AddCFDSource( POINT_SOURCE, pid, 0, 0.25, 2.0, 0.5, 0.5 );      // Add A Point Source
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geom ====//
pid = AddGeom( "POD", "" )

AddCFDSource( POINT_SOURCE, pid, 0, 0.25, 2.0, 0.5, 0.5 )      # Add A Point Source
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800