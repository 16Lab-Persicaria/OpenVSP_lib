---
title: VSPAERO Actuator Disk and Propeller Functions
summary: The following group of functions provide API capability for setting up actuator disks (Disk tab of VSPAERO GUI) and propellers (Propeller tab of VSPAERO GUI) for VSPAERO analysis. If a propeller geometry is used to model the actuator disk, the "PropMode" must be set to PROP_DISK or PROP_BOTH. Alternatively, the "PropMode" but be set to PROP_BLADE or PROP_BOTH for unsteady analysis. must be set to PROP_DISK or PROP_BOTH. Click here to return to the main page. 

---

# VSPAERO Actuator Disk and Propeller Functions

The following group of functions provide API capability for setting up actuator disks (Disk tab of VSPAERO GUI) and propellers (Propeller tab of VSPAERO GUI) for VSPAERO analysis. If a propeller geometry is used to model the actuator disk, the "PropMode" must be set to PROP_DISK or PROP_BOTH. Alternatively, the "PropMode" but be set to PROP_BLADE or PROP_BOTH for unsteady analysis. must be set to PROP_DISK or PROP_BOTH. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::string | **[FindActuatorDisk](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-findactuatordisk)**(int disk_index) |
| int | **[GetNumActuatorDisks](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getnumactuatordisks)**() |
| std::string | **[FindUnsteadyGroup](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-findunsteadygroup)**(int group_index) |
| std::string | **[GetUnsteadyGroupName](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getunsteadygroupname)**(int group_index) |
| std::vector< std::string > | **[GetUnsteadyGroupCompIDs](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getunsteadygroupcompids)**(int group_index) |
| std::vector< int > | **[GetUnsteadyGroupSurfIndexes](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getunsteadygroupsurfindexes)**(int group_index) |
| int | **[GetNumUnsteadyGroups](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getnumunsteadygroups)**() |
| int | **[GetNumUnsteadyRotorGroups](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getnumunsteadyrotorgroups)**() |


## Functions Documentation

### function FindActuatorDisk

```
std::string FindActuatorDisk(
    int disk_index
)
```


**Parameters**: 

  * **disk_index** Actuator disk index for the current VSPAERO set 


