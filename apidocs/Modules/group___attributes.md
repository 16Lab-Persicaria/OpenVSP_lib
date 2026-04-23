---
title: Attributes Manager Functions
summary: This group is for functions included in the Attributes Manager. The Attributes Manager stores Attributes and provides methods to add, delete, get and set them. Click here to return to the main page. 

---

# Attributes Manager Functions

This group is for functions included in the Attributes Manager. The Attributes Manager stores Attributes and provides methods to add, delete, get and set them. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| string | **[SummarizeAttributes](Modules/group___attributes.md#function-summarizeattributes)**() |
| string | **[SummarizeAttributesAsTree](Modules/group___attributes.md#function-summarizeattributesastree)**() |
| vector< string > | **[FindAllAttributes](Modules/group___attributes.md#function-findallattributes)**() |
| vector< string > | **[FindAttributesByName](Modules/group___attributes.md#function-findattributesbyname)**(const string & search_str) |
| string | **[FindAttributeByName](Modules/group___attributes.md#function-findattributebyname)**(const string & search_str, int index) |
| string | **[FindAttributeInCollection](Modules/group___attributes.md#function-findattributeincollection)**(const string & obj_id, const string & search_str, int index) |
| vector< string > | **[FindAttributeNamesInCollection](Modules/group___attributes.md#function-findattributenamesincollection)**(const string & collID) |
| vector< string > | **[FindAttributesInCollection](Modules/group___attributes.md#function-findattributesincollection)**(const string & collID) |
| vector< string > | **[FindAttributedObjects](Modules/group___attributes.md#function-findattributedobjects)**() |
| int | **[GetObjectType](Modules/group___attributes.md#function-getobjecttype)**(const string & attachID) |
| string | **[GetObjectTypeName](Modules/group___attributes.md#function-getobjecttypename)**(const string & attachID) |
| string | **[GetObjectName](Modules/group___attributes.md#function-getobjectname)**(const string & attachID) |
| string | **[GetObjectParent](Modules/group___attributes.md#function-getobjectparent)**(const string & id) |
| string | **[GetChildCollection](Modules/group___attributes.md#function-getchildcollection)**(const string & attachID) |
| string | **[GetGeomSetCollection](Modules/group___attributes.md#function-getgeomsetcollection)**(const int & index) |
| string | **[GetAttributeName](Modules/group___attributes.md#function-getattributename)**(const string & attrID) |
| string | **[GetAttributeID](Modules/group___attributes.md#function-getattributeid)**(const string & collID, const string & attributeName, int index) |
| string | **[GetAttributeDoc](Modules/group___attributes.md#function-getattributedoc)**(const string & attrID) |
| int | **[GetAttributeType](Modules/group___attributes.md#function-getattributetype)**(const string & attrID) |
| string | **[GetAttributeTypeName](Modules/group___attributes.md#function-getattributetypename)**(const string & attrID) |
| vector< int > | **[GetAttributeBoolVal](Modules/group___attributes.md#function-getattributeboolval)**(const string & attrID) |
| vector< int > | **[GetAttributeIntVal](Modules/group___attributes.md#function-getattributeintval)**(const string & attrID) |
| vector< double > | **[GetAttributeDoubleVal](Modules/group___attributes.md#function-getattributedoubleval)**(const string & attrID) |
| vector< string > | **[GetAttributeStringVal](Modules/group___attributes.md#function-getattributestringval)**(const string & attrID) |
| vector< string > | **[GetAttributeParmID](Modules/group___attributes.md#function-getattributeparmid)**(const string & attrID) |
| vector< double > | **[GetAttributeParmVal](Modules/group___attributes.md#function-getattributeparmval)**(const string & attrID) |
| vector< string > | **[GetAttributeParmName](Modules/group___attributes.md#function-getattributeparmname)**(const string & attrID) |
| vector< vec3d > | **[GetAttributeVec3dVal](Modules/group___attributes.md#function-getattributevec3dval)**(const string & attrID) |
| vector< vector< int > > | **[GetAttributeIntMatrixVal](Modules/group___attributes.md#function-getattributeintmatrixval)**(const string & attrID) |
| vector< vector< double > > | **[GetAttributeDoubleMatrixVal](Modules/group___attributes.md#function-getattributedoublematrixval)**(const string & attrID) |
| void | **[SetAttributeName](Modules/group___attributes.md#function-setattributename)**(const string & attrID, const string & name) |
| void | **[SetAttributeDoc](Modules/group___attributes.md#function-setattributedoc)**(const string & attrID, const string & doc) |
| void | **[SetAttributeBool](Modules/group___attributes.md#function-setattributebool)**(const string & attrID, bool value) |
| void | **[SetAttributeInt](Modules/group___attributes.md#function-setattributeint)**(const string & attrID, int value) |
| void | **[SetAttributeDouble](Modules/group___attributes.md#function-setattributedouble)**(const string & attrID, double value) |
| void | **[SetAttributeString](Modules/group___attributes.md#function-setattributestring)**(const string & attrID, const string & value) |
| void | **[SetAttributeParmID](Modules/group___attributes.md#function-setattributeparmid)**(const string & attrID, const string & value) |
| void | **[SetAttributeVec3d](Modules/group___attributes.md#function-setattributevec3d)**(const string & attrID, const vector< vec3d > & value) |
| void | **[SetAttributeIntMatrix](Modules/group___attributes.md#function-setattributeintmatrix)**(const string & attrID, const vector< vector< int > > & value) |
| void | **[SetAttributeDoubleMatrix](Modules/group___attributes.md#function-setattributedoublematrix)**(const string & attrID, const vector< vector< double > > & value) |
| void | **[DeleteAttribute](Modules/group___attributes.md#function-deleteattribute)**(const string & attrID) |
| string | **[AddAttributeBool](Modules/group___attributes.md#function-addattributebool)**(const string & collID, const string & attributeName, bool value) |
| string | **[AddAttributeInt](Modules/group___attributes.md#function-addattributeint)**(const string & collID, const string & attributeName, int value) |
| string | **[AddAttributeDouble](Modules/group___attributes.md#function-addattributedouble)**(const string & collID, const string & attributeName, double value) |
| string | **[AddAttributeString](Modules/group___attributes.md#function-addattributestring)**(const string & collID, const string & attributeName, const string & value) |
| string | **[AddAttributeParm](Modules/group___attributes.md#function-addattributeparm)**(const string & collID, const string & attributeName, const string & parmID) |
| string | **[AddAttributeVec3d](Modules/group___attributes.md#function-addattributevec3d)**(const string & collID, const string & attributeName, const vector< vec3d > & value) |
| string | **[AddAttributeIntMatrix](Modules/group___attributes.md#function-addattributeintmatrix)**(const string & collID, const string & attributeName, const vector< vector< int > > & value) |
| string | **[AddAttributeDoubleMatrix](Modules/group___attributes.md#function-addattributedoublematrix)**(const string & collID, const string & attributeName, const vector< vector< double > > & value) |
| string | **[AddAttributeGroup](Modules/group___attributes.md#function-addattributegroup)**(const string & collID, const string & attributeName) |
| int | **[CopyAttribute](Modules/group___attributes.md#function-copyattribute)**(const string & attrID) |
| void | **[CutAttribute](Modules/group___attributes.md#function-cutattribute)**(const string & attrID) |
| vector< string > | **[PasteAttribute](Modules/group___attributes.md#function-pasteattribute)**(const string & coll_id) |


## Functions Documentation

### function SummarizeAttributes

```
string SummarizeAttributes()
```


**Return**: Tab-delimited summary of all Attributes in vehicle 

Print a tab-delimited summary of all Attributes in the vehicle, denoting Name, Type, Data, Description, and path from Root of vehicle to Attribute 

//==== Attributes: SummarizeAttributes ====//
string SummaryText = SummarizeAttributes();
Print( SummaryText );
```

 \endforcpponly \beginPythonOnly ```py


SummaryText = SummarizeAttributes()
print( SummaryText )
```

  


### function SummarizeAttributesAsTree

```
string SummarizeAttributesAsTree()
```


**Return**: Plain-text attribute tree of vehicle 

Print a plain-text tree summary of all Attribute in the vehicle, each branch node showing the name and ID of the VSP object in the path to the attribute 

//==== Attributes: SummarizeAttributesAsTree ====//
string SummaryTextTree = SummarizeAttributesAsTree();
Print( SummaryTextTree );
```

 \endforcpponly \beginPythonOnly ```py


SummaryTextTree = SummarizeAttributesAsTree();
print( SummaryTextTree )
```

  


### function FindAllAttributes

```
vector< string > FindAllAttributes()
```


**Return**: Vector of All Attribute IDs 

Returns a vector of string IDs for all Attributes in the vehicle 

//==== Attributes: FindAllAttributes ====//
array < string > @AttrIDs = FindAllAttributes();
for ( int i = 0; i < int( AttrIDs.size() ); ++i )
{
    Print( AttrIDs[i] );
}
```

 \endforcpponly \beginPythonOnly ```py


AttrIDs = FindAllAttributes()
for AttrID in AttrIDs:
    print( AttrID )
```

  


### function FindAttributesByName

```
vector< string > FindAttributesByName(
    const string & search_str
)
```


**Parameters**: 

  * **search_str** string for filtering attributes in model 


**Return**: Vector of string IDs of matching Attributes 

Returns all attributes that contain the string search_str within their name, case insensitive 

//==== Attributes: FindAttributesByName ====//
array < string > @AttrIDs = FindAttributesByName( "Watermark" );
for ( int i = 0; i < int( AttrIDs.size() ); ++i )
{
    Print( AttrIDs[i] );
}
```

 \endforcpponly \beginPythonOnly ```py


AttrIDs = FindAttributesByName( "Watermark" )
for AttrID in AttrIDs:
    print( AttrID )
```

  


### function FindAttributeByName

```
string FindAttributeByName(
    const string & search_str,
    int index
)
```


**Parameters**: 

  * **search_str** string for filtering attributes in model 
  * **index** int for indexing which of the vector of found attributes to select 


**Return**: Returns a StringID of the attribute indexed/searched by user, if found 

Searches all attributes that contain the search string, case insensitive, and returns the user-specified index 

//==== Attributes: FindAttributeByName ====//
string AttrID = FindAttributeByName( "Watermark", 0 );
Print( AttrID );
```

 \endforcpponly \beginPythonOnly ```py


AttrID = FindAttributeByName( "Watermark", 0 )
print( AttrID )
```

  


### function FindAttributeInCollection

```
string FindAttributeInCollection(
    const string & obj_id,
    const string & search_str,
    int index
)
```


**Parameters**: 

  * **obj_id** id of object to search within for attributes 
  * **search_str** string for filtering attributes in object 
  * **index** int for indexing which of the vector of found attributes to select 


**Return**: Returns a StringID of the attribute indexed/searched by user, if found 

Searches all attributes in an OpenVSP object or AttributeCollection that contain the search string, case insensitive, and returns the user-specified index. Works either with the ID of an object that contains an attributeCollection or just the ID of an attributeCollection. 

//==== Attributes: FindAttributeInCollection ====//
string VehID = GetVehicleID();
string AttrID = FindAttributeInCollection( VehID, "Watermark", 0 );
Print( AttrID );
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
AttrID = FindAttributeInCollection( VehID, 'Watermark', 0 )
print( AttrID )
```

  


### function FindAttributeNamesInCollection

```
vector< string > FindAttributeNamesInCollection(
    const string & collID
)
```


**Parameters**: 

  * **collID** string ID of an attribute collection 


**Return**: Array of result names 

Return a list of all attribute Names within an attribute collection 

//==== Attributes: FindAttributeNamesInCollection ====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
array < string > @AttrNames = FindAttributeNamesInCollection( CollID );
for ( int i = 0; i < int( AttrNames.size() ); ++i )
{
    Print( AttrNames[i] );
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrNames = FindAttributeNamesInCollection( CollID )
for AttrName in AttrNames:
    print( AttrName )
```

  


### function FindAttributesInCollection

```
vector< string > FindAttributesInCollection(
    const string & collID
)
```


**Parameters**: 

  * **collID** string ID of an attribute collection 


**Return**: Vector of attribute IDs in an attribute collection. 

Get all attribute IDs within a single AttributeCollection, referenced by collID 

//==== Attributes: FindAttributesInCollection ====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
array < string > @AttrIDs = FindAttributesInCollection( CollID );
for ( int i = 0; i < int( AttrIDs.size() ); ++i )
{
    Print( AttrIDs[i] );
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrIDs = FindAttributesInCollection( CollID )
for AttrID in AttrIDs:
    print( AttrID )
```

  


### function FindAttributedObjects

```
vector< string > FindAttributedObjects()
```


**Return**: Array of IDs of entities in OpenVSP that contain populated attribute collections 

Get array of IDs of all OpenVSP entities that have populated attributeCollections Includes attributeGroups 

//==== Attributes: FindAttributedObjects ====//
array < string > @AttachIDs = FindAttributedObjects();
for ( int i = 0; i < int( AttachIDs.size() ); ++i )
{
    Print( AttachIDs[i] );
}
```

 \endforcpponly \beginPythonOnly ```py


AttachIDs = FindAttributedObjects()
for AttachID in AttachIDs:
    print( AttachID )
```

  


### function GetObjectType

```
int GetObjectType(
    const string & attachID
)
```


**Parameters**: 

  * **attachID** string ID of an OpenVSP object 


**Return**: return string of object name 

Get the type of an OpenVSP Entity by ID 

//==== Attributes: GetObjectType ====//
array < string > @AttachIDs = FindAttributedObjects();
for ( int i = 0; i < int( AttachIDs.size() ); ++i )
{
    int ObjType = GetObjectType( AttachIDs[i] );
    Print( ObjType );
}
```

 \endforcpponly \beginPythonOnly ```py


AttachIDs = FindAttributedObjects()
for AttachID in AttachIDs:
    ObjType = GetObjectType( AttachID )
    print( ObjType )
```

  


### function GetObjectTypeName

```
string GetObjectTypeName(
    const string & attachID
)
```


**Parameters**: 

  * **attachID** string ID of an OpenVSP object 


**Return**: return string of object name 

Get the named type of an OpenVSP Entity by ID 

//==== Attributes: GetObjectTypeName ====//
array < string > @AttachIDs = FindAttributedObjects();
for ( int i = 0; i < int( AttachIDs.size() ); ++i )
{
    string ObjTypeName = GetObjectTypeName( AttachIDs[i] );
    Print( ObjTypeName );
}
```

 \endforcpponly \beginPythonOnly ```py

AttachIDs = FindAttributedObjects()
for AttachID in AttachIDs:
    ObjTypeName = GetObjectTypeName( AttachID )
    print( ObjTypeName )
```

  


### function GetObjectName

```
string GetObjectName(
    const string & attachID
)
```


**Parameters**: 

  * **attachID** string ID of an OpenVSP object 


**Return**: return string of object name 

Get the name of an OpenVSP Entity by ID 

//==== Attributes: GetObjectName ====//
array < string > @AttachIDs = FindAttributedObjects();
for ( int i = 0; i < int( AttachIDs.size() ); ++i )
{
    string ObjName = GetObjectName( AttachIDs[i] );
    Print( ObjName );
}
```

 \endforcpponly \beginPythonOnly ```py


AttachIDs = FindAttributedObjects()
for AttachID in AttachIDs:
    ObjName = GetObjectName( AttachID )
    print( ObjName )
```

  


### function GetObjectParent

```
string GetObjectParent(
    const string & id
)
```


**Return**: string ID of object parent 

Get the string ID of the entity's parent Attributes -> Attribute Collections Attribute Collections -> Objects that contain attribute Collections Geoms->Parent Geoms Parms->ParmContainers etc. 

//==== Attributes: GetObjectParent ====//

string WingID = AddGeom( "WING" );
string PodID = AddGeom( "POD", WingID );
string ParentID = GetObjectParent( PodID );

if ( ParentID == WingID )
{
    Print( "Parent of Pod is Wing");
}

// Get first attribute in vehicle as an example
array < string > @AttrIDs = FindAllAttributes();
string AttrID = AttrIDs[0];
string CollID = GetObjectParent( AttrID );
string CollParentObjID = GetObjectParent( CollID );
Print( CollParentObjID );
```

 \endforcpponly \beginPythonOnly ```py



WingID = AddGeom( "WING" )
PodID = AddGeom( "POD", WingID )
ParentID = GetObjectParent( PodID )

if ParentID == WingID:
    print( "Parent of Pod is Wing")

#Get first attribute in vehicle as an example
AttrID = FindAllAttributes()[0]
CollID = GetObjectParent( AttrID )
CollParentObjID = GetObjectParent( CollID )
print( CollParentObjID )
```

  


### function GetChildCollection

```
string GetChildCollection(
    const string & attachID
)
```


**Parameters**: 

  * **attachID** string ID of an OpenVSP object 


**Return**: String ID of attribute collection associated with the attachID 

Get collection ID from any OpenVSP object If ID is an attribute collection, return the same ID back If ID is an attribute group, return its nested collection 

//==== Attributes: GetChildCollection =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
Print( CollID );
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
print( CollID )
```

  


### function GetGeomSetCollection

```
string GetGeomSetCollection(
    const int & index
)
```


**Parameters**: 

  * **index** int Geom set 


**Return**: String ID of attribute collection associated with the geom set 

Get collection ID from a vehicle's GeomSet 

//==== Attributes: GetGeomSetCollection =====//
string CollID = GetGeomSetCollection( 0 );
Print( CollID );
```

 \endforcpponly \beginPythonOnly ```py


CollID = GetGeomSetCollection( 0 )
print( CollID )
```

  


### function GetAttributeName

```
string GetAttributeName(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of an attribute 


**Return**: string name of attribute 

Return the name of an attribute by its ID 

//==== Attributes: GetAttributeName =====//

array < string > @AttrIDs = FindAllAttributes();

for ( int i = 0; i < int( AttrIDs.size() ); ++i )
{
    string AttrName = GetAttributeName( AttrIDs[i] );
    Print( AttrName );
}
```

 \endforcpponly \beginPythonOnly ```py



AttrIDs = FindAllAttributes()

for AttrID in AttrIDs:
    AttrName = GetAttributeName( AttrID )
    print( AttrName )
```

  


### function GetAttributeID

```
string GetAttributeID(
    const string & collID,
    const string & attributeName,
    int index
)
```


**Parameters**: 

  * **collID** string ID of an attribute collection 
  * **attributeName** string name of an attribute in that collection 
  * **index** int index of attribute in collection 


**Return**: String ID of attribute based on collectionID and name 

Return the ID of an attribute by its name and collection ID 

//==== Attributes: GetAttributeID =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
array < string > @AttrNames = FindAttributeNamesInCollection( CollID );
for ( int i = 0; i < int( AttrNames.size() ); ++i )
{
    string AttrID = GetAttributeID( CollID, AttrNames[i], 0 );
    Print( AttrID );
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrNames = FindAttributeNamesInCollection( CollID )
for AttrName in AttrNames:
    AttrID = GetAttributeID( CollID, AttrName, 0 )
    print( AttrID )
```

  


### function GetAttributeDoc

```
string GetAttributeDoc(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Return string doc of attribute by its ID 

Return string doc of attribute by its ID 

//==== Attributes: GetAttributeDoc =====//
array < string > @AttrIDs = FindAllAttributes();
string AttrID = AttrIDs[0];
string AttrDoc = GetAttributeDoc( AttrID );
Print( AttrDoc );
```

 \endforcpponly \beginPythonOnly ```py


AttrID = FindAllAttributes()[0]
AttrDoc = GetAttributeDoc(AttrID)
print( AttrDoc )
```

  


### function GetAttributeType

```
int GetAttributeType(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Int type of attribute 

Get int enum type of attribute by ID Use in conjunction with GetAttributeTypeName for getting strings or with the following enums BOOL_DATA INT_DATA DOUBLE_DATA STRING_DATA VEC3D_DATA INT_MATRIX_DATA DOUBLE_MATRIX_DATA NAMEVAL_COLLECTION_DATA ATTR_COLLECTION_DATA 

//==== Attributes: GetAttributeType =====//
array < string > @AttrIDs = FindAllAttributes();
string AttrID = AttrIDs[0];
int AttrType = GetAttributeType( AttrID );
Print( AttrType );

// not implemented
```

 \endforcpponly \beginPythonOnly ```py


AttrID = FindAllAttributes()[0]
AttrType = GetAttributeType( AttrID )
print( AttrType )
```

  


### function GetAttributeTypeName

```
string GetAttributeTypeName(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Type of attribute as string 

Get the attribute's type as a string 

//==== Attributes: GetAttributeTypeName =====//
array < string > @AttrIDs = FindAllAttributes();
string AttrID = AttrIDs[0];
string AttrTypeName = GetAttributeTypeName( AttrID );
Print( AttrTypeName );
```

 \endforcpponly \beginPythonOnly ```py


AttrID = FindAllAttributes()[0]
AttributeTypeName = GetAttributeTypeName( AttrID )
print( AttributeTypeName )
```

  


### function GetAttributeBoolVal

```
vector< int > GetAttributeBoolVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Bool value of attribute 

Get the boolean value of a bool-type attribute 

//==== Attribute: GetAttributeBoolVal  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
bool InitVal = true;
string AttrID = AddAttributeBool( CollID, "TestBoolAttr", InitVal );

array < bool > @GetVal = GetAttributeBoolVal( AttrID );
if ( GetVal[0] == InitVal )
{
    Print( "Got matching Bool Value from Attribute" );
}
else
{
    Print( "GetAttributeBoolVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = True
AttrID = AddAttributeBool( CollID, "TestBoolAttr", InitVal )

GetVal = GetAttributeBoolVal( AttrID )
if GetVal[0] == InitVal:
    print( "Got matching Bool Value from Attribute" )
else:
    print( "GetAttributeBoolVal error!" )
```

  


### function GetAttributeIntVal

```
vector< int > GetAttributeIntVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Int value of attribute 

Get the integer value of an int-type attribute 

//==== Attribute: GetAttributeIntVal  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
int InitVal = 55;
string AttrID = AddAttributeInt( CollID, "TestIntAttr", InitVal );

array < int > @GetVal = GetAttributeIntVal( AttrID );
if ( GetVal[0] == InitVal )
{
    Print( "Got matching Int Value from Attribute" );
}
else
{
    Print( "GetAttributeIntVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = 55
AttrID = AddAttributeInt( CollID, "TestIntAttr", InitVal )

GetVal = GetAttributeIntVal( AttrID )
if GetVal[0] == InitVal:
    print( "Got matching Int Value from Attribute" )
else:
    print( "GetAttributeIntVal error!" )
```

  


### function GetAttributeDoubleVal

```
vector< double > GetAttributeDoubleVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Double value of attribute 

Get the double value of a double-type attribute 

//==== Attribute: GetAttributeDoubleVal  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
double InitVal = 3.14159;
string AttrID = AddAttributeDouble( CollID, "TestDoubleAttr", InitVal );

array < double > @GetVal = GetAttributeDoubleVal( AttrID );
if ( GetVal[0] == InitVal )
{
    Print( "Got matching Double Value from Attribute" );
}
else
{
    Print( "GetAttributeDoubleVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = 3.14159
AttrID = AddAttributeDouble( CollID, "TestDoubleAttr", InitVal )

GetVal = GetAttributeDoubleVal( AttrID )
if GetVal[0] == InitVal:
    print( "Got matching Double Value from Attribute" )
else:
    print( "GetAttributeDoubleVal error!" )
```

  


### function GetAttributeStringVal

```
vector< string > GetAttributeStringVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: String value of attribute 

Get the string value of a string-type attribute 

//==== Attribute: GetAttributeStringVal  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string InitVal = "Hello_World_of_Attributes";
string AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal );

array < string > @GetVal = GetAttributeStringVal( AttrID );
if ( GetVal[0] == InitVal )
{
    Print( "Got matching String Value from Attribute" );
}
else
{
    Print( "GetAttributeStringVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = "Hello_World_of_Attributes"
AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal )

GetVal = GetAttributeStringVal( AttrID )
if GetVal[0] == InitVal:
    print( "Got matching String Value from Attribute" )
else:
    print( "GetAttributeStringVal error!" )
```

  


### function GetAttributeParmID

```
vector< string > GetAttributeParmID(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Parm value of attribute 

Get the parm value of a parm-type attribute 

//==== Attribute: GetAttributeParmID  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );

string PodID = AddGeom( "POD", "" );
Print( "---> Test Get Parm Val" );
array < string > @ParmArray = GetGeomParmIDs( PodID );

string ParmID = ParmArray[0];
string AttrID = AddAttributeParm( CollID, "TestParmAttr", ParmID );

array < string > @GetID = GetAttributeParmID( AttrID );

if ( GetID[0] == ParmID )
{
    Print( "Got matching Parm ID from Attribute" );
}
else
{
    Print( "GetAttributeParmID error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )

PodID = AddGeom( "POD", "" )
print( "---> Test Get Parm Val" )
ParmArray = GetGeomParmIDs( PodID )

ParmID = ParmArray[0]
AttrID = AddAttributeParm( CollID, "TestParmAttr", ParmID )

GetID = GetAttributeParmID( AttrID )

if GetID[0] == ParmID:
    print( "Got matching Parm ID from Attribute" )
else:
    print( "GetAttributeParmID error!" )
```

  


### function GetAttributeParmVal

```
vector< double > GetAttributeParmVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Parm value of attribute 

Get the parm value of a parm-type attribute 

//==== Attribute: GetAttributeParmVal  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );

string PodID = AddGeom( "POD", "" );
Print( "---> Test Get Parm Val" );
array < string > @ParmArray = GetGeomParmIDs( PodID );

string ParmID = ParmArray[0];
string AttrID = AddAttributeParm( CollID, "TestParmAttr", ParmID );

double InitVal = GetParmVal( ParmID );
array < double > @GetVal = GetAttributeParmVal( AttrID );
if ( GetVal[0] == InitVal )
{
    Print( "Got matching Parm Value from Attribute" );
}
else
{
    Print( "GetAttributeParmVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )

PodID = AddGeom( "POD", "" )
print( "---> Test Get Parm Val" )
ParmArray = GetGeomParmIDs( PodID )

ParmID = ParmArray[0]
AttrID = AddAttributeParm( CollID, "TestParmAttr", ParmID )

InitVal = GetParmVal( ParmID )
GetVal = GetAttributeParmVal( AttrID )

if GetVal[0] == InitVal:
    print( "Got matching Parm Value from Attribute" )
else:
    print( "GetAttributeParmVal error!" )
```

  


### function GetAttributeParmName

```
vector< string > GetAttributeParmName(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Parm name of attribute 

Get the name of the referenced parm of a parm-type attribute 

//==== Attribute: GetAttributeParmName  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );

string PodID = AddGeom( "POD", "" );
Print( "---> Test Get Parm Val" );
array < string > @ParmArray = GetGeomParmIDs( PodID );
string AttrName = "Example_Parm_Attr";
string ParmID = ParmArray[0];

AddAttributeParm( CollID, AttrName, ParmID );
string AttrID = GetAttributeID( CollID, AttrName, 0 );
string ParmName = GetAttributeParmName( AttrID )[0];

if ( ParmName == GetParmName( ParmID ) )
{
    Print( "Got matching Parm Name from Attribute" );
}
else
{
    Print( "GetAttributeParmName error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
PodID = AddGeom( "POD", "" )
print( "---> Test Get Parm Val" )
ParmArray = GetGeomParmIDs( PodID )
AttrName = 'Example_Parm_Attr'
ParmID = ParmArray[0]
AddAttributeParm( CollID, AttrName, ParmID )
AttrID = GetAttributeID( CollID, AttrName, 0 )
ParmName = GetAttributeParmName( AttrID )[0]
if ParmName == GetParmName( ParmID ):
    print( "Got matching Parm Name from Attribute" )
else:
    print( "GetAttributeParmName error!" )
```

  


### function GetAttributeVec3dVal

```
vector< vec3d > GetAttributeVec3dVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Vec3d value of attribute 

Get the vec3d value of a string-type attribute 

//==== Attribute: GetAttributeVec3dVal  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );

vec3d InitVal = vec3d( 1., 0.5, -4. );
string AttrID = AddAttributeVec3d( CollID, "TestVec3dAttr", {InitVal} );

array < vec3d > @Vec3dVal = GetAttributeVec3dVal( AttrID );
if ( Vec3dVal[0].x() == InitVal.x() and Vec3dVal[0].y() == InitVal.y() and Vec3dVal[0].z() == InitVal.z() )
{
    Print( "Got matching Vec3d Value from Attribute" );
}
else
{
    Print( "GetAttributeVec3dVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = vec3d([1., 0.5, -4.])
AttrID = AddAttributeVec3d( CollID, "TestVec3dAttr", [InitVal] )

Vec3dVal = GetAttributeVec3dVal( AttrID )
if ( Vec3dVal[0].x() == InitVal.x() ) and ( Vec3dVal[0].y() == InitVal.y() ) and ( Vec3dVal[0].z() == InitVal.z() ):
    print( "Got matching Vec3d Value from Attribute" )
else:
    print( "GetAttributeVec3dVal error!" )
```

  


### function GetAttributeIntMatrixVal

```
vector< vector< int > > GetAttributeIntMatrixVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Int Matrix value of attribute as vector < vector < int > > 

Get the Int Matrix of an Int-matrix-type attribute 

//==== Attribute: GetAttributeIntMatrixVal  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );

array < array < int > > InitVal = { {0, 1} , {-4, -1000} };
string AttrID = AddAttributeIntMatrix( CollID, "TestIntMatrixAttr", InitVal );

array < array < int > > IntMatrixVal = GetAttributeIntMatrixVal( AttrID );

// can also get object handle to the int array with an @ handle declaration!
array < array < int > > @IntMatrixValJHandle = GetAttributeIntMatrixVal( AttrID );

if ( IntMatrixVal == InitVal )
{
    Print( "Got matching IntMatrix Value from Attribute" );
}
else
{
    Print( "GetAttributeIntMatrixVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = [[0, 1,],[-4, -1000]]
AttrID = AddAttributeIntMatrix( CollID, "TestIntMatrixAttr", InitVal )

IntMatrixVal = GetAttributeIntMatrixVal( AttrID )
IntMatrixVal = [list(row) for row in IntMatrixVal]

if IntMatrixVal == InitVal:
    print( "Got matching IntMatrix Value from Attribute" )
else:
    print( "GetAttributeIntMatrixVal error!" )
```

  


### function GetAttributeDoubleMatrixVal

```
vector< vector< double > > GetAttributeDoubleMatrixVal(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute 


**Return**: Double Matrix value of attribute as vector < vector < Double > > 

Get the Double Matrix of an Double-matrix-type attribute 

//==== Attribute: GetAttributeDoubleMatrixVal  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
array < array < double > > InitVal = {{0., 1.},{-4., -1000.}};
string AttrID = AddAttributeDoubleMatrix( CollID, "TestDoubleMatrixAttr", InitVal );

array < array < double > > DblMatrixVal = GetAttributeDoubleMatrixVal( AttrID );

if ( DblMatrixVal == InitVal )
{
    Print( "Got matching DoubleMatrix Value from Attribute" );
}
else
{
    Print( "GetAttributeDoubleMatrixVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py


VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = [[0., 1.,],[-4., -1000.]]
AttrID = AddAttributeDoubleMatrix( CollID, "TestDoubleMatrixAttr", InitVal )

DblMatrixVal = GetAttributeDoubleMatrixVal( AttrID )
DblMatrixVal = [list(row) for row in DblMatrixVal]

if DblMatrixVal == InitVal:
    print( "Got matching Double Matrix Value from Attribute" )
else:
    print( "GetAttributeDoubleMatrixVal error!" )
```

  


### function SetAttributeName

```
void SetAttributeName(
    const string & attrID,
    const string & name
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **name** string name for attribute 


Set the name of an Attribute by ID 

//==== Attribute: SetAttributeName  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string InitVal = "Hello_World_of_Attributes";
string AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal );

string NameString = "NewName_Example";
SetAttributeName( AttrID, NameString );
string AttrName = GetAttributeName( AttrID );
if ( NameString == AttrName )
{
    Print( "Got matching name from Attribute" );
}
else
{
    Print( "SetAttributeName error!" );
    __failure++;
}

//==== Write Some Fake Test Results =====//
// not implemented
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = "Hello_World_of_Attributes"
AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal )

NameString = 'NewName_Example'
SetAttributeName( AttrID, NameString )
AttrName = GetAttributeName( AttrID )
if NameString == AttrName:
    print( "Got matching name from Attribute")
else:
    print( "SetAttributeName error!" )
```

  


### function SetAttributeDoc

```
void SetAttributeDoc(
    const string & attrID,
    const string & doc
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **doc** string of documentation for attribute 


Set the docstring of an Attribute by ID 

//==== Attribute: SetAttributeDoc  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string InitVal = "Hello_World_of_Attributes";
string AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal );

string DocString = "New_docstring_for_attribute";

SetAttributeDoc( AttrID, DocString );
string NewDocString = GetAttributeDoc( AttrID );

if ( NewDocString == DocString )
{
    Print( "Got matching DocString from Attribute" );
}
else
{
    Print( "SetAttributeDoc error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = "Hello_World_of_Attributes"
AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal )

DocString = 'New_docstring_for_attribute'

SetAttributeDoc( AttrID, DocString )
NewDocString = GetAttributeDoc( AttrID )
if NewDocString == DocString:
    print( "Got matching DocString from Attribute")
else:
    print( "SetAttributeDoc error!" )
```

  


### function SetAttributeBool

```
void SetAttributeBool(
    const string & attrID,
    bool value
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **value** boolean value for attribute 


Set the Bool value of a bool-type Attribute by ID 

//==== Attribute: SetAttributeBool  =====//
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
bool InitVal = true;
string AttrID = AddAttributeBool( CollID, "TestBoolAttr", InitVal );

bool SetVal = false;
SetAttributeBool( AttrID, SetVal );

array < bool > @GetVal = GetAttributeBoolVal( AttrID );
if ( GetVal[0] == SetVal )
{
    Print( "Set matching Bool Value from Attribute" );
}
else
{
    Print( "SetAttributeBoolVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = True
AttrID = AddAttributeBool( CollID, "TestBoolAttr", InitVal )

SetVal = False
SetAttributeBool( AttrID, SetVal )

GetVal = GetAttributeBoolVal( AttrID )
if GetVal[0] == SetVal:
    print( "Set matching Bool Value from Attribute" )
else:
    print( "SetAttributeBoolVal error!" )
```

  


### function SetAttributeInt

```
void SetAttributeInt(
    const string & attrID,
    int value
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **value** int value for attribute 


Set the Int value of an int-type Attribute by ID 

//==== Attribute: SetAttributeInt  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
int InitVal = 55;
string AttrID = AddAttributeInt( CollID, "TestIntAttr", InitVal );

int NewIntVal = -55;

SetAttributeInt( AttrID, NewIntVal );
array < int > @GetVal = GetAttributeIntVal( AttrID );
if ( GetVal[0] == NewIntVal )
{
    Print( "Set matching Int Value from Attribute" );
}
else
{
    Print( "SetAttributeIntVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = 55
AttrID = AddAttributeInt( CollID, "TestIntAttr", InitVal )

NewIntVal = -55

SetAttributeInt( AttrID, NewIntVal )
GetVal = GetAttributeIntVal( AttrID )
if GetVal[0] == NewIntVal:
    print( "Set matching Int Value from Attribute" )
else:
    print( "SetAttributeIntVal error!" )
```

  


### function SetAttributeDouble

```
void SetAttributeDouble(
    const string & attrID,
    double value
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **value** double value for attribute 


Set the Double value of a double-type Attribute by ID 

//==== Attribute: SetAttributeDouble  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
double InitVal = 3.14159;
string AttrID = AddAttributeDouble( CollID, "TestDoubleAttr", InitVal );

double DoubleVal = 3.15;

SetAttributeDouble( AttrID, DoubleVal );

array < double > @GetVal = GetAttributeDoubleVal( AttrID );
if ( GetVal[0] == DoubleVal )
{
    Print( "Set matching Double Value from Attribute" );
}
else
{
    Print( "SetAttributeDoubleVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = 3.14159
AttrID = AddAttributeDouble( CollID, "TestDoubleAttr", InitVal )

DoubleVal = 3.15

SetAttributeDouble( AttrID, DoubleVal )

GetVal = GetAttributeDoubleVal( AttrID )
if GetVal[0] == DoubleVal:
    print( "Set matching Double Value from Attribute" )
else:
    print( "SetAttributeDoubleVal error!" )
```

  


### function SetAttributeString

```
void SetAttributeString(
    const string & attrID,
    const string & value
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **value** string value for attribute 


Set the String value of a string-type Attribute by ID 

//==== Attribute: SetAttributeString  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string InitVal = "Hello_World_of_Attributes";
string AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal );

string StringVal = "Du bist supergeil!";
SetAttributeString( AttrID, StringVal );

array < string > @GetVal = GetAttributeStringVal( AttrID );
if ( GetVal[0] == StringVal )
{
    Print( "Got matching String Value from Attribute" );
}
else
{
    Print( "GetAttributeStringVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = "Hello_World_of_Attributes"
AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal )

StringVal = "Du bist supergeil!"
SetAttributeString( AttrID, StringVal )

GetVal = GetAttributeStringVal( AttrID )
if GetVal[0] == StringVal:
    print( "Got matching String Value from Attribute" )
else:
    print( "GetAttributeStringVal error!" )
```

  


### function SetAttributeParmID

```
void SetAttributeParmID(
    const string & attrID,
    const string & value
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **value** string value for attribute 


Set the ParmID value of a Parm-type Attribute by ID 

//==== Attribute: SetAttributeParmID  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );

string PodID = AddGeom( "POD", "" );
Print( "---> Test Get Parm Val" );
array < string > @ParmArray = GetGeomParmIDs( PodID );

string ParmID = ParmArray[0];
string AttrID = AddAttributeParm( CollID, "TestParmAttr", ParmID );

string NewParmID = ParmArray[1];
SetAttributeParmID( AttrID, NewParmID );
array < string > @GetID = GetAttributeParmID( AttrID );

if ( GetID[0] == NewParmID )
{
    Print( "Set matching Parm ID from Attribute" );
}
else
{
    Print( "SetAttributeParmID error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )

PodID = AddGeom( "POD", "" )
print( "---> Test Get Parm Val" )
ParmArray = GetGeomParmIDs( PodID )

ParmID = ParmArray[0]
AttrID = AddAttributeParm( CollID, "TestParmAttr", ParmID )

NewParmID = ParmArray[1]
SetAttributeParmID( AttrID, NewParmID )
GetID = GetAttributeParmID( AttrID )

if GetID[0] == NewParmID:
    print( "Set matching Parm ID from Attribute" )
else:
    print( "SetAttributeParmID error!" )
```

  


### function SetAttributeVec3d

```
void SetAttributeVec3d(
    const string & attrID,
    const vector< vec3d > & value
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **value** vec3d value for attribute 


Set the Vec3d value of a Vec3d-type Attribute by ID 

//==== Attribute: SetAttributeVec3d  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
vec3d InitVal = vec3d( 1., 0.5, -4. );
string AttrID = AddAttributeVec3d( CollID, "TestVec3dAttr", { InitVal } );

vec3d Vec3dVal = vec3d( 0.5, 0.75, -0.4 );
SetAttributeVec3d( AttrID, {Vec3dVal} );

array < vec3d > @GetVal = GetAttributeVec3dVal( AttrID );
if ( GetVal[0].x() == Vec3dVal.x() and GetVal[0].y() == Vec3dVal.y() and GetVal[0].z() == Vec3dVal.z() )
{
    Print( "Set matching Vec3d Value from Attribute" );
}
else
{
    Print( "SetAttributeVec3dVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = vec3d([1., 0.5, -4.])
AttrID = AddAttributeVec3d( CollID, "TestVec3dAttr", [InitVal] )

Vec3dVal = vec3d([0.5, 0.75, -0.4])
SetAttributeVec3d( AttrID, [Vec3dVal] )

GetVal = GetAttributeVec3dVal( AttrID )
if ( GetVal[0].x() == Vec3dVal.x() ) and ( GetVal[0].y() == Vec3dVal.y() ) and ( GetVal[0].z() == Vec3dVal.z() ):
    print( "Set matching Vec3d Value from Attribute" )
else:
    print( "SetAttributeVec3dVal error!" )
```

  


### function SetAttributeIntMatrix

```
void SetAttributeIntMatrix(
    const string & attrID,
    const vector< vector< int > > & value
)
```




```
Set the int matrix of a int-matrix-type Attribute by ID
\forcpponly
\code{.cpp}
//==== Write Some Fake Test Results =====//
// not implemented
\endcode
```

 ==== Attribute: SetAttributeIntMatrix =====// 

```
string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
array < array < int > > InitVal = {{0, 1},{-4, -1000}};
string AttrID = AddAttributeIntMatrix( CollID, "TestIntMatrixAttr", InitVal );

array < array < int > > NewImatVal = [[1,5],[-8,0]];
SetAttributeIntMatrix( AttrID, NewImatVal );

array < array < int > > IntMatrixVal = GetAttributeIntMatrixVal( AttrID );

if ( IntMatrixVal == NewImatVal )
{
    Print( "Set matching IntMatrix Value from Attribute" );
}
else
{
    Print( "SetAttributeIntMatrixVal error!" );
    __failure++;
}

\code{.py}
##==== Attribute: SetAttributeIntMatrix  =====##

VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = [[0, 1,],[-4, -1000]]
AttrID = AddAttributeIntMatrix( CollID, "TestIntMatrixAttr", InitVal )

ImatVal = [[1,5],[-8,0]]
SetAttributeIntMatrix( AttrID, ImatVal )

IntMatrixVal = GetAttributeIntMatrixVal( AttrID )
IntMatrixVal = [list(row) for row in IntMatrixVal]

if IntMatrixVal == ImatVal:
    print( "Set matching IntMatrix Value from Attribute" )
else:
    print( "SetAttributeIntMatrixVal error!" )

\endcode

\param [in] attrID string of attribute ID
\param [in] value int matrix value for attribute
```


### function SetAttributeDoubleMatrix

```
void SetAttributeDoubleMatrix(
    const string & attrID,
    const vector< vector< double > > & value
)
```


**Parameters**: 

  * **attrID** string of attribute ID 
  * **value** double matrix value for attribute 


Set the double matrix of a double-matrix-type Attribute by ID 

//==== Attribute: SetAttributeDoubleMatrix  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
array < array < double > > InitVal = {{0., 1.},{-4., -1000.}};
string AttrID = AddAttributeDoubleMatrix( CollID, "TestDoubleMatrixAttr", InitVal );

array < array < double > > NewDmatVal = {{0.,1.5},{8.4,1.1566}};
SetAttributeDoubleMatrix( AttrID, NewDmatVal );

array < array < double > > DblMatrixVal = GetAttributeDoubleMatrixVal( AttrID );

if ( DblMatrixVal == NewDmatVal )
{
    Print( "Got matching Double Matrix Value from Attribute" );
}
else
{
    Print( "GetAttributeDoubleMatrixVal error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = [[0., 1.,],[-4., -1000.]]
AttrID = AddAttributeDoubleMatrix( CollID, "TestDoubleMatrixAttr", InitVal )

NewDmatVal = [[0.,1.5],[8.4,1.1566]]
SetAttributeDoubleMatrix( AttrID, NewDmatVal )

DblMatrixVal = GetAttributeDoubleMatrixVal( AttrID )
DblMatrixVal = [list(row) for row in DblMatrixVal]

if DblMatrixVal == NewDmatVal:
    print( "Got matching Double Matrix Value from Attribute" )
else:
    print( "GetAttributeDoubleMatrixVal error!" )
```

  


### function DeleteAttribute

```
void DeleteAttribute(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string of attribute ID 


Delete attribute by attribute ID 

//==== Attribute: DeleteAttribute  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string InitVal = "This_Attribute_Will_Be_Deleted";
string AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal );

bool AttrAdded = false;
bool AttrDeleted = true;

array < string > @AttrIDs = FindAllAttributes();
for ( int i = 0; i < int( AttrIDs.size() ); i++ )
{
    if ( AttrID == AttrIDs[i] )
    {
        AttrAdded = true;
    }
}

DeleteAttribute( AttrID );

array < string > @NewAttrIDs = FindAllAttributes();
for ( int i = 0; i < int( NewAttrIDs.size() ); i++ )
{
    if ( AttrID == NewAttrIDs[i] )
    {
        AttrDeleted = false;
    }
}

if ( AttrAdded and AttrDeleted )
{
    Print( "Attribute successfully deleted" );
}
else
{
    Print( "DeleteAttribute error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = "This_Attribute_Will_Be_Deleted"
AttrID = AddAttributeString( CollID, "TestStringAttr", InitVal )


AttrIDs = FindAllAttributes()
AttrAdded = AttrID in AttrIDs

DeleteAttribute( AttrID )
NewAttrIDs = FindAllAttributes()
AttrDeleted = AttrID not in NewAttrIDs

if AttrAdded and AttrDeleted:
    print( "Attribute successfully deleted" )
else:
    print( "DeleteAttribute error!" )
```

  


### function AddAttributeBool

```
string AddAttributeBool(
    const string & collID,
    const string & attributeName,
    bool value
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **value** boolean value of new attribute 


Add a boolean attribute by name to an attribute collection 

//==== Attribute: AddAttributeBool  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
bool InitVal = true;
string AttrID = AddAttributeBool( CollID, "TestBoolAttr", InitVal );

array < bool > @GetVal = GetAttributeBoolVal( AttrID );
if ( GetVal[0] == InitVal )
{
    Print( "Added Bool Attribute" );
}
else
{
    Print( "AddAttributeBool error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = True
AttrID = AddAttributeBool( CollID, "TestBoolAttr", InitVal )

GetVal = GetAttributeBoolVal( AttrID )
if GetVal[0] == InitVal:
    print( "Added Bool Attribute" )
else:
    print( "AddAttributeBool error!" )
```

  


### function AddAttributeInt

```
string AddAttributeInt(
    const string & collID,
    const string & attributeName,
    int value
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **value** integer value of new attribute 


Add a integer attribute by name to an attribute collection 

//==== Attribute: AddAttributeInt  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
int InitVal = 55;
string AttrID = AddAttributeInt( CollID, "TestIntAttr", InitVal );

array < int > @GetVal = GetAttributeIntVal( AttrID );
if ( GetVal[0] == InitVal )
{
    Print( "Added Int Attribute" );
}
else
{
    Print( "AddAttributeInt error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
InitVal = 55
AttrID = AddAttributeInt( CollID, "TestIntAttr", InitVal )

GetVal = GetAttributeIntVal( AttrID )
if GetVal[0] == InitVal:
    print( "Added Int Attribute" )
else:
    print( "AddAttributeInt error!" )
```

  


### function AddAttributeDouble

```
string AddAttributeDouble(
    const string & collID,
    const string & attributeName,
    double value
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **value** double value of new attribute 


Add a double attribute by name to an attribute collection 

//==== Attribute: AddAttributeDouble  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = 'Example_Double_Attr';
double DoubleValue = 3.14159;
string AttrID = AddAttributeDouble( CollID, AttrName, DoubleValue );

array < double > @GetVal = GetAttributeDoubleVal( AttrID );
if ( GetVal[0] == DoubleValue )
{
    Print( "Added Double Attribute" );
}
else
{
    Print( "AddAttributeDouble error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_Double_Attr'
DoubleValue = 3.14159
AttrID = AddAttributeDouble( CollID, AttrName, DoubleValue )

GetVal = GetAttributeDoubleVal( AttrID )
if GetVal[0] == DoubleValue:
    print( "Added Double Attribute" )
else:
    print( "AddAttributeDouble error!" )
```

  


### function AddAttributeString

```
string AddAttributeString(
    const string & collID,
    const string & attributeName,
    const string & value
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **value** string value of new attribute 


Add a string attribute by name to an attribute collection 

//==== Attribute: AddAttributeString  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_String_Attr";
string StringValue = "Example_String_Attr_DataVal";
string AttrID = AddAttributeString( CollID, AttrName, StringValue );

array < string > @GetVal = GetAttributeStringVal( AttrID );
if ( GetVal[0] == StringValue )
{
    Print( "Added String Attribute" );
}
else
{
    Print( "AddAttributeString error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_String_Attr'
StringValue = 'Example_String_Attr_DataVal'
AttrID = AddAttributeString( CollID, AttrName, StringValue )

GetVal = GetAttributeStringVal( AttrID )
if GetVal[0] == StringValue:
    print( "Added String Attribute" )
else:
    print( "AddAttributeString error!" )
```

  


### function AddAttributeParm

```
string AddAttributeParm(
    const string & collID,
    const string & attributeName,
    const string & parmID
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **parmID** string Parm ID to add to attribute 


Add a parm attribute by name to an attribute collection 

//==== Attribute: AddAttributeParm  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string PodID = AddGeom( "POD", "" );

Print( "---> Test Add Parm Attr" );

array < string > @ParmArray = GetGeomParmIDs( PodID );
string ParmID = ParmArray[0];

string AttrName = "Example_Parm_Attr";
string AttrID = AddAttributeParm( CollID, AttrName, ParmID );

array < string > @GetVal = GetAttributeParmID( AttrID );
if ( GetVal[0] == ParmID )
{
    Print( "Added Parm Attribute" );
}
else
{
    Print( "AddAttributeParm error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
pid = AddGeom( "POD", "" )
print( "---> Test Add Parm Attr" )
parm_array = GetGeomParmIDs( pid )
AttrName = 'Example_Parm_Attr'
ParmID = parm_array[0]
AttrID = AddAttributeParm( CollID, AttrName, ParmID )

GetVal = GetAttributeParmID( AttrID )
if GetVal[0] == ParmID:
    print( "Added Parm Attribute" )
else:
    print( "AddAttributeParm error!" )
```

  


### function AddAttributeVec3d

```
string AddAttributeVec3d(
    const string & collID,
    const string & attributeName,
    const vector< vec3d > & value
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **value** Vec3d value of new attribute 


Add a Vec3d attribute by name to an attribute collection use vec3d() to create a vec3d object to pass into the args! 

//==== Attribute: AddAttributeVec3d  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_Vec3D_Attr";
vec3d Vec3dVal = vec3d( 0.5, 0.75, -0.4 );
string AttrID = AddAttributeVec3d( CollID, AttrName, { Vec3dVal } );

array < vec3d > @GetVal = GetAttributeVec3dVal( AttrID );

if ( GetVal[0].x() == Vec3dVal.x() and GetVal[0].y() == Vec3dVal.y() and GetVal[0].z() == Vec3dVal.z() )
{
    Print( "Added Vec3d Attribute" );
}
else
{
    Print( "AddAttributeVec3d error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_Vec3D_Attr'
Vec3dVal = vec3d( 0.5, 0.75, -0.4 )
AttrID = AddAttributeVec3d( CollID, AttrName, [Vec3dVal] )

GetVal = GetAttributeVec3dVal( AttrID )
if ( GetVal[0].x() == Vec3dVal.x() ) and ( GetVal[0].y() == Vec3dVal.y() ) and ( GetVal[0].z() == Vec3dVal.z() ):
    print( "Added Vec3d Attribute" )
else:
    print( "AddAttributeVec3d error!" )
```

  


### function AddAttributeIntMatrix

```
string AddAttributeIntMatrix(
    const string & collID,
    const string & attributeName,
    const vector< vector< int > > & value
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **value** int matrix value of new attribute 


Add an Int Matrix attribute by name to an attribute collection use nested vectors/arrays of ints for matrix argument 

//==== Attribute: AddAttributeIntMatrix  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_IntMatrix_Attr";
array < array < int > > IntMatrix = {{1,5},{-8,0}};
string AttrID = AddAttributeIntMatrix( CollID, AttrName, IntMatrix );

array < array < int > > IntMatrixVal = GetAttributeIntMatrixVal( AttrID );

if ( IntMatrixVal == IntMatrix )
{
    Print( "Added IntMatrix Attribute" );
}
else
{
    Print( "AddAttributeIntMatrix error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_IntMatrix_Attr'
IntMatrix = [[1,5],[-8,0]]
AttrID = AddAttributeIntMatrix( CollID, AttrName, IntMatrix )

IntMatrixVal = GetAttributeIntMatrixVal( AttrID )
IntMatrixVal = [list(row) for row in IntMatrixVal]

if IntMatrixVal == IntMatrix:
    print( "Added IntMatrix Attribute" )
else:
    print( "AddAttributeIntMatrix error!" )
```

  


### function AddAttributeDoubleMatrix

```
string AddAttributeDoubleMatrix(
    const string & collID,
    const string & attributeName,
    const vector< vector< double > > & value
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute 
  * **value** Double matrix value of new attribute 


Add an Double Matrix attribute by name to an attribute collection use nested vectors/arrays of ints for matrix argument 

//==== Attribute: AddAttributeDoubleMatrix  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_DoubleMat_Attr";
array < array < double > > DoubleMatrix = {{0.,1.5},{8.4,1.1566}};
string AttrID = AddAttributeDoubleMatrix( CollID, AttrName, DoubleMatrix );

array < array < double > > DoubleMatrixVal = GetAttributeDoubleMatrixVal( AttrID );

if ( DoubleMatrixVal == DoubleMatrix )
{
    Print( "Added DoubleMatrix Attribute" );
}
else
{
    Print( "AddAttributeDoubleMatrix error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_DoubleMat_Attr'
DoubleMatrix = [[0.,1.5],[8.4,1.1566]]
AttrID = AddAttributeDoubleMatrix( CollID, AttrName, DoubleMatrix )

DoubleMatrixVal = GetAttributeDoubleMatrixVal( AttrID )
DoubleMatrixVal = [list(row) for row in DoubleMatrixVal]

if DoubleMatrixVal == DoubleMatrix:
    print( "Added DoubleMatrix Attribute" )
else:
    print( "AddAttributeDoubleMatrix error!" )
```

  


### function AddAttributeGroup

```
string AddAttributeGroup(
    const string & collID,
    const string & attributeName
)
```


**Parameters**: 

  * **collID** string ID of attribute collection 
  * **attributeName** string name of new attribute group 


Add an empty Attribute Group-type attribute by name to an attribute collection 

//==== Attribute: AddAttributeGroup  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_Attr_Group";
string AttrID = AddAttributeGroup( CollID, AttrName );

if ( GetAttributeType( AttrID ) == RES_DATA_TYPE::ATTR_COLLECTION_DATA )
{
    Print( "Added Attribute Group" );
}
else
{
    Print( "AddAttributeGroup error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_Attr_Group'
AttrID = AddAttributeGroup( CollID, AttrName )
if GetAttributeType( AttrID ) == ATTR_COLLECTION_DATA:
    print( "Added Attribute Group" )
else:
    print( "AddAttributeGroup error!" )
```

  


### function CopyAttribute

```
int CopyAttribute(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute to be copied 


Copy an attribute to the clipboard by attributeID 

//==== Attribute: CopyAttribute  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_String_Attr";
string StringValue = "Example_String_Attr_DataVal";

string AttrID = AddAttributeString( CollID, AttrName, StringValue );
int CopyError = CopyAttribute( AttrID );

if ( CopyError == 0 )
{
    Print("Successfully copied Attribute");
}
else
{
    Print("CopyAttribute Error!");
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_String_Attr'
StringValue = 'Example_String_Attr_DataVal'
AttrID = AddAttributeString( CollID, AttrName, StringValue )
CopyError = CopyAttribute( AttrID )
if not CopyError:
    print("Successfully copied Attribute")
else:
    print("CopyAttribute Error!")
```

  


### function CutAttribute

```
void CutAttribute(
    const string & attrID
)
```


**Parameters**: 

  * **attrID** string ID of attribute to be copied 


Cut an attribute from its collection to the clipboard by attributeID 

//==== Attribute: CopyAttribute  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_String_Attr";
string StringValue = "Example_String_Attr_DataVal";

string AttrID = AddAttributeString( CollID, AttrName, StringValue );
CutAttribute( AttrID );

string NewCollID = GetChildCollection( "_AttrWMGroup" );
array < string > @PastedAttrIDs = PasteAttribute( NewCollID );

bool MatchIDs = PastedAttrIDs[0] == AttrID;
bool AttrInColl = false;

array < string > OldAttrIDs = FindAttributesInCollection( CollID );
for ( int i = 0; i < int( OldAttrIDs.size() ); i++ )
{
    if ( AttrID == OldAttrIDs[i] )
    {
        AttrInColl = true;
    }
}

if ( MatchIDs and not AttrInColl )
{
    Print( "Successfully Cut Attribute" );
}
else
{
    Print( "CutAttribute Error!" );
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_String_Attr'
StringValue = 'Example_String_Attr_DataVal'
AttrID = AddAttributeString( CollID, AttrName, StringValue )
CutAttribute( AttrID )

NewCollID = GetChildCollection( "_AttrWMGroup" )
NewAttrIDs = PasteAttribute( NewCollID )

MatchIDs = NewAttrIDs[0] == AttrID
Attr_Cut_Check = AttrID not in FindAttributesInCollection( CollID )
if MatchIDs and Attr_Cut_Check:
    print("Successfully cut Attribute")
else:
    print("CutAttribute Error!")
```

  


### function PasteAttribute

```
vector< string > PasteAttribute(
    const string & coll_id
)
```


**Parameters**: 

  * **coll_id** string ID of destination for pasting attribute into 


Paste the attribute clipboard to the specified objectID ObjectID can be any OpenVSP entity that contains a AttributeCollection or simply the attributeCollectionID Returns a vector of pasted attributes IDs, if any 

//==== Attribute: PasteAttribute  =====//

string VehID = GetVehicleID();
string CollID = GetChildCollection( VehID );
string AttrName = "Example_String_Attr";
string StringValue = "Example_String_Attr_DataVal";
string AttrID = AddAttributeString( CollID, AttrName, StringValue );
CutAttribute( AttrID );

string NewCollID = GetChildCollection( "_AttrWMGroup" );
array < string > @NewAttrIDs = PasteAttribute( NewCollID );

bool MatchIDs = false;
bool AttrInOldColl = false;
bool AttrInNewColl = false;

array < string > OldCollAttrs = FindAttributesInCollection( CollID );
array < string > NewCollAttrs = FindAttributesInCollection( NewCollID );

MatchIDs = NewAttrIDs[0] == AttrID;

for ( int i = 0; i < int( OldCollAttrs.size() ); i++ )
{
    if ( AttrID == OldCollAttrs[i] )
    {
        AttrInOldColl = true;
    }
}

for ( int i = 0; i < int( NewCollAttrs.size() ); i++ )
{
    if ( AttrID == NewCollAttrs[i] )
    {
        AttrInNewColl = true;
    }
}

if ( MatchIDs and !AttrInOldColl and AttrInNewColl )
{
    Print("Successfully pasted Attribute");
}
else
{
    Print("PasteAttribute Error!");
    __failure++;
}
```

 \endforcpponly \beginPythonOnly ```py



VehID = GetVehicleID()
CollID = GetChildCollection( VehID )
AttrName = 'Example_String_Attr'
StringValue = 'Example_String_Attr_DataVal'
AttrID = AddAttributeString( CollID, AttrName, StringValue )
CutAttribute( AttrID )

NewCollID = GetChildCollection( "_AttrWMGroup" )
NewAttrIDs = PasteAttribute( NewCollID )

MatchIDs = NewAttrIDs[0] == AttrID
Attr_Cut_Check = AttrID not in FindAttributesInCollection( CollID )
Attr_Paste_Check = AttrID in FindAttributesInCollection( NewCollID )
if MatchIDs and Attr_Cut_Check and Attr_Paste_Check:
    print("Successfully pasted Attribute")
else:
    print("PasteAttribute Error!")
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800