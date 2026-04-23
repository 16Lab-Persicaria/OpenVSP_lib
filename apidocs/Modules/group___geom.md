---
title: Geom Functions
summary: This group of functions is available for adding, deleting, and modifying OpenVSP Geoms through the API. Click here to return to the main page. 

---

# Geom Functions

This group of functions is available for adding, deleting, and modifying OpenVSP Geoms through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::vector< std::string > | **[GetGeomTypes](Modules/group___geom.md#function-getgeomtypes)**() |
| std::string | **[AddGeom](Modules/group___geom.md#function-addgeom)**(const std::string & type, const std::string & parent =std::string()) |
| void | **[UpdateGeom](Modules/group___geom.md#function-updategeom)**(const std::string & geom_id) |
| void | **[DeleteGeom](Modules/group___geom.md#function-deletegeom)**(const std::string & geom_id) |
| void | **[DeleteGeomVec](Modules/group___geom.md#function-deletegeomvec)**(const std::vector< std::string > & del_vec) |
| void | **[CutGeomToClipboard](Modules/group___geom.md#function-cutgeomtoclipboard)**(const std::string & geom_id) |
| void | **[CopyGeomToClipboard](Modules/group___geom.md#function-copygeomtoclipboard)**(const std::string & geom_id) |
| std::vector< std::string > | **[PasteGeomClipboard](Modules/group___geom.md#function-pastegeomclipboard)**(const std::string & parent =std::string()) |
| std::vector< std::string > | **[FindGeoms](Modules/group___geom.md#function-findgeoms)**() |
| std::vector< std::string > | **[FindGeomsWithName](Modules/group___geom.md#function-findgeomswithname)**(const std::string & name) |
| std::string | **[FindGeom](Modules/group___geom.md#function-findgeom)**(const std::string & name, int index) |
| void | **[SetGeomName](Modules/group___geom.md#function-setgeomname)**(const std::string & geom_id, const std::string & name) |
| std::string | **[GetGeomName](Modules/group___geom.md#function-getgeomname)**(const std::string & geom_id) |
| std::vector< std::string > | **[GetGeomParmIDs](Modules/group___geom.md#function-getgeomparmids)**(const std::string & geom_id) |
| std::string | **[GetGeomTypeName](Modules/group___geom.md#function-getgeomtypename)**(const std::string & geom_id) |
| void | **[SetGeomParent](Modules/group___geom.md#function-setgeomparent)**(const std::string & geom_id, const std::string & parent_id) |
| std::string | **[GetGeomParent](Modules/group___geom.md#function-getgeomparent)**(const std::string & geom_id) |
| std::vector< std::string > | **[GetGeomChildren](Modules/group___geom.md#function-getgeomchildren)**(const std::string & geom_id) |
| int | **[GetNumMainSurfs](Modules/group___geom.md#function-getnummainsurfs)**(const std::string & geom_id) |
| int | **[GetTotalNumSurfs](Modules/group___geom.md#function-gettotalnumsurfs)**(const std::string & geom_id) |
| int | **[GetGeomVSPSurfType](Modules/group___geom.md#function-getgeomvspsurftype)**(const std::string & geom_id, int main_surf_ind =0) |
| int | **[GetGeomVSPSurfCfdType](Modules/group___geom.md#function-getgeomvspsurfcfdtype)**(const std::string & geom_id, int main_surf_ind =0) |
| vec3d | **[GetGeomBBoxMax](Modules/group___geom.md#function-getgeombboxmax)**(const std::string & geom_id, int main_surf_ind =0, bool ref_frame_is_absolute =true) |
| vec3d | **[GetGeomBBoxMin](Modules/group___geom.md#function-getgeombboxmin)**(const std::string & geom_id, int main_surf_ind =0, bool ref_frame_is_absolute =true) |
| void | **[SplitWingXSec](Modules/group___geom.md#function-splitwingxsec)**(const string & wing_id, int section_index) |
| void | **[SetDriverGroup](Modules/group___geom.md#function-setdrivergroup)**(const std::string & geom_id, int section_index, int driver_0, int driver_1 =-1, int driver_2 =-1) |


## Functions Documentation

### function GetGeomTypes

```
std::vector< std::string > GetGeomTypes()
```


**Return**: Array of Geom type names 

Get an array of all Geom types (i.e FUSELAGE, POD, etc.) 

//==== Add Pod Geometries ====//
string pod1 = AddGeom( "POD", "" );
string pod2 = AddGeom( "POD", "" );

array< string > @type_array = GetGeomTypes();

if ( type_array[0] != "POD" )                { Print( "---> Error: API GetGeomTypes  " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometries ====//
pod1 = AddGeom( "POD", "" )
pod2 = AddGeom( "POD", "" )

type_array = GetGeomTypes()

if ( type_array[0] != "POD" ): print( "---> Error: API GetGeomTypes  " )
```

  


### function AddGeom

```
std::string AddGeom(
    const std::string & type,
    const std::string & parent =std::string()
)
```


**Parameters**: 

  * **type** Geom type (i.e FUSELAGE, POD, etc.) 
  * **parent** Parent Geom ID 


**Return**: Geom ID 

Add a new Geom of given type as a child of the specified parent. If no parent or an invalid parent is given, the Geom is placed at the top level 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )
```

  


### function UpdateGeom

```
void UpdateGeom(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**See**: [Update()](Modules/group___vehicle.md#function-update)

Perform an update for the specified Geom 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

SetParmVal( pod_id, "X_Rel_Location", "XForm", 5.0 );

UpdateGeom( pod_id ); // Faster than updating the whole vehicle
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

SetParmVal( pod_id, "X_Rel_Location", "XForm", 5.0 )

UpdateGeom( pod_id ) # Faster than updating the whole vehicle
```

  


### function DeleteGeom

```
void DeleteGeom(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


Delete a particular Geom 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

DeleteGeom( wing_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

DeleteGeom( wing_id )
```

  


### function DeleteGeomVec

```
void DeleteGeomVec(
    const std::vector< std::string > & del_vec
)
```


**Parameters**: 

  * **del_vec** vector<string> Vector of Geom IDs 


Delete multiple Geoms 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD", "" );

string rid = ExecAnalysis( "CompGeom" );

array<string>@ mesh_id_vec = GetStringResults( rid, "Mesh_GeomID" );

DeleteGeomVec( mesh_id_vec );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD", "" )

rid = ExecAnalysis( "CompGeom" )

mesh_id_vec = GetStringResults( rid, "Mesh_GeomID" )

DeleteGeomVec( mesh_id_vec )
```

  


### function CutGeomToClipboard

```
void CutGeomToClipboard(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**See**: [PasteGeomClipboard](Modules/group___geom.md#function-pastegeomclipboard)

Cut Geom from current location and store on clipboard 

//==== Add Pod Geometries ====//
string pid1 = AddGeom( "POD", "" );
string pid2 = AddGeom( "POD", "" );

CutGeomToClipboard( pid1 );

PasteGeomClipboard( pid2 ); // Paste Pod 1 as child of Pod 2

array< string > @geom_ids = FindGeoms();

if ( geom_ids.size() != 2 )                { Print( "---> Error: API Cut/Paste Geom  " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometries ====//
pid1 = AddGeom( "POD", "" )
pid2 = AddGeom( "POD", "" )

CutGeomToClipboard( pid1 )

PasteGeomClipboard( pid2 ) # Paste Pod 1 as child of Pod 2

geom_ids = FindGeoms()

if  len(geom_ids) != 2 : print( "---> Error: API Cut/Paste Geom  " )
```

  


### function CopyGeomToClipboard

```
void CopyGeomToClipboard(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**See**: [PasteGeomClipboard](Modules/group___geom.md#function-pastegeomclipboard)

Copy Geom from current location and store on clipboard 

//==== Add Pod Geometries ====//
string pid1 = AddGeom( "POD", "" );
string pid2 = AddGeom( "POD", "" );

CopyGeomToClipboard( pid1 );

PasteGeomClipboard( pid2 ); // Paste Pod 1 as child of Pod 2

array< string > @geom_ids = FindGeoms();

if ( geom_ids.size() != 3 )                { Print( "---> Error: API Copy/Paste Geom  " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometries ====//
pid1 = AddGeom( "POD", "" )
pid2 = AddGeom( "POD", "" )

CopyGeomToClipboard( pid1 )

PasteGeomClipboard( pid2 ) # Paste Pod 1 as child of Pod 2

geom_ids = FindGeoms()

if  len(geom_ids) != 3 : print( "---> Error: API Copy/Paste Geom  " )
```

  


### function PasteGeomClipboard

```
std::vector< std::string > PasteGeomClipboard(
    const std::string & parent =std::string()
)
```


**Parameters**: 

  * **parent** string Parent Geom ID 


**Return**: vector<string> Vector of pasted Geom IDs 

Paste Geom from clipboard into the model. The Geom is pasted as a child of the specified parent, but will be placed at top level if no parent or an invalid one is provided. 

//==== Add Pod Geometries ====//
string pid1 = AddGeom( "POD", "" );
string pid2 = AddGeom( "POD", "" );

CutGeomToClipboard( pid1 );

PasteGeomClipboard( pid2 ); // Paste Pod 1 as child of Pod 2

array< string > @geom_ids = FindGeoms();

if ( geom_ids.size() != 2 )                { Print( "---> Error: API Cut/Paste Geom  " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometries ====//
pid1 = AddGeom( "POD", "" )
pid2 = AddGeom( "POD", "" )

CutGeomToClipboard( pid1 )

PasteGeomClipboard( pid2 ) # Paste Pod 1 as child of Pod 2

geom_ids = FindGeoms()

if  len(geom_ids) != 2 : print( "---> Error: API Cut/Paste Geom  " )
```

  


### function FindGeoms

```
std::vector< std::string > FindGeoms()
```


**Return**: Array of all Geom IDs 

Find and return all Geom IDs in the model 

//==== Add Pod Geometries ====//
string pod1 = AddGeom( "POD", "" );
string pod2 = AddGeom( "POD", "" );

//==== There Should Be Two Geoms =====//
array< string > @geom_ids = FindGeoms();

if ( geom_ids.size() != 2 )                        { Print( "---> Error: API FindGeoms " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometries ====//
pod1 = AddGeom( "POD", "" )
pod2 = AddGeom( "POD", "" )

#==== There Should Be Two Geoms =====//
geom_ids = FindGeoms()

if  len(geom_ids) != 2 : print( "---> Error: API FindGeoms " )
```

  


### function FindGeomsWithName

```
std::vector< std::string > FindGeomsWithName(
    const std::string & name
)
```


**Parameters**: 

  * **name** Geom name 


**See**: [FindGeom](Modules/group___geom.md#function-findgeom)

**Return**: Array of Geom IDs 

Find and return all Geom IDs with the specified name 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD", "" );

SetGeomName( pid, "ExamplePodName" );

array< string > @geom_ids = FindGeomsWithName( "ExamplePodName" );

if ( geom_ids.size() != 1 )
{
    Print( "---> Error: API FindGeomsWithName " );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD", "" )

SetGeomName( pid, "ExamplePodName" )

geom_ids = FindGeomsWithName( "ExamplePodName" )

if  len(geom_ids) != 1 :
    print( "---> Error: API FindGeomsWithName " )
```

  


### function FindGeom

```
std::string FindGeom(
    const std::string & name,
    int index
)
```


**Parameters**: 

  * **name** Geom name 
  * **index** 


**See**: [FindGeomsWithName](Modules/group___geom.md#function-findgeomswithname)

**Return**: Geom ID with name at specified index 

Find and return the Geom ID with the specified name at given index. Equivalent to FindGeomsWithName( name )[index]. 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD", "" );

SetGeomName( pid, "ExamplePodName" );

string geom_id = FindGeom( "ExamplePodName", 0 );

array< string > @geom_ids = FindGeomsWithName( "ExamplePodName" );

if ( geom_ids[0] != geom_id )
{
    Print( "---> Error: API FindGeom & FindGeomsWithName" );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD", "" )

SetGeomName( pid, "ExamplePodName" )

geom_id = FindGeom( "ExamplePodName", 0 )

geom_ids = FindGeomsWithName( "ExamplePodName" )

if  geom_ids[0] != geom_id :
    print( "---> Error: API FindGeom & FindGeomsWithName" )
```

  


### function SetGeomName

```
void SetGeomName(
    const std::string & geom_id,
    const std::string & name
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **name** Geom name 


Set the name of the specified Geom 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD", "" );

SetGeomName( pid, "ExamplePodName" );

array< string > @geom_ids = FindGeomsWithName( "ExamplePodName" );

if ( geom_ids.size() != 1 )
{
    Print( "---> Error: API FindGeomsWithName " );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD", "" )

SetGeomName( pid, "ExamplePodName" )

geom_ids = FindGeomsWithName( "ExamplePodName" )

if  len(geom_ids) != 1 :
    print( "---> Error: API FindGeomsWithName " )
```

  


### function GetGeomName

```
std::string GetGeomName(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: Geom name 

Get the name of a specific Geom 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD", "" );

SetGeomName( pid, "ExamplePodName" );

string name_str = "Geom Name: " + GetGeomName( pid );

Print( name_str );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD", "" )

SetGeomName( pid, "ExamplePodName" )

name_str = "Geom Name: " + GetGeomName( pid )

print( name_str )
```

  


### function GetGeomParmIDs

```
std::vector< std::string > GetGeomParmIDs(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: Array of Parm IDs 

Get all Parm IDs associated with this Geom Parm container 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD", "" );

Print( string( "---> Test Get Parm Arrays" ) );

array< string > @parm_array = GetGeomParmIDs( pid );

if ( parm_array.size() < 1 )            { Print( "---> Error: API GetGeomParmIDs " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD", "" )

print( "---> Test Get Parm Arrays" )

parm_array = GetGeomParmIDs( pid )

if  len(parm_array) < 1 : print( "---> Error: API GetGeomParmIDs " )
```

  


### function GetGeomTypeName

```
std::string GetGeomTypeName(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: Geom type name 

Get the type name of specified Geom (i.e. FUSELAGE) 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

Print( "Geom Type Name: ", false );

Print( GetGeomTypeName( wing_id ) );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

print( "Geom Type Name: ", False )

print( GetGeomTypeName( wing_id ) )
```

  


### function SetGeomParent

```
void SetGeomParent(
    const std::string & geom_id,
    const std::string & parent_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **parent_id** string Parent Geom ID 


Get the parent Geom ID for the input child Geom. "NONE" is returned if the Geom has no parent. 

//==== Reparent two PodGeoms ====//
string pod1 = AddGeom( "POD" );
string pod2 = AddGeom( "POD", pod1 );
string pod3 = AddGeom ("POD" );

string veh_id = GetVehicleID();

SetGeomParent( pod2, veh_id );
SetGeomParent( pod3, pod1 );

string pod2_parent = GetGeomParent( pod2 );
string pod3_parent = GetGeomParent( pod3 );

if ( pod2_parent != string("NONE") || pod3_parent != pod1 )
{
    Print( "SetGeomParent error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Reparent two PodGeoms ====#
pod1 = AddGeom( "POD" )
pod2 = AddGeom( "POD", pod1 )
pod3 = AddGeom ("POD" )

veh_id = GetVehicleID()

SetGeomParent( pod2, veh_id )
SetGeomParent( pod3, pod1 )

pod2_parent = GetGeomParent( pod2 )
pod3_parent = GetGeomParent( pod3 )

if ( pod2_parent != "NONE" or pod3_parent != pod1 ):
    print( "SetGeomParent error!" )
```

  


### function GetGeomParent

```
std::string GetGeomParent(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: string Parent Geom ID 

Get the parent Geom ID for the input child Geom. "NONE" is returned if the Geom has no parent. 

//==== Add Parent and Child Geometry ====//
string pod1 = AddGeom( "POD" );

string pod2 = AddGeom( "POD", pod1 );

Print( "Parent ID of Pod #2: ", false );

Print( GetGeomParent( pod2 ) );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Parent and Child Geometry ====//
pod1 = AddGeom( "POD" )

pod2 = AddGeom( "POD", pod1 )

print( "Parent ID of Pod #2: ", False )

print( GetGeomParent( pod2 ) )
```

  


### function GetGeomChildren

```
std::vector< std::string > GetGeomChildren(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: vector<string> Vector of child Geom IDs 

Get the IDs for each child of the input parent Geom. 

//==== Add Parent and Child Geometry ====//
string pod1 = AddGeom( "POD" );

string pod2 = AddGeom( "POD", pod1 );

string pod3 = AddGeom( "POD", pod2 );

Print( "Children of Pod #1: " );

array<string> children = GetGeomChildren( pod1 );

for ( int i = 0; i < int( children.size() ); i++ )
{
    Print( "\t", false );
    Print( children[i] );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Parent and Child Geometry ====//
pod1 = AddGeom( "POD" )

pod2 = AddGeom( "POD", pod1 )

pod3 = AddGeom( "POD", pod2 )

print( "Children of Pod #1: " )

children = GetGeomChildren( pod1 )

for i in range(int( len(children) )):

    print( "\t", False )
    print( children[i] )
```

  


### function GetNumMainSurfs

```
int GetNumMainSurfs(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: int Number of main surfaces 

Get the number of main surfaces for the specified Geom. Multiple main surfaces may exist for CustoGeoms, propellors, etc., but does not include surfaces created due to symmetry. 

//==== Add Prop Geometry ====//
string prop_id = AddGeom( "PROP" );

int num_surf = 0;

num_surf = GetNumMainSurfs( prop_id ); // Should be the same as the number of blades

Print( "Number of Propeller Surfaces: ", false );

Print( num_surf );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Prop Geometry ====//
prop_id = AddGeom( "PROP" )

num_surf = 0

num_surf = GetNumMainSurfs( prop_id ) # Should be the same as the number of blades

print( "Number of Propeller Surfaces: ", False )

print( num_surf )
```

  


### function GetTotalNumSurfs

```
int GetTotalNumSurfs(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: Number of main surfaces 

Get the total number of surfaces for the specified Geom. This is equivalent to the number of main surface multiplied by the number of symmetric copies. 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

int num_surf = 0;

num_surf = GetTotalNumSurfs( wing_id ); // Wings default with XZ symmetry on -> 2 surfaces

Print( "Total Number of Wing Surfaces: ", false );

Print( num_surf );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

num_surf = 0

num_surf = GetTotalNumSurfs( wing_id ) # Wings default with XZ symmetry on -> 2 surfaces

print( "Total Number of Wing Surfaces: ", False )

print( num_surf )
```

  


### function GetGeomVSPSurfType

```
int GetGeomVSPSurfType(
    const std::string & geom_id,
    int main_surf_ind =0
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **main_surf_ind** Main surface index 


**See**: [VSP_SURF_TYPE](Modules/group___enumerations.md#enum-vsp-surf-type)

**Return**: VSP surface type enum (i.e. DISK_SURF) 

Get the VSP surface type of the specified Geom 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

if ( GetGeomVSPSurfType( wing_id ) != WING_SURF )
{
    Print( "---> Error: API GetGeomVSPSurfType " );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

if  GetGeomVSPSurfType( wing_id ) != WING_SURF :
    print( "---> Error: API GetGeomVSPSurfType " )
```

  


### function GetGeomVSPSurfCfdType

```
int GetGeomVSPSurfCfdType(
    const std::string & geom_id,
    int main_surf_ind =0
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **main_surf_ind** Main surface index 


**See**: [VSP_SURF_CFD_TYPE](Modules/group___enumerations.md#enum-vsp-surf-cfd-type)

**Return**: VSP surface CFD type enum (i.e. CFD_TRANSPARENT) 

Get the VSP surface CFD type of the specified Geom 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

if ( GetGeomVSPSurfCfdType( wing_id ) != CFD_NORMAL )
{
    Print( "---> Error: API GetGeomVSPSurfCfdType " );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

if  GetGeomVSPSurfCfdType( wing_id ) != CFD_NORMAL :
    print( "---> Error: API GetGeomVSPSurfCfdType " )
```

  


### function GetGeomBBoxMax

```
vec3d GetGeomBBoxMax(
    const std::string & geom_id,
    int main_surf_ind =0,
    bool ref_frame_is_absolute =true
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **main_surf_ind** Main surface index 
  * **ref_frame_is_absolute** Flag to specify absolute or body reference frame 


**See**: [GetGeomBBoxMin](Modules/group___geom.md#function-getgeombboxmin)

**Return**: Maximum coordinate of the bounding box 

Get the the maximum coordinate of the bounding box of a Geom with given main surface index. The Geom bounding box may be specified in absolute or body reference frame. 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD" );

SetParmVal( FindParm( pid, "Y_Rotation", "XForm" ), 45 );
SetParmVal( FindParm( pid, "Z_Rotation", "XForm" ), 25 );

Update();

vec3d max_pnt = GetGeomBBoxMax( pid, 0, false );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD" )

SetParmVal( FindParm( pid, "Y_Rotation", "XForm" ), 45 )
SetParmVal( FindParm( pid, "Z_Rotation", "XForm" ), 25 )

Update()

max_pnt = GetGeomBBoxMax( pid, 0, False )
```

  


### function GetGeomBBoxMin

```
vec3d GetGeomBBoxMin(
    const std::string & geom_id,
    int main_surf_ind =0,
    bool ref_frame_is_absolute =true
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **main_surf_ind** Main surface index 
  * **ref_frame_is_absolute** Flag to specify absolute or body reference frame 


**See**: [GetGeomBBoxMax](Modules/group___geom.md#function-getgeombboxmax)

**Return**: Minimum coordinate of the bounding box 

Get the the minimum coordinate of the bounding box of a Geom with given main surface index. The Geom bounding box may be specified in absolute or body reference frame. 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD" );

SetParmVal( FindParm( pid, "Y_Rotation", "XForm" ), 45 );
SetParmVal( FindParm( pid, "Z_Rotation", "XForm" ), 25 );

Update();

vec3d min_pnt = GetGeomBBoxMin( pid, 0, false );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD" )

SetParmVal( FindParm( pid, "Y_Rotation", "XForm" ), 45 )
SetParmVal( FindParm( pid, "Z_Rotation", "XForm" ), 25 )

Update()

min_pnt = GetGeomBBoxMin( pid, 0, False )
```

  


### function SplitWingXSec

```
void SplitWingXSec(
    const string & wing_id,
    int section_index
)
```


**Parameters**: 

  * **wing_id** string Geom ID 
  * **section_index** Wing section index 


**See**: [WING_DRIVERS](Modules/group___enumerations.md#enum-wing-drivers), [XSEC_DRIVERS](Modules/group___enumerations.md#enum-xsec-drivers)

Split a given wing section. 

string wing_id = AddGeom( "WING", "" );

//==== Set Wing Section Controls ====//
SplitWingXSec( wing_id, 1 );

Update();
```

 \endforcpponly \beginPythonOnly ```py

wing_id = AddGeom( "WING", "" )

#==== Set Wing Section Controls ====//
SplitWingXSec( wing_id, 1 )

Update()
```

  


### function SetDriverGroup

```
void SetDriverGroup(
    const std::string & geom_id,
    int section_index,
    int driver_0,
    int driver_1 =-1,
    int driver_2 =-1
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **section_index** Wing section index 
  * **driver_0** First driver enum (i.e. SPAN_WSECT_DRIVER) 
  * **driver_1** Second driver enum (i.e. ROOTC_WSECT_DRIVER) 
  * **driver_2** Third driver enum (i.e. TIPC_WSECT_DRIVER) 


**See**: [WING_DRIVERS](Modules/group___enumerations.md#enum-wing-drivers), [XSEC_DRIVERS](Modules/group___enumerations.md#enum-xsec-drivers)

Set the driver group for a wing section or a XSecCurve. Care has to be taken when setting these driver groups to ensure a valid combination. 

//==== Add Wing Geometry and Set Parms ====//
string wing_id = AddGeom( "WING", "" );

//==== Set Wing Section Controls ====//
SetDriverGroup( wing_id, 1, AR_WSECT_DRIVER, ROOTC_WSECT_DRIVER, TIPC_WSECT_DRIVER );

Update();

//==== Set Parms ====//
SetParmVal( wing_id, "Root_Chord", "XSec_1", 2 );
SetParmVal( wing_id, "Tip_Chord", "XSec_1", 1 );

Update();
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry and Set Parms ====//
wing_id = AddGeom( "WING", "" )

#==== Set Wing Section Controls ====//
SetDriverGroup( wing_id, 1, AR_WSECT_DRIVER, ROOTC_WSECT_DRIVER, TIPC_WSECT_DRIVER )

Update()

#==== Set Parms ====//
SetParmVal( wing_id, "Root_Chord", "XSec_1", 2 )
SetParmVal( wing_id, "Tip_Chord", "XSec_1", 1 )

Update()
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800