---
title: FEA Mesh Functions
summary: The following group of API functions supports all functionality of the FEA Mesh Tool. Structures, FEA Parts, materials, and properties can be defined and manipulated. Mesh and output file settings can be adjusted, and an FEA mesh can be generated. Click here to return to the main page. 

---

# FEA Mesh Functions

The following group of API functions supports all functionality of the FEA Mesh Tool. Structures, FEA Parts, materials, and properties can be defined and manipulated. Mesh and output file settings can be adjusted, and an FEA mesh can be generated. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| int | **[AddFeaStruct](Modules/group___f_e_a_mesh.md#function-addfeastruct)**(const std::string & geom_id, bool init_skin =true, int surfindex =0) |
| void | **[SetFeaMeshStructIndex](Modules/group___f_e_a_mesh.md#function-setfeameshstructindex)**(int struct_index) |
| void | **[DeleteFeaStruct](Modules/group___f_e_a_mesh.md#function-deletefeastruct)**(const std::string & geom_id, int fea_struct_ind) |
| std::string | **[GetFeaStructID](Modules/group___f_e_a_mesh.md#function-getfeastructid)**(const std::string & geom_id, int fea_struct_ind) |
| int | **[GetFeaStructIndex](Modules/group___f_e_a_mesh.md#function-getfeastructindex)**(const std::string & struct_id) |
| std::string | **[GetFeaStructParentGeomID](Modules/group___f_e_a_mesh.md#function-getfeastructparentgeomid)**(const std::string & struct_id) |
| std::string | **[GetFeaStructName](Modules/group___f_e_a_mesh.md#function-getfeastructname)**(const std::string & geom_id, int fea_struct_ind) |
| void | **[SetFeaStructName](Modules/group___f_e_a_mesh.md#function-setfeastructname)**(const std::string & geom_id, int fea_struct_ind, const std::string & name) |
| std::vector< std::string > | **[GetFeaStructIDVec](Modules/group___f_e_a_mesh.md#function-getfeastructidvec)**() |
| void | **[SetFeaPartName](Modules/group___f_e_a_mesh.md#function-setfeapartname)**(const std::string & part_id, const std::string & name) |
| std::string | **[AddFeaPart](Modules/group___f_e_a_mesh.md#function-addfeapart)**(const std::string & geom_id, int fea_struct_ind, int type) |
| void | **[DeleteFeaPart](Modules/group___f_e_a_mesh.md#function-deletefeapart)**(const std::string & geom_id, int fea_struct_ind, const std::string & part_id) |
| std::string | **[GetFeaPartID](Modules/group___f_e_a_mesh.md#function-getfeapartid)**(const std::string & fea_struct_id, int fea_part_index) |
| std::string | **[GetFeaPartName](Modules/group___f_e_a_mesh.md#function-getfeapartname)**(const std::string & part_id) |
| int | **[GetFeaPartType](Modules/group___f_e_a_mesh.md#function-getfeaparttype)**(const std::string & part_id) |
| std::vector< std::string > | **[GetFeaPartIDVec](Modules/group___f_e_a_mesh.md#function-getfeapartidvec)**(const std::string & fea_struct_id) |
| std::vector< std::string > | **[GetFeaSubSurfIDVec](Modules/group___f_e_a_mesh.md#function-getfeasubsurfidvec)**(const std::string & fea_struct_id) |
| void | **[SetFeaPartPerpendicularSparID](Modules/group___f_e_a_mesh.md#function-setfeapartperpendicularsparid)**(const std::string & part_id, const std::string & perpendicular_spar_id) |
| std::string | **[GetFeaPartPerpendicularSparID](Modules/group___f_e_a_mesh.md#function-getfeapartperpendicularsparid)**(const std::string & part_id) |
| void | **[SetFeaSubSurfName](Modules/group___f_e_a_mesh.md#function-setfeasubsurfname)**(const std::string & subsurf_id, const std::string & name) |
| std::string | **[GetFeaSubSurfName](Modules/group___f_e_a_mesh.md#function-getfeasubsurfname)**(const std::string & subsurf_id) |
| std::string | **[AddFeaSubSurf](Modules/group___f_e_a_mesh.md#function-addfeasubsurf)**(const std::string & geom_id, int fea_struct_ind, int type) |
| void | **[DeleteFeaSubSurf](Modules/group___f_e_a_mesh.md#function-deletefeasubsurf)**(const std::string & geom_id, int fea_struct_ind, const std::string & ss_id) |
| int | **[GetFeaSubSurfIndex](Modules/group___f_e_a_mesh.md#function-getfeasubsurfindex)**(const string & ss_id) |
| int | **[NumFeaStructures](Modules/group___f_e_a_mesh.md#function-numfeastructures)**() |
| int | **[NumFeaParts](Modules/group___f_e_a_mesh.md#function-numfeaparts)**(const std::string & fea_struct_id) |
| int | **[NumFeaSubSurfs](Modules/group___f_e_a_mesh.md#function-numfeasubsurfs)**(const std::string & fea_struct_id) |
| std::string | **[AddFeaBC](Modules/group___f_e_a_mesh.md#function-addfeabc)**(const string & fea_struct_id, int type =-1) |
| void | **[DelFeaBC](Modules/group___f_e_a_mesh.md#function-delfeabc)**(const string & fea_struct_id, const std::string & bc_id) |
| std::vector< std::string > | **[GetFeaBCIDVec](Modules/group___f_e_a_mesh.md#function-getfeabcidvec)**(const string & fea_struct_id) |
| int | **[NumFeaBCs](Modules/group___f_e_a_mesh.md#function-numfeabcs)**(const string & fea_struct_id) |
| std::string | **[AddFeaMaterial](Modules/group___f_e_a_mesh.md#function-addfeamaterial)**() |
| std::string | **[AddFeaProperty](Modules/group___f_e_a_mesh.md#function-addfeaproperty)**(int property_type =0) |
| void | **[SetFeaMeshVal](Modules/group___f_e_a_mesh.md#function-setfeameshval)**(const std::string & geom_id, int fea_struct_ind, int type, double val) |
| void | **[SetFeaMeshFileName](Modules/group___f_e_a_mesh.md#function-setfeameshfilename)**(const std::string & geom_id, int fea_struct_ind, int file_type, const string & file_name) |
| void | **[ComputeFeaMesh](Modules/group___f_e_a_mesh.md#function-computefeamesh)**(const std::string & geom_id, int fea_struct_ind, int file_type) |
| void | **[ComputeFeaMesh](Modules/group___f_e_a_mesh.md#function-computefeamesh)**(const std::string & struct_id, int file_type) |


## Functions Documentation

### function AddFeaStruct

```
int AddFeaStruct(
    const std::string & geom_id,
    bool init_skin =true,
    int surfindex =0
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **init_skin** Flag to initialize the FEA Structure by creating an FEA Skin from the parent Geom's OML at surfindex 
  * **surfindex** Main surface index for the FEA Structure 


**Return**: FEA Structure index 

**Warning**: init_skin should ALWAYS be set to true. 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )
```

  

Add an FEA Structure to a specified Geom 


### function SetFeaMeshStructIndex

```
void SetFeaMeshStructIndex(
    int struct_index
)
```


Sets FeaMeshMgr m_FeaMeshStructIndex member using passed in index of a FeaStructure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

SetFeaMeshStructIndex( struct_ind );

if ( FindGeoms().size() != 0 ) { Print( "ERROR: VSPRenew" ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

SetFeaMeshStructIndex( struct_ind )

if  len(FindGeoms()) != 0 : print( "ERROR: VSPRenew" )
```

  


### function DeleteFeaStruct

```
void DeleteFeaStruct(
    const std::string & geom_id,
    int fea_struct_ind
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 


Delete an FEA Structure and all FEA Parts and FEA SubSurfaces associated with it 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind_1 = AddFeaStruct( pod_id );

int struct_ind_2 = AddFeaStruct( pod_id );

DeleteFeaStruct( pod_id, struct_ind_1 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind_1 = AddFeaStruct( pod_id )

struct_ind_2 = AddFeaStruct( pod_id )

DeleteFeaStruct( pod_id, struct_ind_1 )
```

  


### function GetFeaStructID

```
std::string GetFeaStructID(
    const std::string & geom_id,
    int fea_struct_ind
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 


**Return**: FEA Structure ID 

Get the ID of an FEA Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )
```

  


### function GetFeaStructIndex

```
int GetFeaStructIndex(
    const std::string & struct_id
)
```


**Parameters**: 

  * **struct_id** FEA Structure ID 


**Return**: FEA Structure index 

Get the index of an FEA Structure in its Parent Geom's vector of Structures 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind_1 = AddFeaStruct( pod_id );

int struct_ind_2 = AddFeaStruct( pod_id );

string struct_id_2 = GetFeaStructID( pod_id, struct_ind_2 );

DeleteFeaStruct( pod_id, struct_ind_1 );

int struct_ind_2_new = GetFeaStructIndex( struct_id_2 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind_1 = AddFeaStruct( pod_id )

struct_ind_2 = AddFeaStruct( pod_id )

struct_id_2 = GetFeaStructID( pod_id, struct_ind_2 )

DeleteFeaStruct( pod_id, struct_ind_1 )

struct_ind_2_new = GetFeaStructIndex( struct_id_2 )
```

  


### function GetFeaStructParentGeomID

```
std::string GetFeaStructParentGeomID(
    const std::string & struct_id
)
```


**Parameters**: 

  * **struct_id** FEA Structure ID 


**Return**: Parent Geom ID 

Get the Parent Geom ID for an FEA Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Get Parent Geom ID and Index ====//
string parent_id = GetFeaStructParentGeomID( struct_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#==== Get Parent Geom ID and Index ====//
parent_id = GetFeaStructParentGeomID( struct_id )
```

  


### function GetFeaStructName

```
std::string GetFeaStructName(
    const std::string & geom_id,
    int fea_struct_ind
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 


**See**: [FindContainer](Modules/group___parm_container.md#function-findcontainer), [SetFeaStructName](Modules/group___f_e_a_mesh.md#function-setfeastructname)

**Return**: Name for the FEA Structure 

Get the name of an FEA Structure. The FEA Structure name functions as the the Parm Container name 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Get Structure Name ====//
string parm_container_name = GetFeaStructName( pod_id, struct_ind );

string display_name = string("Current Structure Parm Container Name: ") + parm_container_name + string("\n");

Print( display_name );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Get Structure Name ====//
parm_container_name = GetFeaStructName( pod_id, struct_ind )

display_name = "Current Structure Parm Container Name: " + parm_container_name + "\n"

print( display_name )
```

  


### function SetFeaStructName

```
void SetFeaStructName(
    const std::string & geom_id,
    int fea_struct_ind,
    const std::string & name
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 
  * **name** New name for the FEA Structure 


**See**: [GetFeaStructName](Modules/group___f_e_a_mesh.md#function-getfeastructname)

Set the name of an FEA Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Change the Structure Name ====//
SetFeaStructName( pod_id, struct_ind, "Example_Struct" );

string parm_container_id = FindContainer( "Example_Struct", struct_ind );

string display_id = string("New Structure Parm Container ID: ") + parm_container_id + string("\n");

Print( display_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Change the Structure Name ====//
SetFeaStructName( pod_id, struct_ind, "Example_Struct" )

parm_container_id = FindContainer( "Example_Struct", struct_ind )

display_id = "New Structure Parm Container ID: " + parm_container_id + "\n"

print( display_id )
```

  


### function GetFeaStructIDVec

```
std::vector< std::string > GetFeaStructIDVec()
```


**See**: [NumFeaStructures](Modules/group___f_e_a_mesh.md#function-numfeastructures)

**Return**: Array of FEA Structure IDs 

Get the IDs of all FEA Structures in the vehicle 

//==== Add Geometries ====//
string pod_id = AddGeom( "POD" );
string wing_id = AddGeom( "WING" );

//==== Add FeaStructures ====//
int pod_struct_ind = AddFeaStruct( pod_id );
int wing_struct_ind = AddFeaStruct( wing_id );

array < string > struct_id_vec = GetFeaStructIDVec();
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Geometries ====//
pod_id = AddGeom( "POD" )
wing_id = AddGeom( "WING" )

#==== Add FeaStructures ====//
pod_struct_ind = AddFeaStruct( pod_id )
wing_struct_ind = AddFeaStruct( wing_id )

struct_id_vec = GetFeaStructIDVec()
```

  


### function SetFeaPartName

```
void SetFeaPartName(
    const std::string & part_id,
    const std::string & name
)
```


**Parameters**: 

  * **part_id** FEA Part ID 
  * **name** New name for the FEA Part 


**See**: [GetFeaPartName](Modules/group___f_e_a_mesh.md#function-getfeapartname)

Set the name of an FEA Part 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add Bulkead ====//
string bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );

SetFeaPartName( bulkhead_id, "Bulkhead" );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add Bulkead ====//
bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )

SetFeaPartName( bulkhead_id, "Bulkhead" )
```

  


### function AddFeaPart

```
std::string AddFeaPart(
    const std::string & geom_id,
    int fea_struct_ind,
    int type
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 
  * **type** FEA Part type enum (i.e. FEA_RIB) 


**See**: [FEA_PART_TYPE](Modules/group___enumerations.md#enum-fea-part-type)

**Return**: FEA Part ID 

Add an FEA Part to a Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add Bulkead ====//
string bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );

SetParmVal( FindParm( bulkhead_id, "IncludedElements", "FeaPart" ), FEA_SHELL_AND_BEAM );

SetParmVal( FindParm( bulkhead_id, "RelCenterLocation", "FeaPart" ), 0.15 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add Bulkead ====//
bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )

SetParmVal( FindParm( bulkhead_id, "IncludedElements", "FeaPart" ), FEA_SHELL_AND_BEAM )

SetParmVal( FindParm( bulkhead_id, "RelCenterLocation", "FeaPart" ), 0.15 )
```

  


### function DeleteFeaPart

```
void DeleteFeaPart(
    const std::string & geom_id,
    int fea_struct_ind,
    const std::string & part_id
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 
  * **part_id** FEA Part ID 


Delete an FEA Part from a Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add Bulkead ====//
string bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );

//==== Add Fixed Point ====//
string fixed_id = AddFeaPart( pod_id, struct_ind, FEA_FIX_POINT );

//==== Delete Bulkead ====//
DeleteFeaPart( pod_id, struct_ind, bulkhead_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add Bulkead ====//
bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )

#==== Add Fixed Point ====//
fixed_id = AddFeaPart( pod_id, struct_ind, FEA_FIX_POINT )

#==== Delete Bulkead ====//
DeleteFeaPart( pod_id, struct_ind, bulkhead_id )
```

  


### function GetFeaPartID

```
std::string GetFeaPartID(
    const std::string & fea_struct_id,
    int fea_part_index
)
```


**Parameters**: 

  * **fea_struct_id** FEA Structure ID 
  * **fea_part_index** FEA Part index 


**Return**: FEA Part ID 

Get the Parm ID of an FEA Part, identified from a FEA Structure Parm ID and FEA Part index. 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add Bulkead ====//
string bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );

Update();

if ( bulkhead_id != GetFeaPartID( struct_id, 1 ) ) // These should be equivalent (index 0 is skin)
{
    Print( "Error: GetFeaPartID" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#==== Add Bulkead ====//
bulkhead_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )

Update()

if  bulkhead_id != GetFeaPartID( struct_id, 1 ) : # These should be equivalent (index 0 is skin)

    print( "Error: GetFeaPartID" )
```

  


### function GetFeaPartName

```
std::string GetFeaPartName(
    const std::string & part_id
)
```


**Parameters**: 

  * **part_id** FEA Part ID 


**See**: [SetFeaPartName](Modules/group___f_e_a_mesh.md#function-setfeapartname)

**Return**: FEA Part name 

Get the name of an FEA Part 

//==== Add Fuselage Geometry ====//
string fuse_id = AddGeom( "FUSELAGE" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( fuse_id );

//==== Add Bulkead ====//
string bulkhead_id = AddFeaPart( fuse_id, struct_ind, FEA_SLICE );

string name = "example_name";
SetFeaPartName( bulkhead_id, name );

if ( name != GetFeaPartName( bulkhead_id ) ) // These should be equivalent
{
    Print( "Error: GetFeaPartName" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Fuselage Geometry ====//
fuse_id = AddGeom( "FUSELAGE" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( fuse_id )

#==== Add Bulkead ====//
bulkhead_id = AddFeaPart( fuse_id, struct_ind, FEA_SLICE )

name = "example_name"
SetFeaPartName( bulkhead_id, name )

if  name != GetFeaPartName( bulkhead_id ) : # These should be equivalent

    print( "Error: GetFeaPartName" )
```

  


### function GetFeaPartType

```
int GetFeaPartType(
    const std::string & part_id
)
```


**Parameters**: 

  * **part_id** FEA Part ID 


**See**: [FEA_PART_TYPE](Modules/group___enumerations.md#enum-fea-part-type)

**Return**: FEA Part type enum 

Get the type of an FEA Part 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add Slice ====//
string slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );

if ( FEA_SLICE != GetFeaPartType( slice_id ) ) // These should be equivalent
{
    Print( "Error: GetFeaPartType" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add Slice ====//
slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )

if  FEA_SLICE != GetFeaPartType( slice_id ) : # These should be equivalent

    print( "Error: GetFeaPartType" )
```

  


### function GetFeaPartIDVec

```
std::vector< std::string > GetFeaPartIDVec(
    const std::string & fea_struct_id
)
```


**Parameters**: 

  * **fea_struct_id** FEA Structure ID 


**See**: [NumFeaParts](Modules/group___f_e_a_mesh.md#function-numfeaparts)

**Return**: Array of FEA Part IDs 

Get the IDs of all FEA Parts in the given FEA Structure 

//==== Add Geometries ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add FEA Parts ====//
string slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );
string dome_id = AddFeaPart( pod_id, struct_ind, FEA_DOME );

array < string > part_id_vec = GetFeaPartIDVec( struct_id ); // Should include slice_id & dome_id
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Geometries ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#==== Add FEA Parts ====//
slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )
dome_id = AddFeaPart( pod_id, struct_ind, FEA_DOME )

part_id_vec = GetFeaPartIDVec( struct_id ) # Should include slice_id & dome_id
```

  


### function GetFeaSubSurfIDVec

```
std::vector< std::string > GetFeaSubSurfIDVec(
    const std::string & fea_struct_id
)
```


**Parameters**: 

  * **fea_struct_id** FEA Structure ID 


**See**: [NumFeaSubSurfs](Modules/group___f_e_a_mesh.md#function-numfeasubsurfs)

**Return**: Array of FEA Part IDs 

Get the IDs of all FEA SubSurfaces in the given FEA Structure 

//==== Add Geometries ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add SubSurfaces ====//
string line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY );
string rectangle_id = AddFeaSubSurf( pod_id, struct_ind, SS_RECTANGLE );

array < string > part_id_vec = GetFeaSubSurfIDVec( struct_id ); // Should include line_array_id & rectangle_id
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Geometries ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#==== Add SubSurfaces ====//
line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY )
rectangle_id = AddFeaSubSurf( pod_id, struct_ind, SS_RECTANGLE )

part_id_vec = GetFeaSubSurfIDVec( struct_id ) # Should include line_array_id & rectangle_id
```

  


### function SetFeaPartPerpendicularSparID

```
void SetFeaPartPerpendicularSparID(
    const std::string & part_id,
    const std::string & perpendicular_spar_id
)
```


**Parameters**: 

  * **part_id** FEA Part ID (Rib or Rib Array Type) 
  * **perpendicular_spar_id** FEA Spar ID 


**See**: [FEA_RIB_NORMAL](Modules/group___enumerations.md#enum-fea-rib-normal), [GetFeaPartPerpendicularSparID](Modules/group___f_e_a_mesh.md#function-getfeapartperpendicularsparid)

Set the ID of the perpendicular spar for an FEA Rib or Rib Array. Note, the FEA Rib or Rib Array should have "SPAR_NORMAL" set for the "PerpendicularEdgeType" Parm. If it is not, the ID will still be set, but the orientation of the Rib or Rib Array will not change. 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

//==== Add FeaStructure to Wing ====//
int struct_ind = AddFeaStruct( wing_id );

//==== Add Rib ====//
string rib_id = AddFeaPart( wing_id, struct_ind, FEA_RIB );

//==== Add Spars ====//
string spar_id_1 = AddFeaPart( wing_id, struct_ind, FEA_SPAR );
string spar_id_2 = AddFeaPart( wing_id, struct_ind, FEA_SPAR );

SetParmVal( FindParm( spar_id_1, "RelCenterLocation", "FeaPart" ), 0.25 );
SetParmVal( FindParm( spar_id_2, "RelCenterLocation", "FeaPart" ), 0.75 );

//==== Set Perpendicular Edge type to SPAR ====//
SetParmVal( FindParm( rib_id, "PerpendicularEdgeType", "FeaRib" ), SPAR_NORMAL );

SetFeaPartPerpendicularSparID( rib_id, spar_id_2 );

if ( spar_id_2 != GetFeaPartPerpendicularSparID( rib_id ) )
{
    Print( "Error: SetFeaPartPerpendicularSparID" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

#==== Add FeaStructure to Wing ====//
struct_ind = AddFeaStruct( wing_id )

#==== Add Rib ====//
rib_id = AddFeaPart( wing_id, struct_ind, FEA_RIB )

#==== Add Spars ====//
spar_id_1 = AddFeaPart( wing_id, struct_ind, FEA_SPAR )
spar_id_2 = AddFeaPart( wing_id, struct_ind, FEA_SPAR )

SetParmVal( FindParm( spar_id_1, "RelCenterLocation", "FeaPart" ), 0.25 )
SetParmVal( FindParm( spar_id_2, "RelCenterLocation", "FeaPart" ), 0.75 )

#==== Set Perpendicular Edge type to SPAR ====//
SetParmVal( FindParm( rib_id, "PerpendicularEdgeType", "FeaRib" ), SPAR_NORMAL )

SetFeaPartPerpendicularSparID( rib_id, spar_id_2 )

if  spar_id_2 != GetFeaPartPerpendicularSparID( rib_id ) :
    print( "Error: SetFeaPartPerpendicularSparID" )
```

  


### function GetFeaPartPerpendicularSparID

```
std::string GetFeaPartPerpendicularSparID(
    const std::string & part_id
)
```


**Parameters**: 

  * **part_id** FEA Part ID (Rib or Rib Array Type) 


**See**: [FEA_RIB_NORMAL](Modules/group___enumerations.md#enum-fea-rib-normal), [SetFeaPartPerpendicularSparID](Modules/group___f_e_a_mesh.md#function-setfeapartperpendicularsparid)

**Return**: Perpendicular FEA Spar ID 

Get the ID of the perpendicular spar for an FEA Rib or Rib Array. Note, the FEA Rib or Rib Array doesn't have to have "SPAR_NORMAL" set for the "PerpendicularEdgeType" Parm for this function to still return a value. 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

//==== Add FeaStructure to Wing ====//
int struct_ind = AddFeaStruct( wing_id );

//==== Add Rib ====//
string rib_id = AddFeaPart( wing_id, struct_ind, FEA_RIB );

//==== Add Spars ====//
string spar_id_1 = AddFeaPart( wing_id, struct_ind, FEA_SPAR );
string spar_id_2 = AddFeaPart( wing_id, struct_ind, FEA_SPAR );

SetParmVal( FindParm( spar_id_1, "RelCenterLocation", "FeaPart" ), 0.25 );
SetParmVal( FindParm( spar_id_2, "RelCenterLocation", "FeaPart" ), 0.75 );

//==== Set Perpendicular Edge type to SPAR ====//
SetParmVal( FindParm( rib_id, "PerpendicularEdgeType", "FeaRib" ), SPAR_NORMAL );

SetFeaPartPerpendicularSparID( rib_id, spar_id_2 );

if ( spar_id_2 != GetFeaPartPerpendicularSparID( rib_id ) )
{
    Print( "Error: GetFeaPartPerpendicularSparID" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

#==== Add FeaStructure to Wing ====//
struct_ind = AddFeaStruct( wing_id )

#==== Add Rib ====//
rib_id = AddFeaPart( wing_id, struct_ind, FEA_RIB )

#==== Add Spars ====//
spar_id_1 = AddFeaPart( wing_id, struct_ind, FEA_SPAR )
spar_id_2 = AddFeaPart( wing_id, struct_ind, FEA_SPAR )

SetParmVal( FindParm( spar_id_1, "RelCenterLocation", "FeaPart" ), 0.25 )
SetParmVal( FindParm( spar_id_2, "RelCenterLocation", "FeaPart" ), 0.75 )

#==== Set Perpendicular Edge type to SPAR ====//
SetParmVal( FindParm( rib_id, "PerpendicularEdgeType", "FeaRib" ), SPAR_NORMAL )

SetFeaPartPerpendicularSparID( rib_id, spar_id_2 )

if  spar_id_2 != GetFeaPartPerpendicularSparID( rib_id ) :
    print( "Error: GetFeaPartPerpendicularSparID" )
```

  


### function SetFeaSubSurfName

```
void SetFeaSubSurfName(
    const std::string & subsurf_id,
    const std::string & name
)
```


**Parameters**: 

  * **subsurf_id** FEA SubSurface ID 
  * **name** New name for the FEA SubSurface 


Set the name of an FEA SubSurface 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add LineArray ====//
string line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY );

SetFeaSubSurfName( line_array_id, "Stiffener_array" );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add LineArray ====//
line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY )

SetFeaSubSurfName( line_array_id, "Stiffener_array" )
```

  


### function GetFeaSubSurfName

```
std::string GetFeaSubSurfName(
    const std::string & subsurf_id
)
```


**Parameters**: 

  * **subsurf_id** FEA SubSurface ID 


**Return**: FEA SubSurf name 

Set the name of an FEA SubSurface 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add LineArray ====//
string line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY );

string name = "example_name";
SetFeaSubSurfName( line_array_id, name );

if ( name != GetFeaSubSurfName( line_array_id ) ) // These should be equivalent
{
    Print( "Error: GetFeaSubSurfName" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add LineArray ====//
line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY )

name = "example_name"
SetFeaSubSurfName( line_array_id, name )

if  name != GetFeaSubSurfName( line_array_id ) : # These should be equivalent
    print( "Error: GetFeaSubSurfName" )
```

  


### function AddFeaSubSurf

```
std::string AddFeaSubSurf(
    const std::string & geom_id,
    int fea_struct_ind,
    int type
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 
  * **type** FEA SubSurface type enum (i.e. SS_ELLIPSE) 


**See**: [SUBSURF_TYPE](Modules/group___enumerations.md#enum-subsurf-type)

**Return**: FEA SubSurface ID 

Add an FEA SubSurface to a Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add LineArray ====//
string line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY );

SetParmVal( FindParm( line_array_id, "ConstLineType", "SS_LineArray" ), 1 ); // Constant W

SetParmVal( FindParm( line_array_id, "Spacing", "SS_LineArray" ), 0.25 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add LineArray ====//
line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY )

SetParmVal( FindParm( line_array_id, "ConstLineType", "SS_LineArray" ), 1 ) # Constant W

SetParmVal( FindParm( line_array_id, "Spacing", "SS_LineArray" ), 0.25 )
```

  


### function DeleteFeaSubSurf

```
void DeleteFeaSubSurf(
    const std::string & geom_id,
    int fea_struct_ind,
    const std::string & ss_id
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 
  * **ss_id** FEA SubSurface ID 


Delete an FEA SubSurface from a Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add LineArray ====//
string line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY );

//==== Add Rectangle ====//
string rect_id = AddFeaSubSurf( pod_id, struct_ind, SS_RECTANGLE );

//==== Delete LineArray ====//
DeleteFeaSubSurf( pod_id, struct_ind, line_array_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add LineArray ====//
line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY )

#==== Add Rectangle ====//
rect_id = AddFeaSubSurf( pod_id, struct_ind, SS_RECTANGLE )

#==== Delete LineArray ====//
DeleteFeaSubSurf( pod_id, struct_ind, line_array_id )
```

  


### function GetFeaSubSurfIndex

```
int GetFeaSubSurfIndex(
    const string & ss_id
)
```


**Parameters**: 

  * **ss_id** FEA SubSurface ID 


**Return**: FEA SubSurface Index 

Get the index of an FEA SubSurface give the SubSurface ID 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Add Slice ====//
string slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );

//==== Add LineArray ====//
string line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY );

//==== Add Rectangle ====//
string rect_id = AddFeaSubSurf( pod_id, struct_ind, SS_RECTANGLE );

if ( 1 != GetFeaSubSurfIndex( rect_id ) ) // These should be equivalent
{
    Print( "Error: GetFeaSubSurfIndex" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Add Slice ====//
slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )

#==== Add LineArray ====//
line_array_id = AddFeaSubSurf( pod_id, struct_ind, SS_LINE_ARRAY )

#==== Add Rectangle ====//
rect_id = AddFeaSubSurf( pod_id, struct_ind, SS_RECTANGLE )

if  1 != GetFeaSubSurfIndex( rect_id ) : # These should be equivalent

    print( "Error: GetFeaSubSurfIndex" )
```

  


### function NumFeaStructures

```
int NumFeaStructures()
```


**See**: [GetFeaStructIDVec](Modules/group___f_e_a_mesh.md#function-getfeastructidvec)

**Return**: Total Number of FEA Structures 

Get the total number of FEA Subsurfaces in the vehicle 

//==== Add Pod Geometry ====//
string wing_id = AddGeom( "WING" );

//==== Add FeaStructure to Pod ====//
int struct_1 = AddFeaStruct( wing_id );
int struct_2 = AddFeaStruct( wing_id );

if ( NumFeaStructures() != 2 )
{
    Print( "Error: NumFeaStructures" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
wing_id = AddGeom( "WING" )

#==== Add FeaStructure to Pod ====//
struct_1 = AddFeaStruct( wing_id )
struct_2 = AddFeaStruct( wing_id )

if  NumFeaStructures() != 2 :
    print( "Error: NumFeaStructures" )
```

  


### function NumFeaParts

```
int NumFeaParts(
    const std::string & fea_struct_id
)
```


**Parameters**: 

  * **fea_struct_id** FEA Structure ID 


**See**: [GetFeaPartIDVec](Modules/group___f_e_a_mesh.md#function-getfeapartidvec)

**Return**: Number of FEA Parts 

Get the number of FEA Parts for a particular FEA Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add FEA Parts ====//
string slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE );
string dome_id = AddFeaPart( pod_id, struct_ind, FEA_DOME );

if ( NumFeaParts( struct_id ) != 3 ) // Includes FeaSkin
{
    Print( "Error: NumFeaParts" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#==== Add FEA Parts ====//
slice_id = AddFeaPart( pod_id, struct_ind, FEA_SLICE )
dome_id = AddFeaPart( pod_id, struct_ind, FEA_DOME )

if  NumFeaParts( struct_id ) != 3 : # Includes FeaSkin

    print( "Error: NumFeaParts" )
```

  


### function NumFeaSubSurfs

```
int NumFeaSubSurfs(
    const std::string & fea_struct_id
)
```


**Parameters**: 

  * **fea_struct_id** FEA Structure ID 


**See**: [GetFeaSubSurfIDVec](Modules/group___f_e_a_mesh.md#function-getfeasubsurfidvec)

**Return**: Number of FEA SubSurfaces 

Get the number of FEA Subsurfaces for a particular FEA Structure 

//==== Add Pod Geometry ====//
string wing_id = AddGeom( "WING" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( wing_id );

string struct_id = GetFeaStructID( wing_id, struct_ind );

//==== Add SubSurfaces ====//
string line_array_id = AddFeaSubSurf( wing_id, struct_ind, SS_LINE_ARRAY );
string rectangle_id = AddFeaSubSurf( wing_id, struct_ind, SS_RECTANGLE );

if ( NumFeaSubSurfs( struct_id ) != 2 )
{
    Print( "Error: NumFeaSubSurfs" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
wing_id = AddGeom( "WING" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( wing_id )

struct_id = GetFeaStructID( wing_id, struct_ind )

#==== Add SubSurfaces ====//
line_array_id = AddFeaSubSurf( wing_id, struct_ind, SS_LINE_ARRAY )
rectangle_id = AddFeaSubSurf( wing_id, struct_ind, SS_RECTANGLE )

if  NumFeaSubSurfs( struct_id ) != 2 :
    print( "Error: NumFeaSubSurfs" )
```

  


### function AddFeaBC

```
std::string AddFeaBC(
    const string & fea_struct_id,
    int type =-1
)
```


**Parameters**: 

  * **fea_struct_id** string FEA Structure ID 
  * **type** int FEA BC type enum ( i.e. FEA_BC_STRUCTURE ) 


**See**: [FEA_BC_TYPE](Modules/group___enumerations.md#enum-fea-bc-type)

**Return**: FEA BC ID 

Add an FEA BC to a Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add BC ====//
string bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind );

#==== Add BC ====//
bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE )
```

  


### function DelFeaBC

```
void DelFeaBC(
    const string & fea_struct_id,
    const std::string & bc_id
)
```


**Parameters**: 

  * **fea_struct_id** string FEA Structure ID 
  * **bc_id** int FEA BC ID 


**See**: [FEA_BC_TYPE](Modules/group___enumerations.md#enum-fea-bc-type)

Delete an FEA BC from a Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add BC ====//
string bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE );

DelFeaBC( struct_id, bc_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind );

#==== Add BC ====//
bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE )

DelFeaBC( struct_id, bc_id )
```

  


### function GetFeaBCIDVec

```
std::vector< std::string > GetFeaBCIDVec(
    const string & fea_struct_id
)
```


**Parameters**: 

  * **fea_struct_id** string FEA Structure ID 


**Return**: Array of FEA BC IDs 

Return a vector of FEA BC ID's for a structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add BC ====//
string bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE );

array < string > bc_id_vec = GetFeaBCIDVec( struct_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind );

#==== Add BC ====//
bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE )

bc_id_vec = GetFeaBCIDVec( struct_id )
```

  


### function NumFeaBCs

```
int NumFeaBCs(
    const string & fea_struct_id
)
```


**Parameters**: 

  * **fea_struct_id** string FEA Structure ID 


**Return**: Number of FEA BCs 

Return number of FEA BC's in a structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Add BC ====//
string bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE );

int nbc = NumFeaBCs( struct_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind );

#==== Add BC ====//
bc_id = AddFeaBC( struct_id, FEA_BC_STRUCTURE )

nbc = NumFeaBCs( struct_id )
```

  


### function AddFeaMaterial

```
std::string AddFeaMaterial()
```


**Return**: FEA Material ID 

Add an FEA Material the FEA Mesh material library. Materials are available across all Geoms and Structures. 

//==== Create FeaMaterial ====//
string mat_id = AddFeaMaterial();

SetParmVal( FindParm( mat_id, "MassDensity", "FeaMaterial" ), 0.016 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Create FeaMaterial ====//
mat_id = AddFeaMaterial()

SetParmVal( FindParm( mat_id, "MassDensity", "FeaMaterial" ), 0.016 )
```

  


### function AddFeaProperty

```
std::string AddFeaProperty(
    int property_type =0
)
```


**Parameters**: 

  * **property_type** FEA Property type enum (i.e. FEA_SHELL). 


**See**: [FEA_PART_ELEMENT_TYPE](Modules/group___enumerations.md#enum-fea-part-element-type)

**Return**: FEA Property ID 

Add aa FEA Property the FEA Mesh property library. Properties are available across all Geoms and Structures. Currently only beam and shell properties are available. Note FEA_SHELL_AND_BEAM is not a valid property type. 

//==== Create FeaProperty ====//
string prop_id = AddFeaProperty();

SetParmVal( FindParm( prop_id, "Thickness", "FeaProperty" ), 0.01 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Create FeaProperty ====//
prop_id = AddFeaProperty()

SetParmVal( FindParm( prop_id, "Thickness", "FeaProperty" ), 0.01 )
```

  


### function SetFeaMeshVal

```
void SetFeaMeshVal(
    const std::string & geom_id,
    int fea_struct_ind,
    int type,
    double val
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 
  * **type** FEA Mesh option type enum (i.e. CFD_MAX_EDGE_LEN) 
  * **val** Value the option is set to 


**See**: [CFD_CONTROL_TYPE](Modules/group___enumerations.md#enum-cfd-control-type)

Set the value of a particular FEA Mesh option for the specified Structure. Note, FEA Mesh makes use of enums initially created for CFD Mesh but not all CFD Mesh options are available for FEA Mesh. 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Adjust FeaMeshSettings ====//
SetFeaMeshVal( pod_id, struct_ind, CFD_MAX_EDGE_LEN, 0.75 );

SetFeaMeshVal( pod_id, struct_ind, CFD_MIN_EDGE_LEN, 0.2 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Adjust FeaMeshSettings ====//
SetFeaMeshVal( pod_id, struct_ind, CFD_MAX_EDGE_LEN, 0.75 )

SetFeaMeshVal( pod_id, struct_ind, CFD_MIN_EDGE_LEN, 0.2 )
```

  


### function SetFeaMeshFileName

```
void SetFeaMeshFileName(
    const std::string & geom_id,
    int fea_struct_ind,
    int file_type,
    const string & file_name
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** FEA Structure index 
  * **file_type** FEA output file type enum (i.e. [FEA_EXPORT_TYPE](Modules/group___enumerations.md#enum-fea-export-type)) 
  * **file_name** Name for the output file 


Set the name of a particular FEA Mesh output file for a specified Structure 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//=== Set Export File Name ===//
string export_name = "FEAMeshTest_calculix.dat";

//==== Get Parent Geom ID and Index ====//
string parent_id = GetFeaStructParentGeomID( struct_id ); // same as pod_id

SetFeaMeshFileName( parent_id, struct_ind, FEA_CALCULIX_FILE_NAME, export_name );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#=== Set Export File Name ===//
export_name = "FEAMeshTest_calculix.dat"

#==== Get Parent Geom ID and Index ====//
parent_id = GetFeaStructParentGeomID( struct_id ) # same as pod_id

SetFeaMeshFileName( parent_id, struct_ind, FEA_CALCULIX_FILE_NAME, export_name )
```

  


### function ComputeFeaMesh

```
void ComputeFeaMesh(
    const std::string & geom_id,
    int fea_struct_ind,
    int file_type
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **fea_struct_ind** int FEA Structure index 
  * **file_type** int FEA output file type enum (i.e. [FEA_EXPORT_TYPE](Modules/group___enumerations.md#enum-fea-export-type)) 


**See**: [SetFeaMeshFileName](Modules/group___f_e_a_mesh.md#function-setfeameshfilename), [FEA_EXPORT_TYPE](Modules/group___enumerations.md#enum-fea-export-type)

Compute an FEA Mesh for a Structure. Only a single output file can be generated with this function. 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Generate FEA Mesh and Export ====//
Print( string( "--> Generating FeaMesh " ) );

//==== Get Parent Geom ID and Index ====//
string parent_id = GetFeaStructParentGeomID( struct_id ); // same as pod_id

ComputeFeaMesh( parent_id, struct_ind, FEA_CALCULIX_FILE_NAME );
// Could also call ComputeFeaMesh ( struct_id, FEA_CALCULIX_FILE_NAME );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#==== Generate FEA Mesh and Export ====//
print( "--> Generating FeaMesh " )

#==== Get Parent Geom ID and Index ====//
parent_id = GetFeaStructParentGeomID( struct_id ) # same as pod_id

ComputeFeaMesh( parent_id, struct_ind, FEA_CALCULIX_FILE_NAME )
```

  


### function ComputeFeaMesh

```
void ComputeFeaMesh(
    const std::string & struct_id,
    int file_type
)
```


**Parameters**: 

  * **struct_id** string FEA Structure index 
  * **file_type** int FEA output file type enum (i.e. [FEA_EXPORT_TYPE](Modules/group___enumerations.md#enum-fea-export-type)) 


**See**: [SetFeaMeshFileName](Modules/group___f_e_a_mesh.md#function-setfeameshfilename), [FEA_EXPORT_TYPE](Modules/group___enumerations.md#enum-fea-export-type)

Compute an FEA Mesh for a Structure. Only a single output file can be generated with this function. 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

string struct_id = GetFeaStructID( pod_id, struct_ind );

//==== Generate FEA Mesh and Export ====//
Print( string( "--> Generating FeaMesh " ) );

//==== Get Parent Geom ID and Index ====//
string parent_id = GetFeaStructParentGeomID( struct_id ); // same as pod_id

ComputeFeaMesh( parent_id, struct_ind, FEA_CALCULIX_FILE_NAME );
// Could also call ComputeFeaMesh ( struct_id, FEA_CALCULIX_FILE_NAME );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

struct_id = GetFeaStructID( pod_id, struct_ind )

#==== Generate FEA Mesh and Export ====//
print( string( "--> Generating FeaMesh " ) )

#==== Get Parent Geom ID and Index ====//
parent_id = GetFeaStructParentGeomID( struct_id ) # same as pod_id

Could also call ComputeFeaMesh ( struct_id, FEA_CALCULIX_FILE_NAME )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800