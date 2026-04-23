---
title: File Input and Output Functions
summary: This group of functions provides file input and output interfacing through the API. Click here to return to the main page. 

---

# File Input and Output Functions

This group of functions provides file input and output interfacing through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[ReadVSPFile](Modules/group___file_i_o.md#function-readvspfile)**(const std::string & file_name) |
| void | **[WriteVSPFile](Modules/group___file_i_o.md#function-writevspfile)**(const std::string & file_name, int set =SET_ALL) |
| void | **[SetVSP3FileName](Modules/group___file_i_o.md#function-setvsp3filename)**(const std::string & file_name) |
| void | **[InsertVSPFile](Modules/group___file_i_o.md#function-insertvspfile)**(const std::string & file_name, const std::string & parent_geom_id) |
| std::string | **[ExportFile](Modules/group___file_i_o.md#function-exportfile)**(const std::string & file_name, int thick_set, int file_type, int subsFlag =1, int thin_set =[vsp::SET_NONE](Modules/group___enumerations.md#enumvalue-set-none), bool useMode =false, const string & modeID ="") |
| std::string | **[ImportFile](Modules/group___file_i_o.md#function-importfile)**(const std::string & file_name, int file_type, const std::string & parent) |
| void | **[SetBEMPropID](Modules/group___file_i_o.md#function-setbempropid)**(const string & prop_id) |


## Functions Documentation

### function ReadVSPFile

```
void ReadVSPFile(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** *.vsp3 file name 


Load an OpenVSP project from a VSP3 file 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string fname = "example_fuse.vsp3";

SetVSP3FileName( fname );

Update();

//==== Save Vehicle to File ====//
Print( "\tSaving vehicle file to: ", false );

Print( fname );

WriteVSPFile( GetVSPFileName(), SET_ALL );

//==== Reset Geometry ====//
Print( string( "--->Resetting VSP model to blank slate\n" ) );

ClearVSPModel();

ReadVSPFile( fname );
```

 

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

fname = "example_fuse.vsp3"

SetVSP3FileName( fname )

Update()

#==== Save Vehicle to File ====//
print( "\tSaving vehicle file to: ", False )

print( fname )

WriteVSPFile( GetVSPFileName(), SET_ALL )

#==== Reset Geometry ====//
print( "--->Resetting VSP model to blank slate\n" )

ClearVSPModel()

ReadVSPFile( fname )
```

  


### function WriteVSPFile

```
void WriteVSPFile(
    const std::string & file_name,
    int set =SET_ALL
)
```


**Parameters**: 

  * **file_name** *.vsp3 file name 
  * **set** Set index to write (i.e. SET_ALL) 


Save the current OpenVSP project to a VSP3 file 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string fname = "example_fuse.vsp3";

SetVSP3FileName( fname );

Update();

//==== Save Vehicle to File ====//
Print( "\tSaving vehicle file to: ", false );

Print( fname );

WriteVSPFile( GetVSPFileName(), SET_ALL );

//==== Reset Geometry ====//
Print( string( "--->Resetting VSP model to blank slate\n" ) );

ClearVSPModel();

ReadVSPFile( fname );
```

 

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

fname = "example_fuse.vsp3"

SetVSP3FileName( fname )

Update()

#==== Save Vehicle to File ====//
print( "\tSaving vehicle file to: ", False )

print( fname )

WriteVSPFile( GetVSPFileName(), SET_ALL )

#==== Reset Geometry ====//
print( "--->Resetting VSP model to blank slate\n" )

ClearVSPModel()

ReadVSPFile( fname )
```

  


### function SetVSP3FileName

```
void SetVSP3FileName(
    const std::string & file_name
)
```


**Parameters**: 

  * **file_name** File name 


Set the file name of a OpenVSP project 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string fname = "example_fuse.vsp3";

SetVSP3FileName( fname );

Update();

//==== Save Vehicle to File ====//
Print( "\tSaving vehicle file to: ", false );

Print( fname );

WriteVSPFile( GetVSPFileName(), SET_ALL );

//==== Reset Geometry ====//
Print( string( "--->Resetting VSP model to blank slate\n" ) );

ClearVSPModel();

ReadVSPFile( fname );
```

 

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

fname = "example_fuse.vsp3"

SetVSP3FileName( fname )

Update()

#==== Save Vehicle to File ====//
print( "\tSaving vehicle file to: ", False )

print( fname )

WriteVSPFile( GetVSPFileName(), SET_ALL )

#==== Reset Geometry ====//
print( "--->Resetting VSP model to blank slate\n" )

ClearVSPModel()

ReadVSPFile( fname )
```

  


### function InsertVSPFile

```
void InsertVSPFile(
    const std::string & file_name,
    const std::string & parent_geom_id
)
```


**Parameters**: 

  * **file_name** string *.vsp3 filename 
  * **parent_geom_id** string Parent geom ID (ignored with empty string) 


Insert an external OpenVSP project into the current project. All Geoms in the external project are placed as children of the specified parent. If no parent or an invalid parent is given, the Geoms are inserted at the top level. 


### function ExportFile

```
std::string ExportFile(
    const std::string & file_name,
    int thick_set,
    int file_type,
    int subsFlag =1,
    int thin_set =vsp::SET_NONE,
    bool useMode =false,
    const string & modeID =""
)
```


**Parameters**: 

  * **file_name** Export file name 
  * **thick_set** Set index to export (i.e. SET_ALL) 
  * **file_type** File type enum (i.e. EXPORT_IGES) 
  * **subsFlag** Flag to tag subsurfaces if MeshGeom is created 
  * **thin_set** Set index to export as degenerate geometry (i.e. SET_NONE) 
  * **useMode** bool Flag determine if mode is used instead of sets 
  * **modeID** string ID of Mode to use 


**See**: [EXPORT_TYPE](Modules/group___enumerations.md#enum-export-type)

**Return**: Mesh Geom ID if the export generates a mesh 

Export a file from OpenVSP. Many formats are available, such as STL, IGES, and SVG. If a mesh is generated for a particular export, the ID of the MeshGeom will be returned. If no mesh is generated an empty string will be returned. 

string wid = AddGeom( "WING" );             // Add Wing

ExportFile( "Airfoil_Metadata.csv", SET_ALL, EXPORT_SELIG_AIRFOIL );

string mesh_id = ExportFile( "Example_Mesh.msh", SET_ALL, EXPORT_GMSH );
DeleteGeom( mesh_id ); // Delete the mesh generated by the GMSH export
```

 

wid = AddGeom( "WING" )             # Add Wing

ExportFile( "Airfoil_Metadata.csv", SET_ALL, EXPORT_SELIG_AIRFOIL )

mesh_id = ExportFile( "Example_Mesh.msh", SET_ALL, EXPORT_GMSH )
DeleteGeom( mesh_id ) # Delete the mesh generated by the GMSH export
```

  


### function ImportFile

```
std::string ImportFile(
    const std::string & file_name,
    int file_type,
    const std::string & parent
)
```


**Parameters**: 

  * **file_name** Import file name 
  * **file_type** File type enum (i.e. IMPORT_PTS) 
  * **parent** Parent Geom ID (ignored with empty string) 


**See**: [IMPORT_TYPE](Modules/group___enumerations.md#enum-import-type)

Import a file into OpenVSP. Many formats are available, such as NASCART, V2, and BEM). The imported Geom, mesh, or other object is inserted as a child of the specified parent. If no parent or an invalid parent is given, the import will be done at the top level. 


### function SetBEMPropID

```
void SetBEMPropID(
    const string & prop_id
)
```


**Parameters**: 

  * **prop_id** Propeller Geom ID 


**See**: [EXPORT_TYPE](Modules/group___enumerations.md#enum-export-type), [ExportFile](Modules/group___file_i_o.md#function-exportfile)

Set the ID of the propeller to be exported to a BEM file. Call this function before ExportFile. 

//==== Add Prop Geometry ====//
string prop_id = AddGeom( "PROP" );

SetBEMPropID( prop_id );

ExportFile( "ExampleBEM.bem", SET_ALL, EXPORT_BEM );
```

 

#==== Add Prop Geometry ====//
prop_id = AddGeom( "PROP" )

SetBEMPropID( prop_id )

ExportFile( "ExampleBEM.bem", SET_ALL, EXPORT_BEM )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800