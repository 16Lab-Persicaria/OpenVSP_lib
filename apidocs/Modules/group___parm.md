---
title: Parm Functions
summary: Every Parm in OpenVSP can be accessed and modified through the functions defined in this API group. Every Parm has an associated ParmContainer. Click here to return to the main page. 

---

# Parm Functions

Every Parm in OpenVSP can be accessed and modified through the functions defined in this API group. Every Parm has an associated ParmContainer. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::string | **[GetParm](Modules/group___parm.md#function-getparm)**(const std::string & geom_id, const std::string & name, const std::string & group) |
| bool | **[ValidParm](Modules/group___parm.md#function-validparm)**(const std::string & id) |
| double | **[SetParmVal](Modules/group___parm.md#function-setparmval)**(const std::string & parm_id, double val) |
| double | **[SetParmVal](Modules/group___parm.md#function-setparmval)**(const std::string & geom_id, const std::string & name, const std::string & group, double val) |
| double | **[SetParmValLimits](Modules/group___parm.md#function-setparmvallimits)**(const std::string & parm_id, double val, double lower_limit, double upper_limit) |
| double | **[SetParmValUpdate](Modules/group___parm.md#function-setparmvalupdate)**(const std::string & parm_id, double val) |
| double | **[SetParmValUpdate](Modules/group___parm.md#function-setparmvalupdate)**(const std::string & geom_id, const std::string & parm_name, const std::string & parm_group_name, double val) |
| double | **[GetParmVal](Modules/group___parm.md#function-getparmval)**(const std::string & parm_id) |
| double | **[GetParmVal](Modules/group___parm.md#function-getparmval)**(const std::string & geom_id, const std::string & name, const std::string & group) |
| int | **[GetIntParmVal](Modules/group___parm.md#function-getintparmval)**(const std::string & parm_id) |
| bool | **[GetBoolParmVal](Modules/group___parm.md#function-getboolparmval)**(const std::string & parm_id) |
| void | **[SetParmUpperLimit](Modules/group___parm.md#function-setparmupperlimit)**(const std::string & parm_id, double val) |
| double | **[GetParmUpperLimit](Modules/group___parm.md#function-getparmupperlimit)**(const std::string & parm_id) |
| void | **[SetParmLowerLimit](Modules/group___parm.md#function-setparmlowerlimit)**(const std::string & parm_id, double val) |
| double | **[GetParmLowerLimit](Modules/group___parm.md#function-getparmlowerlimit)**(const std::string & parm_id) |
| int | **[GetParmType](Modules/group___parm.md#function-getparmtype)**(const std::string & parm_id) |
| std::string | **[GetParmName](Modules/group___parm.md#function-getparmname)**(const std::string & parm_id) |
| std::string | **[GetParmGroupName](Modules/group___parm.md#function-getparmgroupname)**(const std::string & parm_id) |
| std::string | **[GetParmDisplayGroupName](Modules/group___parm.md#function-getparmdisplaygroupname)**(const std::string & parm_id) |
| std::string | **[GetParmContainer](Modules/group___parm.md#function-getparmcontainer)**(const std::string & parm_id) |
| void | **[SetParmDescript](Modules/group___parm.md#function-setparmdescript)**(const std::string & parm_id, const std::string & desc) |
| std::string | **[GetParmDescript](Modules/group___parm.md#function-getparmdescript)**(const std::string & parm_id) |
| std::string | **[FindParm](Modules/group___parm.md#function-findparm)**(const std::string & parm_container_id, const std::string & parm_name, const std::string & group_name) |


## Functions Documentation

### function GetParm

```
std::string GetParm(
    const std::string & geom_id,
    const std::string & name,
    const std::string & group
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **name** string Parm name 
  * **group** string Parm group name 


**Return**: string Parm ID 

Get Parm ID 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD" );

string lenid = GetParm( pid, "Length", "Design" );

if ( !ValidParm( lenid ) )                { Print( "---> Error: API GetParm  " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD" )

lenid = GetParm( pid, "Length", "Design" )

if  not ValidParm( lenid ) : print( "---> Error: API GetParm  " )
```

  


### function ValidParm

```
bool ValidParm(
    const std::string & id
)
```


**Parameters**: 

  * **id** Parm ID 


**Return**: True if Parm ID is valid, false otherwise 

Check if given Parm is valid 

//==== Add Pod Geometry ====//
string pid = AddGeom( "POD" );

string lenid = GetParm( pid, "Length", "Design" );

if ( !ValidParm( lenid ) )                { Print( "---> Error: API GetParm  " ); }
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pid = AddGeom( "POD" )

lenid = GetParm( pid, "Length", "Design" )

if  not ValidParm( lenid ) : print( "---> Error: API GetParm  " )
```

  


### function SetParmVal

```
double SetParmVal(
    const std::string & parm_id,
    double val
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **val** Parm value to set 


**See**: [SetParmValUpdate](Modules/group___parm.md#function-setparmvalupdate)

**Return**: Value that the Parm was set to 

Set the value of the specified Parm. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

SetParmVal( wid, 23.0 );

if ( abs( GetParmVal( wid ) - 23 ) > 1e-6 )                { Print( "---> Error: API Parm Val Set/Get " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

SetParmVal( wid, 23.0 )

if  abs( GetParmVal( wid ) - 23 ) > 1e-6 : print( "---> Error: API Parm Val Set/Get " )
```

  


### function SetParmVal

```
double SetParmVal(
    const std::string & geom_id,
    const std::string & name,
    const std::string & group,
    double val
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **name** string Parm name 
  * **group** string Parm group name 
  * **val** double Parm value to set 


**See**: [SetParmValUpdate](Modules/group___parm.md#function-setparmvalupdate)

**Return**: double Value that the Parm was set to 

Set the value of the specified Parm. 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

SetParmVal( wid, 23.0 );

if ( abs( GetParmVal( wid ) - 23 ) > 1e-6 )                { Print( "---> Error: API Parm Val Set/Get " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

SetParmVal( wid, 23.0 )

if  abs( GetParmVal( wid ) - 23 ) > 1e-6 : print( "---> Error: API Parm Val Set/Get " )
```

  


### function SetParmValLimits

```
double SetParmValLimits(
    const std::string & parm_id,
    double val,
    double lower_limit,
    double upper_limit
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **val** Parm value to set 
  * **lower_limit** Parm lower limit 
  * **upper_limit** Parm upper limit 


**See**: [SetParmLowerLimit](Modules/group___parm.md#function-setparmlowerlimit), [SetParmUpperLimit](Modules/group___parm.md#function-setparmupperlimit)

**Return**: Value that the Parm was set to 

Set the value along with the upper and lower limits of the specified Parm 

string pod_id = AddGeom( "POD" );

string length = FindParm( pod_id, "Length", "Design" );

SetParmValLimits( length, 10.0, 0.001, 1.0e12 );

SetParmDescript( length, "Total Length of Geom" );
```

 \endforcpponly \beginPythonOnly ```py

pod_id = AddGeom( "POD" )

length = FindParm( pod_id, "Length", "Design" )

SetParmValLimits( length, 10.0, 0.001, 1.0e12 )

SetParmDescript( length, "Total Length of Geom" )
```

  


### function SetParmValUpdate

```
double SetParmValUpdate(
    const std::string & parm_id,
    double val
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **val** Parm value to set 


**See**: [SetParmVal](Modules/group___parm.md#function-setparmval)

**Return**: Value that the Parm was set to 

Set the value of the specified Parm and force an Update. 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

string parm_id = GetParm( pod_id, "X_Rel_Location", "XForm" );

SetParmValUpdate( parm_id, 5.0 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

parm_id = GetParm( pod_id, "X_Rel_Location", "XForm" )

SetParmValUpdate( parm_id, 5.0 )
```

  


### function SetParmValUpdate

```
double SetParmValUpdate(
    const std::string & geom_id,
    const std::string & parm_name,
    const std::string & parm_group_name,
    double val
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **parm_name** string Parm name 
  * **parm_group_name** string Parm group name 
  * **val** double Parm value to set 


**See**: [SetParmVal](Modules/group___parm.md#function-setparmval)

**Return**: double Value that the Parm was set to 

Set the value of the specified Parm and force an Update. 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

string parm_id = GetParm( pod_id, "X_Rel_Location", "XForm" );

SetParmValUpdate( parm_id, 5.0 );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

parm_id = GetParm( pod_id, "X_Rel_Location", "XForm" )

SetParmValUpdate( parm_id, 5.0 )
```

  


### function GetParmVal

```
double GetParmVal(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: Parm value 

Get the value of the specified Parm. The data type of the Parm value will be cast to a double 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

SetParmVal( wid, 23.0 );

if ( abs( GetParmVal( wid ) - 23 ) > 1e-6 )                { Print( "---> Error: API Parm Val Set/Get " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

SetParmVal( wid, 23.0 )

if  abs( GetParmVal( wid ) - 23 ) > 1e-6 : print( "---> Error: API Parm Val Set/Get " )
```

  


### function GetParmVal

```
double GetParmVal(
    const std::string & geom_id,
    const std::string & name,
    const std::string & group
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **name** string Parm name 
  * **group** string Parm group name 


**Return**: double Parm value 

Get the value of the specified Parm. The data type of the Parm value will be cast to a double 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

SetParmVal( wid, 23.0 );

if ( abs( GetParmVal( wid ) - 23 ) > 1e-6 )                { Print( "---> Error: API Parm Val Set/Get " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

SetParmVal( wid, 23.0 )

if  abs( GetParmVal( wid ) - 23 ) > 1e-6 : print( "---> Error: API Parm Val Set/Get " )
```

  


### function GetIntParmVal

```
int GetIntParmVal(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: double Parm value 

Get the value of the specified int type Parm 

//==== Add Prop Geometry ====//
string prop_id = AddGeom( "PROP" );

string num_blade_id = GetParm( prop_id, "NumBlade", "Design" );

int num_blade = GetIntParmVal( num_blade_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Prop Geometry ====//
prop_id = AddGeom( "PROP" )

num_blade_id = GetParm( prop_id, "NumBlade", "Design" )

num_blade = GetIntParmVal( num_blade_id )
```

  


### function GetBoolParmVal

```
bool GetBoolParmVal(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: bool Parm value 

Get the value of the specified bool type Parm 

//==== Add Prop Geometry ====//
string prop_id = AddGeom( "PROP" );

string rev_flag_id = GetParm( prop_id, "ReverseFlag", "Design" );

bool reverse_flag = GetBoolParmVal( rev_flag_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Prop Geometry ====//
prop_id = AddGeom( "PROP" )

rev_flag_id = GetParm( prop_id, "ReverseFlag", "Design" )

reverse_flag = GetBoolParmVal( rev_flag_id )
```

  


### function SetParmUpperLimit

```
void SetParmUpperLimit(
    const std::string & parm_id,
    double val
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **val** double Parm upper limit 


**See**: [SetParmValLimits](Modules/group___parm.md#function-setparmvallimits)

Set the upper limit value for the specified Parm 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

SetParmVal( wid, 23.0 );

SetParmUpperLimit( wid, 13.0 );

if ( abs( GetParmVal( wid ) - 13 ) > 1e-6 )                { Print( "---> Error: API SetParmUpperLimit " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

SetParmVal( wid, 23.0 )

SetParmUpperLimit( wid, 13.0 )

if  abs( GetParmVal( wid ) - 13 ) > 1e-6 : print( "---> Error: API SetParmUpperLimit " )
```

  


### function GetParmUpperLimit

```
double GetParmUpperLimit(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: double Parm upper limit 

Get the upper limit value for the specified Parm 

//==== Add Prop Geometry ====//
string prop_id = AddGeom( "PROP" );

string num_blade_id = GetParm( prop_id, "NumBlade", "Design" );

double max_blade = GetParmUpperLimit( num_blade_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Prop Geometry ====//
prop_id = AddGeom( "PROP" )

num_blade_id = GetParm( prop_id, "NumBlade", "Design" )

max_blade = GetParmUpperLimit( num_blade_id )
```

  


### function SetParmLowerLimit

```
void SetParmLowerLimit(
    const std::string & parm_id,
    double val
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **val** Parm lower limit 


**See**: [SetParmValLimits](Modules/group___parm.md#function-setparmvallimits)

Set the lower limit value for the specified Parm 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

SetParmVal( wid, 13.0 );

SetParmLowerLimit( wid, 15.0 );

if ( abs( GetParmVal( wid ) - 15 ) > 1e-6 )                { Print( "---> Error: API SetParmLowerLimit " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

SetParmVal( wid, 13.0 )

SetParmLowerLimit( wid, 15.0 )

if  abs( GetParmVal( wid ) - 15 ) > 1e-6 : print( "---> Error: API SetParmLowerLimit " )
```

  


### function GetParmLowerLimit

```
double GetParmLowerLimit(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: Parm lower limit 

Get the lower limit value for the specified Parm 

//==== Add Prop Geometry ====//
string prop_id = AddGeom( "PROP" );

string num_blade_id = GetParm( prop_id, "NumBlade", "Design" );

double min_blade = GetParmLowerLimit( num_blade_id );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Prop Geometry ====//
prop_id = AddGeom( "PROP" )

num_blade_id = GetParm( prop_id, "NumBlade", "Design" )

min_blade = GetParmLowerLimit( num_blade_id )
```

  


### function GetParmType

```
int GetParmType(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**See**: [PARM_TYPE](Modules/group___enumerations.md#enum-parm-type)

**Return**: Parm data type enum (i.e. PARM_BOOL_TYPE) 

Get the data type for the specified Parm 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

if ( GetParmType( wid ) != PARM_DOUBLE_TYPE )        { Print( "---> Error: API GetParmType " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

if  GetParmType( wid ) != PARM_DOUBLE_TYPE : print( "---> Error: API GetParmType " )
```

  


### function GetParmName

```
std::string GetParmName(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: Parm name 

Get the name for the specified Parm 

//==== Add Pod Geometry ====//
string pod_id = AddGeom( "POD" );

//==== Add FeaStructure to Pod ====//
int struct_ind = AddFeaStruct( pod_id );

//==== Get Structure Name and Parm Container ID ====//
string parm_container_name = GetFeaStructName( pod_id, struct_ind );

string parm_container_id = FindContainer( parm_container_name, struct_ind );

//==== Get and List All Parms in the Container ====//
array<string> parm_ids = FindContainerParmIDs( parm_container_id );

for ( uint i = 0; i < uint(parm_ids.length()); i++ )
{
    string name_id = GetParmName( parm_ids[i] ) + string(": ") + parm_ids[i] + string("\n");

    Print( name_id );
}
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Pod Geometry ====//
pod_id = AddGeom( "POD" )

#==== Add FeaStructure to Pod ====//
struct_ind = AddFeaStruct( pod_id )

#==== Get Structure Name and Parm Container ID ====//
parm_container_name = GetFeaStructName( pod_id, struct_ind )

parm_container_id = FindContainer( parm_container_name, struct_ind )

#==== Get and List All Parms in the Container ====//
parm_ids = FindContainerParmIDs( parm_container_id )

for i in range(len(parm_ids)):

    name_id = GetParmName( parm_ids[i] ) + ": " + parm_ids[i] + "\n"

    print( name_id )
```

  


### function GetParmGroupName

```
std::string GetParmGroupName(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: Parm group name 

Get the group name for the specified Parm 

string veh_id = FindContainer( "Vehicle", 0 );

//==== Get and List All Parms in the Container ====//
array<string> parm_ids = FindContainerParmIDs( veh_id );

Print( "Parm Groups and IDs in Vehicle Parm Container: " );

for ( uint i = 0; i < uint(parm_ids.length()); i++ )
{
    string group_str = GetParmGroupName( parm_ids[i] ) + string(": ") + parm_ids[i] + string("\n");

    Print( group_str );
}
```

 \endforcpponly \beginPythonOnly ```py

veh_id = FindContainer( "Vehicle", 0 )

#==== Get and List All Parms in the Container ====//
parm_ids = FindContainerParmIDs( veh_id )

print( "Parm Groups and IDs in Vehicle Parm Container: " )

for i in range(len(parm_ids)):

    group_str = GetParmGroupName( parm_ids[i] ) + ": " + parm_ids[i] + "\n"

    print( group_str )
```

  


### function GetParmDisplayGroupName

```
std::string GetParmDisplayGroupName(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: Parm display group name 

Get the display group name for the specified Parm 

string veh_id = FindContainer( "Vehicle", 0 );

//==== Get and List All Parms in the Container ====//
array<string> parm_ids = FindContainerParmIDs( veh_id );

Print( "Parm Group Display Names and IDs in Vehicle Parm Container: " );

for ( uint i = 0; i < uint(parm_ids.length()); i++ )
{
    string group_str = GetParmDisplayGroupName( parm_ids[i] ) + string(": ") + parm_ids[i] + string("\n");

    Print( group_str );
}
```

 \endforcpponly \beginPythonOnly ```py

veh_id = FindContainer( "Vehicle", 0 )

#==== Get and List All Parms in the Container ====//
parm_ids = FindContainerParmIDs( veh_id )

print( "Parm Group Display Names and IDs in Vehicle Parm Container: " )

for i in range(len(parm_ids)):

    group_str = GetParmDisplayGroupName( parm_ids[i] ) + ": " + parm_ids[i] + "\n"

    print( group_str )
```

  


### function GetParmContainer

```
std::string GetParmContainer(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: Parm Container ID 

Get Parm Container ID for the specified Parm 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE", "" );

string xsec_surf = GetXSecSurf( fuseid, 0 );

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE );

string xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 );

string wid = GetXSecParm( xsec, "RoundedRect_Width" );

string cid = GetParmContainer( wid );

if ( cid.size() == 0 )                                { Print( "---> Error: API GetParmContainer " ); }
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE", "" )

xsec_surf = GetXSecSurf( fuseid, 0 )

ChangeXSecShape( xsec_surf, GetNumXSec( xsec_surf ) - 1, XS_ROUNDED_RECTANGLE )

xsec = GetXSec( xsec_surf, GetNumXSec( xsec_surf ) - 1 )

wid = GetXSecParm( xsec, "RoundedRect_Width" )

cid = GetParmContainer( wid )

if  len(cid) == 0 : print( "---> Error: API GetParmContainer " )
```

  


### function SetParmDescript

```
void SetParmDescript(
    const std::string & parm_id,
    const std::string & desc
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **desc** Parm description 


Set the description of the specified Parm 

string pod_id = AddGeom( "POD" );

string length = FindParm( pod_id, "Length", "Design" );

SetParmValLimits( length, 10.0, 0.001, 1.0e12 );

SetParmDescript( length, "Total Length of Geom" );
```

 \endforcpponly \beginPythonOnly ```py

pod_id = AddGeom( "POD" )

length = FindParm( pod_id, "Length", "Design" )

SetParmValLimits( length, 10.0, 0.001, 1.0e12 )

SetParmDescript( length, "Total Length of Geom" )
```

  


### function GetParmDescript

```
std::string GetParmDescript(
    const std::string & parm_id
)
```


**Parameters**: 

  * **parm_id** string Parm ID 


**Return**: desc Parm description 

Get the description of the specified Parm 

string pod_id = AddGeom( "POD" );

string length = FindParm( pod_id, "Length", "Design" );

SetParmValLimits( length, 10.0, 0.001, 1.0e12 );

string desc = GetParmDescript( length );
Print( desc );
```

 \endforcpponly \beginPythonOnly ```py

pod_id = AddGeom( "POD" )

length = FindParm( pod_id, "Length", "Design" )

SetParmValLimits( length, 10.0, 0.001, 1.0e12 )

desc = GetParmDescript( length )
print( desc )
```

  


### function FindParm

```
std::string FindParm(
    const std::string & parm_container_id,
    const std::string & parm_name,
    const std::string & group_name
)
```


**Parameters**: 

  * **parm_container_id** Parm Container ID 
  * **parm_name** Parm name 
  * **group_name** Parm group name 


**Return**: Parm ID 

Find a Parm ID given the Parm Container ID, Parm name, and Parm group 

//==== Add Wing Geometry ====//
string wing_id = AddGeom( "WING" );

//==== Turn Symmetry OFF ====//
string sym_id = FindParm( wing_id, "Sym_Planar_Flag", "Sym");

SetParmVal( sym_id, 0.0 ); // Note: bool input not supported in SetParmVal
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geometry ====//
wing_id = AddGeom( "WING" )

#==== Turn Symmetry OFF ====//
sym_id = FindParm( wing_id, "Sym_Planar_Flag", "Sym")

SetParmVal( sym_id, 0.0 ) # Note: bool input not supported in SetParmVal
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800