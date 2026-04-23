---
title: Parm Container Functions
summary: All Parms in OpenVSP are stored in Parm Containers. The functions in this group can be used to work with Parm Containers through the API. Click here to return to the main page. 

---

# Parm Container Functions

All Parms in OpenVSP are stored in Parm Containers. The functions in this group can be used to work with Parm Containers through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::vector< std::string > | **[FindContainers](Modules/group___parm_container.md#function-findcontainers)**() |
| std::vector< std::string > | **[FindContainersWithName](Modules/group___parm_container.md#function-findcontainerswithname)**(const std::string & name) |
| std::string | **[FindContainer](Modules/group___parm_container.md#function-findcontainer)**(const std::string & name, int index) |
| std::string | **[GetContainerName](Modules/group___parm_container.md#function-getcontainername)**(const std::string & parm_container_id) |
| std::vector< std::string > | **[FindContainerGroupNames](Modules/group___parm_container.md#function-findcontainergroupnames)**(const std::string & parm_container_id) |
| std::vector< std::string > | **[FindContainerParmIDs](Modules/group___parm_container.md#function-findcontainerparmids)**(const std::string & parm_container_id) |
| std::string | **[GetVehicleID](Modules/group___parm_container.md#function-getvehicleid)**() |
| int | **[GetNumUserParms](Modules/group___parm_container.md#function-getnumuserparms)**() |
| int | **[GetNumPredefinedUserParms](Modules/group___parm_container.md#function-getnumpredefineduserparms)**() |
| std::vector< std::string > | **[GetAllUserParms](Modules/group___parm_container.md#function-getalluserparms)**() |
| std::string | **[GetUserParmContainer](Modules/group___parm_container.md#function-getuserparmcontainer)**() |
| string | **[AddUserParm](Modules/group___parm_container.md#function-adduserparm)**(int type, const string & name, const string & group) |
| void | **[DeleteUserParm](Modules/group___parm_container.md#function-deleteuserparm)**(const std::string & id) |
| void | **[DeleteAllUserParm](Modules/group___parm_container.md#function-deletealluserparm)**() |


## Functions Documentation

### function FindContainers

```
std::vector< std::string > FindContainers()
```


**Return**: Array of Parm Container IDs 

Get an array of all Parm Container IDs 

array<string> @ctr_arr = FindContainers();

Print( "---> API Parm Container IDs: " );

for ( int i = 0; i < int( ctr_arr.size() ); i++ )
{
    string message = "\t" + ctr_arr[i] + "\n";

    Print( message );
}
```

 

ctr_arr = FindContainers()

print( "---> API Parm Container IDs: " )

for i in range(int( len(ctr_arr) )):

    message = "\t" + ctr_arr[i] + "\n"

    print( message )
```

  


### function FindContainersWithName

```
std::vector< std::string > FindContainersWithName(
    const std::string & name
)
```


**Parameters**: 

  * **name** Parm Container name 


**Return**: Array of Parm Container IDs 

Get an array of Parm Container IDs for Containers with the specified name 

array<string> @ctr_arr = FindContainersWithName( "UserParms" );

if ( ctr_arr.size() > 0 )            { Print( ( "UserParms Parm Container ID: " + ctr_arr[0] ) ); }
```

 

ctr_arr = FindContainersWithName( "UserParms" )

if  len(ctr_arr) > 0 : print( ( "UserParms Parm Container ID: " + ctr_arr[0] ) )
```

  


### function FindContainer

```
std::string FindContainer(
    const std::string & name,
    int index
)
```


**Parameters**: 

  * **name** Parm Container name 
  * **index** Parm Container index 


**See**: [FindContainersWithName](Modules/group___parm_container.md#function-findcontainerswithname)

**Return**: Parm Container ID 

Get the ID of a Parm Container with specified name at input index 

//===== Get Vehicle Parm Container ID ====//
string veh_id = FindContainer( "Vehicle", 0 );
```

 

#===== Get Vehicle Parm Container ID ====//
veh_id = FindContainer( "Vehicle", 0 )
```

  


### function GetContainerName

```
std::string GetContainerName(
    const std::string & parm_container_id
)
```


**Parameters**: 

  * **parm_container_id** Parm Container ID 


**Return**: Parm Container name 

Get the name of the specified Parm Container 

string veh_id = FindContainer( "Vehicle", 0 );

if ( GetContainerName( veh_id ) != "Vehicle" )         { Print( "---> Error: API GetContainerName" ); }
```

 

veh_id = FindContainer( "Vehicle", 0 )

if  GetContainerName( veh_id) != "Vehicle":       print( "---> Error: API GetContainerName" )
```

  


### function FindContainerGroupNames

```
std::vector< std::string > FindContainerGroupNames(
    const std::string & parm_container_id
)
```


**Parameters**: 

  * **parm_container_id** Parm Container ID 


**Return**: Array of Parm group names 

Get an array of Parm group names included in the specified Container 

string user_ctr = FindContainer( "UserParms", 0 );

array<string> @grp_arr = FindContainerGroupNames( user_ctr );

Print( "---> UserParms Container Group IDs: " );
for ( int i = 0; i < int( grp_arr.size() ); i++ )
{
    string message = "\t" + grp_arr[i] + "\n";

    Print( message );
}
```

 

user_ctr = FindContainer( "UserParms", 0 )

grp_arr = FindContainerGroupNames( user_ctr )

print( "---> UserParms Container Group IDs: " )
for i in range(int( len(grp_arr) )):

    message = "\t" + grp_arr[i] + "\n"

    print( message )
```

  


### function FindContainerParmIDs

```
std::vector< std::string > FindContainerParmIDs(
    const std::string & parm_container_id
)
```


**Parameters**: 

  * **parm_container_id** Parm Container ID 


**Return**: Array of Parm IDs 

Get an array of Parm IDs included in the specified Container 

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

  


### function GetVehicleID

```
std::string GetVehicleID()
```


**Return**: Vehicle ID 

Get the ID of the Vehicle Parm Container 

//===== Get Vehicle Parm Container ID ====//
string veh_id = GetVehicleID();
```

 

#===== Get Vehicle Parm Container ID ====//
veh_id = GetVehicleID()
```

  


### function GetNumUserParms

```
int GetNumUserParms()
```


**Return**: Number of user Parms 

Get the number of user parameters 

int n = GetNumUserParms();
```

 

n = GetNumUserParms()
```

  


### function GetNumPredefinedUserParms

```
int GetNumPredefinedUserParms()
```


**Return**: Number of pre-defined user Parms 

Get the number of pre-defined user parameters 

int n = GetNumPredefinedUserParms();
```

 

n = GetNumPredefinedUserParms()
```

  


### function GetAllUserParms

```
std::vector< std::string > GetAllUserParms()
```


**Return**: Array of user parameter ids 

Get the vector of id's for all user parameters 

array<string> @id_arr = GetAllUserParms();

Print( "---> User Parm IDs: " );

for ( int i = 0; i < int( id_arr.size() ); i++ )
{
    string message = "\t" + id_arr[i] + "\n";

    Print( message );
}
```

 

id_arr = GetAllUserParms()

print( "---> User Parm IDs: " )

for i in range(int( len(id_arr) )):

    message = "\t" + id_arr[i] + "\n"

    print( message )
```

  


### function GetUserParmContainer

```
std::string GetUserParmContainer()
```


**Return**: User parm container ID 

Get the user parm container ID 

string up_id = GetUserParmContainer();
```

 

up_id = GetUserParmContainer()
```

  


### function AddUserParm

```
string AddUserParm(
    int type,
    const string & name,
    const string & group
)
```


**Parameters**: 

  * **type** Parm type enum (i.e. PARM_DOUBLE_TYPE) 
  * **name** Parm name 
  * **group** Parm group 


**See**: [PARM_TYPE](Modules/group___enumerations.md#enum-parm-type)

**Return**: Parm ID 

Function to add a new user Parm of input type, name, and group 

string length = AddUserParm( PARM_DOUBLE_TYPE, "Length", "Design" );

SetParmValLimits( length, 10.0, 0.001, 1.0e12 );

SetParmDescript( length, "Length user parameter" );
```

 

length = AddUserParm( PARM_DOUBLE_TYPE, "Length", "Design" )

SetParmValLimits( length, 10.0, 0.001, 1.0e12 )

SetParmDescript( length, "Length user parameter" )
```

  


### function DeleteUserParm

```
void DeleteUserParm(
    const std::string & id
)
```


Get the user parm container ID 

int n = GetNumPredefinedUserParms();
array<string> @id_arr = GetAllUserParms();

if ( int( id_arr.size() ) > n )
{
    DeleteUserParm( id_arr[n] );
}
```

 

n = GetNumPredefinedUserParms()
id_arr = GetAllUserParms()

if  len(id_arr) > n :
    DeleteUserParm( id_arr[n] )
```

  


### function DeleteAllUserParm

```
void DeleteAllUserParm()
```


Get the user parm container ID 

DeleteAllUserParm();
```

 

DeleteAllUserParm()
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800