---
title: Functions for Sets
summary: The following group of API functions deals with set manipulation. Click here to return to the main page. 

---

# Functions for Sets

The following group of API functions deals with set manipulation. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| int | **[GetNumSets](Modules/group___sets.md#function-getnumsets)**() |
| void | **[SetSetName](Modules/group___sets.md#function-setsetname)**(int index, const std::string & name) |
| std::string | **[GetSetName](Modules/group___sets.md#function-getsetname)**(int index) |
| std::vector< std::string > | **[GetGeomSetAtIndex](Modules/group___sets.md#function-getgeomsetatindex)**(int index) |
| std::vector< std::string > | **[GetGeomSet](Modules/group___sets.md#function-getgeomset)**(const std::string & name) |
| int | **[GetSetIndex](Modules/group___sets.md#function-getsetindex)**(const std::string & name) |
| bool | **[GetSetFlag](Modules/group___sets.md#function-getsetflag)**(const std::string & geom_id, int set_index) |
| void | **[SetSetFlag](Modules/group___sets.md#function-setsetflag)**(const std::string & geom_id, int set_index, bool flag) |
| void | **[CopyPasteSet](Modules/group___sets.md#function-copypasteset)**(int copyIndex, int pasteIndex) |
| bool | **[GetBBoxSet](Modules/group___sets.md#function-getbboxset)**(int set, double & xmin_out, double & ymin_out, double & zmin_out, double & xlen_out, double & ylen_out, double & zlen_out) |
| bool | **[GetScaleIndependentBBoxSet](Modules/group___sets.md#function-getscaleindependentbboxset)**(int set, double & xmin_out, double & ymin_out, double & zmin_out, double & xlen_out, double & ylen_out, double & zlen_out) |


## Functions Documentation

### function GetNumSets

```
int GetNumSets()
```


**Return**: Number of sets 

Get the total number of defined sets. Named sets are used to group components and read/write on them. The number of named sets will be 10 for OpenVSP versions up to 3.17.1 and 20 for later versions. 

if ( GetNumSets() <= 0 )                            { Print( "---> Error: API GetNumSets " ); }
```

 

if  GetNumSets() <= 0 : print( "---> Error: API GetNumSets " )
```

  


### function SetSetName

```
void SetSetName(
    int index,
    const std::string & name
)
```


**Parameters**: 

  * **index** Set index 
  * **name** Set name 


**See**: [SET_TYPE](Modules/group___enumerations.md#enum-set-type)

Set the name of a set at specified index 

SetSetName( 3, "SetFromScript" );

if ( GetSetName( 3 ) != "SetFromScript" )            { Print( "---> Error: API Get/Set Set Name " ); }
```

 

SetSetName( 3, "SetFromScript" )

if GetSetName(3) != "SetFromScript":
    print("---> Error: API Get/Set Set Name")
```

  


### function GetSetName

```
std::string GetSetName(
    int index
)
```


**Parameters**: 

  * **index** Set index 


**See**: [SET_TYPE](Modules/group___enumerations.md#enum-set-type)

**Return**: Set name 

Get the name of a set at specified index 

SetSetName( 3, "SetFromScript" );

if (GetSetName(3) != "SetFromScript" )
    Print("---> Error: API Get/Set Set Name");
```

 

SetSetName( 3, "SetFromScript" )

if GetSetName(3) != "SetFromScript":
    print("---> Error: API Get/Set Set Name")
```

  


### function GetGeomSetAtIndex

```
std::vector< std::string > GetGeomSetAtIndex(
    int index
)
```


**Parameters**: 

  * **index** Set index 


**See**: [SET_TYPE](Modules/group___enumerations.md#enum-set-type)

**Return**: Array of Geom IDs 

Get an array of Geom IDs for the specified set index 

SetSetName( 3, "SetFromScript" );

array<string> @geom_arr1 = GetGeomSetAtIndex( 3 );

array<string> @geom_arr2 = GetGeomSet( "SetFromScript" );

if ( geom_arr1.size() != geom_arr2.size() )            { Print( "---> Error: API GetGeomSet " ); }
```

 

SetSetName( 3, "SetFromScript" )

geom_arr1 = GetGeomSetAtIndex( 3 )

geom_arr2 = GetGeomSet( "SetFromScript" )

if  len(geom_arr1) != len(geom_arr2) : print( "---> Error: API GetGeomSet " )
```

  


### function GetGeomSet

```
std::vector< std::string > GetGeomSet(
    const std::string & name
)
```


**Parameters**: 

  * **name** const string set name 


**Return**: array<string> array of Geom IDs 

Get an array of Geom IDs for the specified set name 

SetSetName( 3, "SetFromScript" );

array<string> @geom_arr1 = GetGeomSetAtIndex( 3 );

array<string> @geom_arr2 = GetGeomSet( "SetFromScript" );

if ( geom_arr1.size() != geom_arr2.size() )            { Print( "---> Error: API GetGeomSet " ); }
```

 

SetSetName( 3, "SetFromScript" )

geom_arr1 = GetGeomSetAtIndex( 3 )

geom_arr2 = GetGeomSet( "SetFromScript" )

if  len(geom_arr1) != len(geom_arr2) : print( "---> Error: API GetGeomSet " )
```

  


### function GetSetIndex

```
int GetSetIndex(
    const std::string & name
)
```


**Parameters**: 

  * **name** Set name 


**Return**: Set index 

Get the set index for the specified set name 

SetSetName( 3, "SetFromScript" );

if ( GetSetIndex( "SetFromScript" ) != 3 ) { Print( "ERROR: GetSetIndex" ); }
```

 

SetSetName( 3, "SetFromScript" )

if GetSetIndex("SetFromScript") != 3:
    print("ERROR: GetSetIndex")
```

  


### function GetSetFlag

```
bool GetSetFlag(
    const std::string & geom_id,
    int set_index
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **set_index** Set index 


**Return**: True if geom is in the set, false otherwise 

Check if a Geom is in the set at the specified set index 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

SetSetFlag( fuseid, 3, true );

if ( !GetSetFlag( fuseid, 3 ) )                        { Print( "---> Error: API Set/Get Set Flag " ); }
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

SetSetFlag( fuseid, 3, True )

if not GetSetFlag(fuseid, 3):
    print("---> Error: API Set/Get Set Flag")
```

  


### function SetSetFlag

```
void SetSetFlag(
    const std::string & geom_id,
    int set_index,
    bool flag
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **set_index** Set index 
  * **flag** Flag that indicates set membership 


Set whether or not a Geom is a member of the set at specified set index 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

SetSetFlag( fuseid, 3, true );

if ( !GetSetFlag( fuseid, 3 ) )                        { Print( "---> Error: API Set/Get Set Flag " ); }
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

SetSetFlag( fuseid, 3, True )

if not GetSetFlag(fuseid, 3):
    print("---> Error: API Set/Get Set Flag")
```

  


### function CopyPasteSet

```
void CopyPasteSet(
    int copyIndex,
    int pasteIndex
)
```


**Parameters**: 

  * **copyIndex** Copy Index 
  * **pasteIndex** Paste Index 


Copies all the states of a geom set and pastes them into a specific set based on passed in indexs 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

//set fuseid's state for set 3 to true
SetSetFlag( fuseid, 3, true );

//Copy set 3 and Paste into set 4
CopyPasteSet( 3, 4 );

//get fuseid's state for set 4
bool flag_value = GetSetFlag( fuseid, 4 );

if ( flag_value != true)                      { Print( "---> Error: API CopyPasteSet " ); }
```

 

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

#set fuseid's state for set 3 to true
SetSetFlag( fuseid, 3, True )

#Copy set 3 and Paste into set 4
CopyPasteSet( 3, 4 )

#get fuseid's state for set 4
flag_value = GetSetFlag( fuseid, 4 )

if  flag_value != True: print( "---> Error: API CopyPasteSet " )
```

  


### function GetBBoxSet

```
bool GetBBoxSet(
    int set,
    double & xmin_out,
    double & ymin_out,
    double & zmin_out,
    double & xlen_out,
    double & ylen_out,
    double & zlen_out
)
```


**Parameters**: 

  * **set** int Desired Set 
  * **xmin_out** double Minimum bounding box X coordinate 
  * **ymin_out** double Minimum bounding box Y coordinate 
  * **zmin_out** double Minimum bounding box Z coordinate 
  * **xlen_out** double Maximum bounding box X length 
  * **ylen_out** double Maximum bounding box Y length 
  * **zlen_out** double Maximum bounding box Z length 


**Return**: bool Flag indicating whether the set has members (is non-empty) 

Get the corners of the bounding box of the specified Set. 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD" );

Update();

double xmin, ymin, zmin, xlen, ylen, zlen;
bool sethasmembers = GetBBoxSet( SET_ALL, xmin, ymin, zmin, xlen, ylen, zlen );
```

 

#==== Add Pod Geometry ====//
pid = AddGeom( "POD" )

Update()

sethasmembers, xmin, ymin, zmin, xlen, ylen, zlen = GetBBoxSet( SET_ALL )
```

  


### function GetScaleIndependentBBoxSet

```
bool GetScaleIndependentBBoxSet(
    int set,
    double & xmin_out,
    double & ymin_out,
    double & zmin_out,
    double & xlen_out,
    double & ylen_out,
    double & zlen_out
)
```


**Parameters**: 

  * **set** int Desired Set 
  * **xmin_out** double Minimum bounding box X coordinate 
  * **ymin_out** double Minimum bounding box Y coordinate 
  * **zmin_out** double Minimum bounding box Z coordinate 
  * **xlen_out** double Maximum bounding box X length 
  * **ylen_out** double Maximum bounding box Y length 
  * **zlen_out** double Maximum bounding box Z length 


**Return**: bool Flag indicating whether the set has members (is non-empty) 

Get the corners of the scale independent bounding box of the specified Set. 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD" );

Update();

double xmin, ymin, zmin, xlen, ylen, zlen;
bool sethasmembers = GetScaleIndependentBBoxSet( SET_ALL, xmin, ymin, zmin, xlen, ylen, zlen );
```

 

#==== Add Pod Geometry ====//
pid = AddGeom( "POD" )

Update()

sethasmembers, xmin, ymin, zmin, xlen, ylen, zlen = GetScaleIndependentBBoxSet( SET_ALL );
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800