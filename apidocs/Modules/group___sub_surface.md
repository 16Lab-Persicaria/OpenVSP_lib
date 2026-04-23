---
title: Sub-Surface Functions
summary: Functions related to Sub-Surfaces are defined in this group. Click here to return to the main page. 

---

# Sub-Surface Functions

Functions related to Sub-Surfaces are defined in this group. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::string | **[AddSubSurf](Modules/group___sub_surface.md#function-addsubsurf)**(const std::string & geom_id, int type, int surfindex =0) |
| std::string | **[GetSubSurf](Modules/group___sub_surface.md#function-getsubsurf)**(const std::string & geom_id, int index) |
| std::vector< std::string > | **[GetSubSurf](Modules/group___sub_surface.md#function-getsubsurf)**(const std::string & geom_id, const std::string & name) |
| void | **[DeleteSubSurf](Modules/group___sub_surface.md#function-deletesubsurf)**(const std::string & geom_id, const std::string & sub_id) |
| void | **[DeleteSubSurf](Modules/group___sub_surface.md#function-deletesubsurf)**(const std::string & sub_id) |
| void | **[SetSubSurfName](Modules/group___sub_surface.md#function-setsubsurfname)**(const std::string & geom_id, const std::string & sub_id, const std::string & name) |
| void | **[SetSubSurfName](Modules/group___sub_surface.md#function-setsubsurfname)**(const std::string & sub_id, const std::string & name) |
| std::string | **[GetSubSurfName](Modules/group___sub_surface.md#function-getsubsurfname)**(const std::string & geom_id, const std::string & sub_id) |
| std::string | **[GetSubSurfName](Modules/group___sub_surface.md#function-getsubsurfname)**(const std::string & sub_id) |
| int | **[GetSubSurfIndex](Modules/group___sub_surface.md#function-getsubsurfindex)**(const std::string & sub_id) |
| std::vector< std::string > | **[GetSubSurfIDVec](Modules/group___sub_surface.md#function-getsubsurfidvec)**(const std::string & geom_id) |
| std::vector< std::string > | **[GetAllSubSurfIDs](Modules/group___sub_surface.md#function-getallsubsurfids)**() |
| int | **[GetNumSubSurf](Modules/group___sub_surface.md#function-getnumsubsurf)**(const std::string & geom_id) |
| int | **[GetSubSurfType](Modules/group___sub_surface.md#function-getsubsurftype)**(const std::string & sub_id) |
| std::vector< std::string > | **[GetSubSurfParmIDs](Modules/group___sub_surface.md#function-getsubsurfparmids)**(const std::string & sub_id) |
| void | **[IntersectSubSurf](Modules/group___sub_surface.md#function-intersectsubsurf)**(const std::string & sub_id) |
| void | **[SetIntersectSubSurfGeomID](Modules/group___sub_surface.md#function-setintersectsubsurfgeomid)**(const std::string & sub_id, const std::string & geom_id) |


## Functions Documentation

### function AddSubSurf

```
std::string AddSubSurf(
    const std::string & geom_id,
    int type,
    int surfindex =0
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **type** Sub-surface type enum (i.e. SS_RECTANGLE) 
  * **surfindex** Main surface index (default: 0) 


**See**: [SUBSURF_TYPE](Modules/group___enumerations.md#enum-subsurf-type)

**Return**: Sub-surface ID 

Add a sub-surface to the specified Geom 

string wid = AddGeom( "WING", "" );                             // Add Wing

// Note: Parm Group for SubSurfaces in the form: "SS_" + type + "_" + count (initialized at 1)
string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line

SetParmVal( wid, "Const_Line_Value", "SubSurface_1", 0.4 );     // Change Location
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

# Note: Parm Group for SubSurfaces in the form: "SS_" + type + "_" + count (initialized at 1)
ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line

SetParmVal( wid, "Const_Line_Value", "SubSurface_1", 0.4 )     # Change Location
```

  


### function GetSubSurf

```
std::string GetSubSurf(
    const std::string & geom_id,
    int index
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **index** Sub-surface index 


**Return**: Sub-surface ID 

Get the ID of the specified sub-surface 

string wid = AddGeom( "WING", "" ); // Add Wing

string ss_rec_1 = AddSubSurf( wid, SS_RECTANGLE ); // Add Sub Surface Rectangle #1

string ss_rec_2 = AddSubSurf( wid, SS_RECTANGLE ); // Add Sub Surface Rectangle #2

Print( ss_rec_2, false );

Print( " = ", false );

Print( GetSubSurf( wid, 1 ) );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" ) # Add Wing

ss_rec_1 = AddSubSurf( wid, SS_RECTANGLE ) # Add Sub Surface Rectangle #1

ss_rec_2 = AddSubSurf( wid, SS_RECTANGLE ) # Add Sub Surface Rectangle #2

print( ss_rec_2, False )

print( " = ", False )

print( GetSubSurf( wid, 1 ) )
```

  


### function GetSubSurf

```
std::vector< std::string > GetSubSurf(
    const std::string & geom_id,
    const std::string & name
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **name** string Sub surface name 


**Return**: vector<string> Vector of sub-surface ID 

Get the ID of the specified sub-surface 

string wid = AddGeom( "WING", "" ); // Add Wing

string ss_rec_1 = AddSubSurf( wid, SS_RECTANGLE ); // Add Sub Surface Rectangle #1

string ss_rec_2 = AddSubSurf( wid, SS_RECTANGLE ); // Add Sub Surface Rectangle #2

Print( ss_rec_2, false );

Print( " = ", false );

Print( GetSubSurf( wid, 1 ) );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" ) # Add Wing

ss_rec_1 = AddSubSurf( wid, SS_RECTANGLE ) # Add Sub Surface Rectangle #1

ss_rec_2 = AddSubSurf( wid, SS_RECTANGLE ) # Add Sub Surface Rectangle #2

print( ss_rec_2, False )

print( " = ", False )

print( GetSubSurf( wid, 1 ) )
```

  


### function DeleteSubSurf

```
void DeleteSubSurf(
    const std::string & geom_id,
    const std::string & sub_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **sub_id** string Sub-surface ID 


Delete the specified sub-surface 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line
string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

Print("Delete SS_Line\n");

DeleteSubSurf( wid, ss_line_id );

int num_ss = GetNumSubSurf( wid );

string num_str = string("Number of SubSurfaces: ") + formatInt( num_ss, '' ) + string("\n");

Print( num_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line
ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

print("Delete SS_Line\n")

DeleteSubSurf( wid, ss_line_id )

num_ss = GetNumSubSurf( wid )

num_str = f"Number of SubSurfaces: {num_ss}\n"

print( num_str )
```

  


### function DeleteSubSurf

```
void DeleteSubSurf(
    const std::string & sub_id
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 


Delete the specified sub-surface 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line
string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

Print("Delete SS_Line\n");

DeleteSubSurf( ss_line_id );

int num_ss = GetNumSubSurf( wid );

string num_str = string("Number of SubSurfaces: ") + formatInt( num_ss, '' ) + string("\n");

Print( num_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line
ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

print("Delete SS_Line\n")

DeleteSubSurf( ss_line_id )

num_ss = GetNumSubSurf( wid )

num_str = f"Number of SubSurfaces: {num_ss}\n"

print( num_str )
```

  


### function SetSubSurfName

```
void SetSubSurfName(
    const std::string & geom_id,
    const std::string & sub_id,
    const std::string & name
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **sub_id** string Sub-surface ID 
  * **name** string Sub-surface name 


Set the name of the specified sub-surface 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

string new_name = string("New_SS_Rec_Name");

SetSubSurfName( wid, ss_rec_id, new_name );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

new_name = "New_SS_Rec_Name"

SetSubSurfName( wid, ss_rec_id, new_name )
```

  


### function SetSubSurfName

```
void SetSubSurfName(
    const std::string & sub_id,
    const std::string & name
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 
  * **name** string Sub-surface name 


Set the name of the specified sub-surface 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

string new_name = string("New_SS_Rec_Name");

SetSubSurfName( ss_rec_id, new_name );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

new_name = "New_SS_Rec_Name"

SetSubSurfName( ss_rec_id, new_name )
```

  


### function GetSubSurfName

```
std::string GetSubSurfName(
    const std::string & geom_id,
    const std::string & sub_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **sub_id** string Sub-surface ID 


**Return**: Sub-surface name 

Get the name of the specified sub-surface 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

string rec_name = GetSubSurfName( wid, ss_rec_id );

string name_str = string("Current Name of SS_Rectangle: ") + rec_name + string("\n");

Print( name_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

rec_name = GetSubSurfName( wid, ss_rec_id )

name_str = "Current Name of SS_Rectangle: " + rec_name + "\n"

print( name_str )
```

  


### function GetSubSurfName

```
std::string GetSubSurfName(
    const std::string & sub_id
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 


**Return**: string Sub-surface name 

Get the name of the specified sub-surface 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

string rec_name = GetSubSurfName( wid, ss_rec_id );

string name_str = string("Current Name of SS_Rectangle: ") + rec_name + string("\n");

Print( name_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

rec_name = GetSubSurfName( wid, ss_rec_id )

name_str = "Current Name of SS_Rectangle: " + rec_name + "\n"

print( name_str )
```

  


### function GetSubSurfIndex

```
int GetSubSurfIndex(
    const std::string & sub_id
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 


**Return**: int Sub-surface index 

Get the index of the specified sub-surface in its parent Geom's sub-surface vector 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line
string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

int ind = GetSubSurfIndex( ss_rec_id );

string ind_str = string("Index of SS_Rectangle: ") + ind + string("\n");

Print( ind_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line
ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

ind = GetSubSurfIndex( ss_rec_id )

ind_str = f"Index of SS_Rectangle: {ind}"

print( ind_str )
```

  


### function GetSubSurfIDVec

```
std::vector< std::string > GetSubSurfIDVec(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: vector<int> Array of sub-surface IDs 

Get a vector of all sub-surface IDs for the specified geometry 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line
string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

array<string> id_vec = GetSubSurfIDVec( wid );

string id_type_str = string( "SubSurface IDs and Type Indexes -> ");

for ( uint i = 0; i < uint(id_vec.length()); i++ )
{
    id_type_str += id_vec[i];

    id_type_str += string(": ");

    id_type_str += GetSubSurfType(id_vec[i]);

    id_type_str += string("\t");
}

id_type_str += string("\n");

Print( id_type_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line
ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

id_vec = GetSubSurfIDVec( wid )

id_type_str = "SubSurface IDs and Type Indexes -> "

for i in range(len(id_vec)):

    id_type_str += id_vec[i]

    id_type_str += ": "

    id_type_str += f'{GetSubSurfType(id_vec[i])}'

    id_type_str += "\t"

id_type_str += "\n"

print( id_type_str )
```

  


### function GetAllSubSurfIDs

```
std::vector< std::string > GetAllSubSurfIDs()
```


**Return**: Array of sub-surface IDs 

Get a vector of all sub-surface IDs for the entire model 


### function GetNumSubSurf

```
int GetNumSubSurf(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** string Geom ID 


**Return**: int Number of Sub-surfaces 

Get the number of sub-surfaces for the specified Geom 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line
string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

int num_ss = GetNumSubSurf( wid );

string num_str = string("Number of SubSurfaces: ") + num_ss + string("\n");

Print( num_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line
ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

num_ss = GetNumSubSurf( wid )

num_str = "Number of SubSurfaces: {num_ss}"

print( num_str )
```

  


### function GetSubSurfType

```
int GetSubSurfType(
    const std::string & sub_id
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 


**See**: [SUBSURF_TYPE](Modules/group___enumerations.md#enum-subsurf-type)

**Return**: int Sub-surface type enum (i.e. SS_RECTANGLE) 

Get the type for the specified sub-surface (i.e. SS_RECTANGLE) 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line
string ss_rec_id = AddSubSurf( wid, SS_RECTANGLE );                        // Add Sub Surface Rectangle

array<string> id_vec = GetSubSurfIDVec( wid );

string id_type_str = string( "SubSurface IDs and Type Indexes -> ");

for ( uint i = 0; i < uint(id_vec.length()); i++ )
{
    id_type_str += id_vec[i];

    id_type_str += string(": ");

    id_type_str += GetSubSurfType(id_vec[i]);

    id_type_str += string("\t");
}

id_type_str += string("\n");

Print( id_type_str );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line
ss_rec_id = AddSubSurf( wid, SS_RECTANGLE )                        # Add Sub Surface Rectangle

id_vec = GetSubSurfIDVec( wid )

id_type_str = "SubSurface IDs and Type Indexes -> "

for i in range(len(id_vec)):

    id_type_str += id_vec[i]

    id_type_str += ": "

    id_type_str += f'{GetSubSurfType(id_vec[i])}'

    id_type_str += "\t"

id_type_str += "\n"

print( id_type_str )
```

  


### function GetSubSurfParmIDs

```
std::vector< std::string > GetSubSurfParmIDs(
    const std::string & sub_id
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 


**Return**: vector<string> Vector of Parm IDs 

Get the vector of Parm IDs for specified sub-surface 

string wid = AddGeom( "WING", "" );                             // Add Wing

string ss_line_id = AddSubSurf( wid, SS_LINE );                      // Add Sub Surface Line

// Get and list all Parm info for SS_Line
array<string> parm_id_vec = GetSubSurfParmIDs( ss_line_id );

for ( uint i = 0; i < uint(parm_id_vec.length()); i++ )
{
    string id_name_str = string("\tName: ") + GetParmName( parm_id_vec[i] ) + string(", Group: ") + GetParmDisplayGroupName( parm_id_vec[i] ) +
        string(", ID: ") + parm_id_vec[i] + string("\n");

    Print( id_name_str );
}
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

ss_line_id = AddSubSurf( wid, SS_LINE )                      # Add Sub Surface Line

# Get and list all Parm info for SS_Line
parm_id_vec = GetSubSurfParmIDs( ss_line_id )

for i in range(len(parm_id_vec)):

    id_name_str = "\tName: " + GetParmName(parm_id_vec[i]) + ", Group: " + GetParmDisplayGroupName(parm_id_vec[i]) + ", ID: " + str(parm_id_vec[i]) + "\n"


    print( id_name_str )
```

  


### function IntersectSubSurf

```
void IntersectSubSurf(
    const std::string & sub_id
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 


Trigger intersection for SS_INTERSECT type subsurfaces 

string pid = AddGeom( "POD", "" );
string p2id = AddGeom( "POD", "" );

string xpod2 = GetParm( p2id, "X_Rel_Location", "XForm" );
SetParmVal( xpod2, 4.0 );

string zrotpod2 = GetParm( p2id, "Z_Rel_Rotation", "XForm" );
SetParmVal( zrotpod2, 60.0 );

string sub_id = AddSubSurf( pid, SS_INTERSECT );

Update();

SetIntersectSubSurfGeomID( sub_id, p2id );

IntersectSubSurf( sub_id );
```

 \endforcpponly \beginPythonOnly ```py

pid = AddGeom( "POD", "" )
p2id = AddGeom( "POD", "" )

xpod2 = GetParm( p2id, "X_Rel_Location", "XForm" )
SetParmVal( xpod2, 4.0 )

zrotpod2 = GetParm( p2id, "Z_Rel_Rotation", "XForm" )
SetParmVal( zrotpod2, 60.0 )

sub_id = AddSubSurf( pid, SS_INTERSECT )

Update()

SetIntersectSubSurfGeomID( sub_id, p2id )

IntersectSubSurf( sub_id )
```

  


### function SetIntersectSubSurfGeomID

```
void SetIntersectSubSurfGeomID(
    const std::string & sub_id,
    const std::string & geom_id
)
```


**Parameters**: 

  * **sub_id** string Sub-surface ID 
  * **geom_id** string Geom ID to intersect with parent to create subsurface 


Set Geom ID to intersect parent with to create intersection SS_INTERSECT type subsurfaces 

string pid = AddGeom( "POD", "" );
string p2id = AddGeom( "POD", "" );

string xpod2 = GetParm( p2id, "X_Rel_Location", "XForm" );
SetParmVal( xpod2, 4.0 );

string zrotpod2 = GetParm( p2id, "Z_Rel_Rotation", "XForm" );
SetParmVal( zrotpod2, 60.0 );

string sub_id = AddSubSurf( pid, SS_INTERSECT );

Update();

SetIntersectSubSurfGeomID( sub_id, p2id );

IntersectSubSurf( sub_id );
```

 \endforcpponly \beginPythonOnly ```py

pid = AddGeom( "POD", "" )
p2id = AddGeom( "POD", "" )

xpod2 = GetParm( p2id, "X_Rel_Location", "XForm" )
SetParmVal( xpod2, 4.0 )

zrotpod2 = GetParm( p2id, "Z_Rel_Rotation", "XForm" )
SetParmVal( zrotpod2, 60.0 )

sub_id = AddSubSurf( pid, SS_INTERSECT )

Update()

SetIntersectSubSurfGeomID( sub_id, p2id )

IntersectSubSurf( sub_id )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800