**See**: [PROP_MODE](Modules/group___enumerations.md#enum-prop-mode)

**Return**: Actuator disk ID 

Get the ID of a VSPAERO actuator disk at the specified index. An empty string is returned if the index is out of range. 

// Add a propeller
string prop_id = AddGeom( "PROP", "" );
SetParmVal( prop_id, "PropMode", "Design", PROP_DISK );
SetParmVal( prop_id, "Diameter", "Design", 6.0 );

Update();

// Setup the actuator disk VSPAERO parms
string disk_id = FindActuatorDisk( 0 );

SetParmVal( FindParm( disk_id, "RotorRPM", "Rotor" ), 1234.0 );
SetParmVal( FindParm( disk_id, "RotorCT", "Rotor" ), 0.35 );
SetParmVal( FindParm( disk_id, "RotorCP", "Rotor" ), 0.55 );
SetParmVal( FindParm( disk_id, "RotorHubDiameter", "Rotor" ), 1.0 );
```

 \endforcpponly \beginPythonOnly ```py

# Add a propeller
prop_id = AddGeom( "PROP", "" )
SetParmVal( prop_id, "PropMode", "Design", PROP_DISK )
SetParmVal( prop_id, "Diameter", "Design", 6.0 )

Update()

# Setup the actuator disk VSPAERO parms
disk_id = FindActuatorDisk( 0 )

SetParmVal( FindParm( disk_id, "RotorRPM", "Rotor" ), 1234.0 )
SetParmVal( FindParm( disk_id, "RotorCT", "Rotor" ), 0.35 )
SetParmVal( FindParm( disk_id, "RotorCP", "Rotor" ), 0.55 )
SetParmVal( FindParm( disk_id, "RotorHubDiameter", "Rotor" ), 1.0 )
```

  


### function GetNumActuatorDisks

```
int GetNumActuatorDisks()
```


**See**: [PROP_MODE](Modules/group___enumerations.md#enum-prop-mode)

**Return**: Number of actuator disks in the current VSPAERO set 

Get the number of actuator disks in the current VSPAERO set. This is equivalent to the number of disk surfaces in the VSPAERO set. 

// Set VSPAERO set index to SET_ALL
SetParmVal( FindParm( FindContainer( "VSPAEROSettings", 0 ), "GeomSet", "VSPAERO" ), SET_ALL );

// Add a propeller
string prop_id = AddGeom( "PROP", "" );
SetParmValUpdate( prop_id, "PropMode", "Design", PROP_BLADES );

int num_disk = GetNumActuatorDisks(); // Should be 0

SetParmValUpdate( prop_id, "PropMode", "Design", PROP_DISK );

num_disk = GetNumActuatorDisks(); // Should be 1
```

 \endforcpponly \beginPythonOnly ```py

# Set VSPAERO set index to SET_ALL
SetParmVal( FindParm( FindContainer( "VSPAEROSettings", 0 ), "GeomSet", "VSPAERO" ), SET_ALL )

# Add a propeller
prop_id = AddGeom( "PROP", "" )
SetParmValUpdate( prop_id, "PropMode", "Design", PROP_BLADES )

num_disk = GetNumActuatorDisks() # Should be 0

SetParmValUpdate( prop_id, "PropMode", "Design", PROP_DISK )

num_disk = GetNumActuatorDisks() # Should be 1
```

  


### function FindUnsteadyGroup

```
std::string FindUnsteadyGroup(
    int group_index
)
```


**Parameters**: 

  * **group_index** Unsteady group index for the current VSPAERO set 


**See**: [PROP_MODE](Modules/group___enumerations.md#enum-prop-mode)

**Return**: Unsteady group ID 

Get the ID of the VSPAERO unsteady group at the specified index. An empty string is returned if the index is out of range. 

string wing_id = AddGeom( "WING" );
string pod_id = AddGeom( "POD" );

// Create an actuator disk
string prop_id = AddGeom( "PROP", "" );
SetParmVal( prop_id, "PropMode", "Design", PROP_BLADES );

Update();

// Setup the unsteady group VSPAERO parms
string disk_id = FindUnsteadyGroup( 1 ); // fixed components are in group 0 (wing & pod)

SetParmVal( FindParm( disk_id, "RPM", "UnsteadyGroup" ), 1234.0 );
```

 \endforcpponly \beginPythonOnly ```py

wing_id = AddGeom( "WING" )
pod_id = AddGeom( "POD" )

# Create an actuator disk
prop_id = AddGeom( "PROP", "" )
SetParmVal( prop_id, "PropMode", "Design", PROP_BLADES )

Update()

# Setup the unsteady group VSPAERO parms
disk_id = FindUnsteadyGroup( 1 ) # fixed components are in group 0 (wing & pod)

SetParmVal( FindParm( disk_id, "RPM", "UnsteadyGroup" ), 1234.0 )
```

  


### function GetUnsteadyGroupName

```
std::string GetUnsteadyGroupName(
    int group_index
)
```


**Parameters**: 

  * **group_index** Unsteady group index for the current VSPAERO set 


**See**: SetUnsteadyGroupName 

**Return**: Unsteady group name 

Get the name of the unsteady group at the specified index. 

// Add a pod and wing
string pod_id = AddGeom( "POD", "" );
string wing_id = AddGeom( "WING", pod_id );

SetParmVal( wing_id, "X_Rel_Location", "XForm", 2.5 );
Update();

Print( GetUnsteadyGroupName( 0 ) );
```

 \endforcpponly \beginPythonOnly ```py

# Add a pod and wing
pod_id = AddGeom( "POD", "" )
wing_id = AddGeom( "WING", pod_id )

SetParmVal( wing_id, "X_Rel_Location", "XForm", 2.5 )
Update()

print( GetUnsteadyGroupName( 0 ) )
```

  


### function GetUnsteadyGroupCompIDs

```
std::vector< std::string > GetUnsteadyGroupCompIDs(
    int group_index
)
```


**Parameters**: 

  * **group_index** Unsteady group index for the current VSPAERO set 


**See**: [GetUnsteadyGroupSurfIndexes](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getunsteadygroupsurfindexes)

**Return**: Array of component IDs 

Get an array of IDs for all components in the unsteady group at the specified index. 

// Add a pod and wing
string pod_id = AddGeom( "POD", "" );
string wing_id = AddGeom( "WING", pod_id ); // Default with symmetry on -> 2 surfaces

SetParmVal( wing_id, "X_Rel_Location", "XForm", 2.5 );
Update();

array < string > comp_ids = GetUnsteadyGroupCompIDs( 0 );

if ( comp_ids.size() != 3 )
{
    Print( "ERROR: GetUnsteadyGroupCompIDs" );
}
```

 \endforcpponly \beginPythonOnly ```py

# Add a pod and wing
pod_id = AddGeom( "POD", "" )
wing_id = AddGeom( "WING", pod_id ) # Default with symmetry on -> 2 surfaces

SetParmVal( wing_id, "X_Rel_Location", "XForm", 2.5 )
Update()

comp_ids = GetUnsteadyGroupCompIDs( 0 )

if  len(comp_ids) != 3 :
    print( "ERROR: GetUnsteadyGroupCompIDs" )
```

  


### function GetUnsteadyGroupSurfIndexes

```
std::vector< int > GetUnsteadyGroupSurfIndexes(
    int group_index
)
```


**Parameters**: 

  * **group_index** Unsteady group index for the current VSPAERO set 


**See**: [GetUnsteadyGroupCompIDs](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getunsteadygroupcompids)

**Return**: Array of surface indexes 

Get an array of surface indexes for all components in the unsteady group at the specified index. 

// Add a pod and wing
string pod_id = AddGeom( "POD", "" );
string wing_id = AddGeom( "WING", pod_id ); // Default with symmetry on -> 2 surfaces

SetParmVal( wing_id, "X_Rel_Location", "XForm", 2.5 );
Update();

array < int > surf_indexes = GetUnsteadyGroupSurfIndexes( 0 );

if ( surf_indexes.size() != 3 )
{
    Print( "ERROR: GetUnsteadyGroupSurfIndexes" );
}
```

 \endforcpponly \beginPythonOnly ```py

# Add a pod and wing
pod_id = AddGeom( "POD", "" )
wing_id = AddGeom( "WING", pod_id ) # Default with symmetry on -> 2 surfaces

SetParmVal( wing_id, "X_Rel_Location", "XForm", 2.5 )
Update()

surf_indexes = GetUnsteadyGroupSurfIndexes( 0 )

if  len(surf_indexes) != 3 :
    print( "ERROR: GetUnsteadyGroupSurfIndexes" )
```

  


### function GetNumUnsteadyGroups

```
int GetNumUnsteadyGroups()
```


**See**: [PROP_MODE](Modules/group___enumerations.md#enum-prop-mode), [GetNumUnsteadyRotorGroups](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getnumunsteadyrotorgroups)

**Return**: Number of unsteady groups in the current VSPAERO set 

Get the number of unsteady groups in the current VSPAERO set. Each propeller is placed in its own unsteady group. All symmetric copies of propellers are also placed in an unsteady group. All other component types are placed in a single fixed component unsteady group. 

// Set VSPAERO set index to SET_ALL
SetParmVal( FindParm( FindContainer( "VSPAEROSettings", 0 ), "GeomSet", "VSPAERO" ), SET_ALL );

// Add a propeller
string prop_id = AddGeom( "PROP" );
SetParmValUpdate( prop_id, "PropMode", "Design", PROP_DISK );

int num_group = GetNumUnsteadyGroups(); // Should be 0

SetParmValUpdate( prop_id, "PropMode", "Design", PROP_BLADES );

num_group = GetNumUnsteadyGroups(); // Should be 1

string wing_id = AddGeom( "WING" );

num_group = GetNumUnsteadyGroups(); // Should be 2 (includes fixed component group)
```

 \endforcpponly \beginPythonOnly ```py

# Set VSPAERO set index to SET_ALL
SetParmVal( FindParm( FindContainer( "VSPAEROSettings", 0 ), "GeomSet", "VSPAERO" ), SET_ALL )

# Add a propeller
prop_id = AddGeom( "PROP" )
SetParmValUpdate( prop_id, "PropMode", "Design", PROP_DISK )

num_group = GetNumUnsteadyGroups() # Should be 0

SetParmValUpdate( prop_id, "PropMode", "Design", PROP_BLADES )

num_group = GetNumUnsteadyGroups() # Should be 1

wing_id = AddGeom( "WING" )

num_group = GetNumUnsteadyGroups() # Should be 2 (includes fixed component group)
```

  


### function GetNumUnsteadyRotorGroups

```
int GetNumUnsteadyRotorGroups()
```


**See**: [PROP_MODE](Modules/group___enumerations.md#enum-prop-mode), [GetNumUnsteadyGroups](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md#function-getnumunsteadygroups)

**Return**: Number of unsteady rotor groups in the current VSPAERO set 

Get the number of unsteady rotor groups in the current VSPAERO set. This is equivalent to the total number of propeller Geoms, including each symmetric copy, in the current VSPAERO set. While all fixed components (wings, fuseleage, etc.) are placed in their own unsteady group, this function does not consider them. 

// Set VSPAERO set index to SET_ALL
SetParmVal( FindParm( FindContainer( "VSPAEROSettings", 0 ), "GeomSet", "VSPAERO" ), SET_ALL );

// Add a propeller
string prop_id = AddGeom( "PROP" );
SetParmValUpdate( prop_id, "PropMode", "Design", PROP_DISK );

int num_group = GetNumUnsteadyRotorGroups(); // Should be 0

SetParmValUpdate( prop_id, "PropMode", "Design", PROP_BLADES );

num_group = GetNumUnsteadyRotorGroups(); // Should be 1

string wing_id = AddGeom( "WING" );

num_group = GetNumUnsteadyRotorGroups(); // Should be 1 still (fixed group not included)
```

 \endforcpponly \beginPythonOnly ```py

# Set VSPAERO set index to SET_ALL
SetParmVal( FindParm( FindContainer( "VSPAEROSettings", 0 ), "GeomSet", "VSPAERO" ), SET_ALL )

# Add a propeller
prop_id = AddGeom( "PROP" )
SetParmValUpdate( prop_id, "PropMode", "Design", PROP_DISK )

num_group = GetNumUnsteadyRotorGroups() # Should be 0

SetParmValUpdate( prop_id, "PropMode", "Design", PROP_BLADES )

num_group = GetNumUnsteadyRotorGroups() # Should be 1

wing_id = AddGeom( "WING" )

num_group = GetNumUnsteadyRotorGroups() # Should be 1 still (fixed group not included)
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800