---
title: VSPAERO Control Surface Group Functions
summary: This group of functions is available for manipulating VSPAERO control surface groups through the API. Note, VSPAERO also includes rectangle type sub-surfaces as possible control surfaces. Click here to return to the main page. 

---

# VSPAERO Control Surface Group Functions

This group of functions is available for manipulating VSPAERO control surface groups through the API. Note, VSPAERO also includes rectangle type sub-surfaces as possible control surfaces. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[AutoGroupVSPAEROControlSurfaces](Modules/group___c_s_group.md#function-autogroupvspaerocontrolsurfaces)**() |
| int | **[CreateVSPAEROControlSurfaceGroup](Modules/group___c_s_group.md#function-createvspaerocontrolsurfacegroup)**() |
| void | **[AddAllToVSPAEROControlSurfaceGroup](Modules/group___c_s_group.md#function-addalltovspaerocontrolsurfacegroup)**(int CSGroupIndex) |
| void | **[RemoveAllFromVSPAEROControlSurfaceGroup](Modules/group___c_s_group.md#function-removeallfromvspaerocontrolsurfacegroup)**(int CSGroupIndex) |
| std::vector< std::string > | **[GetActiveCSNameVec](Modules/group___c_s_group.md#function-getactivecsnamevec)**(int CSGroupIndex) |
| std::vector< std::string > | **[GetCompleteCSNameVec](Modules/group___c_s_group.md#function-getcompletecsnamevec)**() |
| std::vector< std::string > | **[GetAvailableCSNameVec](Modules/group___c_s_group.md#function-getavailablecsnamevec)**(int CSGroupIndex) |
| void | **[SetVSPAEROControlGroupName](Modules/group___c_s_group.md#function-setvspaerocontrolgroupname)**(const string & name, int CSGroupIndex) |
| std::string | **[GetVSPAEROControlGroupName](Modules/group___c_s_group.md#function-getvspaerocontrolgroupname)**(int CSGroupIndex) |
| void | **[AddSelectedToCSGroup](Modules/group___c_s_group.md#function-addselectedtocsgroup)**(const vector< int > & selected, int CSGroupIndex) |
| void | **[RemoveSelectedFromCSGroup](Modules/group___c_s_group.md#function-removeselectedfromcsgroup)**(const vector< int > & selected, int CSGroupIndex) |
| int | **[GetNumControlSurfaceGroups](Modules/group___c_s_group.md#function-getnumcontrolsurfacegroups)**() |


## Functions Documentation

### function AutoGroupVSPAEROControlSurfaces

```
void AutoGroupVSPAEROControlSurfaces()
```


**See**: [CreateVSPAEROControlSurfaceGroup](Modules/group___c_s_group.md#function-createvspaerocontrolsurfacegroup)

Creates the initial default grouping for the control surfaces. The initial grouping collects all surface copies of the sub-surface into a single group. For example if a wing is defined with an aileron and that wing is symmetrical about the xz plane there will be a surface copy of the master wing surface as well as a copy of the sub-surface. The two sub-surfaces may get deflected differently during analysis routines and can be identified uniquely by their full name. 

string wid = AddGeom( "WING", "" );                             // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL );                      // Add Control Surface Sub-Surface

//==== Add Vertical tail and set some parameters =====//
string vert_id = AddGeom( "WING" );

SetGeomName( vert_id, "Vert" );

SetParmValUpdate( vert_id, "TotalArea", "WingGeom", 10.0 );
SetParmValUpdate( vert_id, "X_Rel_Location", "XForm", 8.5 );
SetParmValUpdate( vert_id, "X_Rel_Rotation", "XForm", 90 );

string rudder_id = AddSubSurf( vert_id, SS_CONTROL );                      // Add Control Surface Sub-Surface

AutoGroupVSPAEROControlSurfaces();

Update();

Print( "COMPLETE\n" );
string control_group_settings_container_id = FindContainer( "VSPAEROSettings", 0 );   // auto grouping produces parm containers within VSPAEROSettings

//==== Set Control Surface Group Deflection Angle ====//
Print( "\tSetting control surface group deflection angles..." );

//  setup asymmetric deflection for aileron
string deflection_gain_id;

// subsurfaces get added to groups with "CSGQualities_[geom_name]_[control_surf_name]"
// subsurfaces gain parm name is "Surf[surfndx]_Gain" starting from 0 to NumSymmetricCopies-1

deflection_gain_id = FindParm( control_group_settings_container_id, "Surf_" + aileron_id + "_0_Gain", "ControlSurfaceGroup_0" );
deflection_gain_id = FindParm( control_group_settings_container_id, "Surf_" + aileron_id + "_1_Gain", "ControlSurfaceGroup_0" );

//  deflect aileron
string deflection_angle_id = FindParm( control_group_settings_container_id, "DeflectionAngle", "ControlSurfaceGroup_0" );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL )                      # Add Control Surface Sub-Surface

#==== Add Vertical tail and set some parameters =====//
vert_id = AddGeom( "WING" )

SetGeomName( vert_id, "Vert" )

SetParmValUpdate( vert_id, "TotalArea", "WingGeom", 10.0 )
SetParmValUpdate( vert_id, "X_Rel_Location", "XForm", 8.5 )
SetParmValUpdate( vert_id, "X_Rel_Rotation", "XForm", 90 )

rudder_id = AddSubSurf( vert_id, SS_CONTROL )                      # Add Control Surface Sub-Surface

AutoGroupVSPAEROControlSurfaces()

Update()

print( "COMPLETE\n" )
control_group_settings_container_id = FindContainer( "VSPAEROSettings", 0 )   # auto grouping produces parm containers within VSPAEROSettings

#==== Set Control Surface Group Deflection Angle ====//
print( "\tSetting control surface group deflection angles..." )

# subsurfaces get added to groups with "CSGQualities_[geom_name]_[control_surf_name]"
# subsurfaces gain parm name is "Surf[surfndx]_Gain" starting from 0 to NumSymmetricCopies-1

deflection_gain_id = FindParm( control_group_settings_container_id, "Surf_" + aileron_id + "_0_Gain", "ControlSurfaceGroup_0" )
deflection_gain_id = FindParm( control_group_settings_container_id, "Surf_" + aileron_id + "_1_Gain", "ControlSurfaceGroup_0" )

#  deflect aileron
deflection_angle_id = FindParm( control_group_settings_container_id, "DeflectionAngle", "ControlSurfaceGroup_0" )
```

  


### function CreateVSPAEROControlSurfaceGroup

```
int CreateVSPAEROControlSurfaceGroup()
```


**See**: [AddSelectedToCSGroup](Modules/group___c_s_group.md#function-addselectedtocsgroup)

**Return**: Index of the new VSPAERO control surface group 

Add a new VSPAERO control surface group using the default naming convention. The control surface group will not contain any control surfaces until they are added. 

string wid = AddGeom( "WING", "" );                             // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL );                      // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

int num_group = GetNumControlSurfaceGroups();

if ( num_group != 1 ) { Print( "Error: CreateVSPAEROControlSurfaceGroup" ); }
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL )                      # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

num_group = GetNumControlSurfaceGroups()

if  num_group != 1 : print( "Error: CreateVSPAEROControlSurfaceGroup" )
```

  


### function AddAllToVSPAEROControlSurfaceGroup

```
void AddAllToVSPAEROControlSurfaceGroup(
    int CSGroupIndex
)
```


**Parameters**: 

  * **CSGroupIndex** Index of the control surface group 


Add all available control surfaces to the control surface group at the specified index 

string wid = AddGeom( "WING", "" );                             // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL );                      // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

AddAllToVSPAEROControlSurfaceGroup( group_index );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL )                      # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

AddAllToVSPAEROControlSurfaceGroup( group_index )
```

  


### function RemoveAllFromVSPAEROControlSurfaceGroup

```
void RemoveAllFromVSPAEROControlSurfaceGroup(
    int CSGroupIndex
)
```


**Parameters**: 

  * **CSGroupIndex** Index of the control surface group 


Remove all used control surfaces from the control surface group at the specified index 

string wid = AddGeom( "WING", "" );                             // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL );                      // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

AddAllToVSPAEROControlSurfaceGroup( group_index );

RemoveAllFromVSPAEROControlSurfaceGroup( group_index ); // Empty control surface group
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL )                      # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

AddAllToVSPAEROControlSurfaceGroup( group_index )

RemoveAllFromVSPAEROControlSurfaceGroup( group_index ) # Empty control surface group
```

  


### function GetActiveCSNameVec

```
std::vector< std::string > GetActiveCSNameVec(
    int CSGroupIndex
)
```


**Parameters**: 

  * **CSGroupIndex** Index of the control surface group 


**Return**: Array of active control surface names 

Get the names of each active (used) control surface in the control surface group at the specified index 

string wid = AddGeom( "WING", "" );                             // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL );                      // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

AddAllToVSPAEROControlSurfaceGroup( group_index );

array<string> @cs_name_vec = GetActiveCSNameVec( group_index );

Print( "Active CS in Group Index #", false );
Print( group_index );

for ( int i = 0; i < int( cs_name_vec.size() ); i++ )
{
    Print( cs_name_vec[i] );
}
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL )                      # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

AddAllToVSPAEROControlSurfaceGroup( group_index )

cs_name_vec = GetActiveCSNameVec( group_index )

print( "Active CS in Group Index #", False )
print( group_index )

for i in range(int( len(cs_name_vec) )):

    print( cs_name_vec[i] )
```

  


### function GetCompleteCSNameVec

```
std::vector< std::string > GetCompleteCSNameVec()
```


**Return**: Array of all control surface names 

Get the names of all control surfaces. Some may be active (used) while others may be available. 

string wid = AddGeom( "WING", "" );                             // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL );                      // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

array<string> @cs_name_vec = GetCompleteCSNameVec();

Print( "All Control Surfaces: ", false );

for ( int i = 0; i < int( cs_name_vec.size() ); i++ )
{
    Print( cs_name_vec[i] );
}
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL )                      # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

cs_name_vec = GetCompleteCSNameVec()

print( "All Control Surfaces: ", False )

for i in range(int( len(cs_name_vec) )):

    print( cs_name_vec[i] )
```

  


### function GetAvailableCSNameVec

```
std::vector< std::string > GetAvailableCSNameVec(
    int CSGroupIndex
)
```


**Parameters**: 

  * **CSGroupIndex** Index of the control surface group 


**Return**: Array of active control surface names 

Get the names of each available (not used) control surface in the control surface group at the specified index 

string wid = AddGeom( "WING", "" ); // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL ); // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

array<string> @cs_name_vec = GetAvailableCSNameVec( group_index );

array < int > cs_ind_vec(1);
cs_ind_vec[0] = 1;

AddSelectedToCSGroup( cs_ind_vec, group_index ); // Add the first available control surface to the group
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" ) # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL ) # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

cs_name_vec = GetAvailableCSNameVec( group_index )

cs_ind_vec = [1]

AddSelectedToCSGroup( cs_ind_vec, group_index ) # Add the first available control surface to the group
```

  


### function SetVSPAEROControlGroupName

```
void SetVSPAEROControlGroupName(
    const string & name,
    int CSGroupIndex
)
```


**Parameters**: 

  * **name** Name to set for the control surface group 
  * **CSGroupIndex** Index of the control surface group 


Set the name for the control surface group at the specified index 

string wid = AddGeom( "WING", "" ); // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL ); // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

SetVSPAEROControlGroupName( "Example_CS_Group", group_index );

Print( "CS Group name: ", false );

Print( GetVSPAEROControlGroupName( group_index ) );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" ) # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL ) # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

SetVSPAEROControlGroupName( "Example_CS_Group", group_index )

print( "CS Group name: ", False )

print( GetVSPAEROControlGroupName( group_index ) )
```

  


### function GetVSPAEROControlGroupName

```
std::string GetVSPAEROControlGroupName(
    int CSGroupIndex
)
```


**Parameters**: 

  * **CSGroupIndex** Index of the control surface group 


Get the name of the control surface group at the specified index 

string wid = AddGeom( "WING", "" ); // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL ); // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

SetVSPAEROControlGroupName( "Example_CS_Group", group_index );

Print( "CS Group name: ", false );

Print( GetVSPAEROControlGroupName( group_index ) );
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" ) # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL ) # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

SetVSPAEROControlGroupName( "Example_CS_Group", group_index )

print( "CS Group name: ", False )

print( GetVSPAEROControlGroupName( group_index ) )
```

  


### function AddSelectedToCSGroup

```
void AddSelectedToCSGroup(
    const vector< int > & selected,
    int CSGroupIndex
)
```


**Parameters**: 

  * **selected** Array of control surface indexes to add to the group. Note, the integer values are one based. 
  * **CSGroupIndex** Index of the control surface group 


**See**: [GetAvailableCSNameVec](Modules/group___c_s_group.md#function-getavailablecsnamevec)

**Warning**: The indexes in input "selected" must be matched with available control surfaces identified by GetAvailableCSNameVec. The "selected" input uses one- based indexing to associate available control surfaces.

Add each control surfaces in the array of control surface indexes to the control surface group at the specified index.




string wid = AddGeom( "WING", "" ); // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL ); // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

array < string > cs_name_vec = GetAvailableCSNameVec( group_index );

array < int > cs_ind_vec( cs_name_vec.size() );

for ( int i = 0; i < int( cs_name_vec.size() ); i++ )
{
    cs_ind_vec[i] = i + 1;
}

AddSelectedToCSGroup( cs_ind_vec, group_index ); // Add all available control surfaces to the group
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" ) # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL ) # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

cs_name_vec = GetAvailableCSNameVec( group_index )

cs_ind_vec = [0] * len(cs_name_vec)

for i in range(int( len(cs_name_vec) )):

    cs_ind_vec[i] = i + 1

AddSelectedToCSGroup( cs_ind_vec, group_index ) # Add all available control surfaces to the group
```

  


### function RemoveSelectedFromCSGroup

```
void RemoveSelectedFromCSGroup(
    const vector< int > & selected,
    int CSGroupIndex
)
```


**Parameters**: 

  * **selected** Array of control surface indexes to remove from the group. Note, the integer values are one based. 
  * **CSGroupIndex** Index of the control surface group 


**See**: [GetActiveCSNameVec](Modules/group___c_s_group.md#function-getactivecsnamevec)

**Warning**: The indexes in input "selected" must be matched with active control surfaces identified by GetActiveCSNameVec. The "selected" input uses one-based indexing to associate available control surfaces.

Remove each control surfaces in the array of control surface indexes from the control surface group at the specified index.




string wid = AddGeom( "WING", "" ); // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL ); // Add Control Surface Sub-Surface

int group_index = CreateVSPAEROControlSurfaceGroup(); // Empty control surface group

array < string > cs_name_vec = GetAvailableCSNameVec( group_index );

array < int > cs_ind_vec( cs_name_vec.size() );

for ( int i = 0; i < int( cs_name_vec.size() ); i++ )
{
    cs_ind_vec[i] = i + 1;
}

AddSelectedToCSGroup( cs_ind_vec, group_index ); // Add the available control surfaces to the group

array < int > remove_cs_ind_vec( 1 );
remove_cs_ind_vec[0] = 1;

RemoveSelectedFromCSGroup( remove_cs_ind_vec, group_index ); // Remove the first control surface
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" ) # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL ) # Add Control Surface Sub-Surface

group_index = CreateVSPAEROControlSurfaceGroup() # Empty control surface group

cs_name_vec = GetAvailableCSNameVec( group_index )

cs_ind_vec = [0] * len(cs_name_vec)

for i in range(int( len(cs_name_vec) )):

    cs_ind_vec[i] = i + 1

AddSelectedToCSGroup( cs_ind_vec, group_index ) # Add the available control surfaces to the group

remove_cs_ind_vec = [1]

RemoveSelectedFromCSGroup( remove_cs_ind_vec, group_index ) # Remove the first control surface
```

  


### function GetNumControlSurfaceGroups

```
int GetNumControlSurfaceGroups()
```


**Return**: Number of control surface groups 

Get the total number of control surface groups 

string wid = AddGeom( "WING", "" );                             // Add Wing

string aileron_id = AddSubSurf( wid, SS_CONTROL );                      // Add Control Surface Sub-Surface

//==== Add Horizontal tail and set some parameters =====//
string horiz_id = AddGeom( "WING", "" );

SetGeomName( horiz_id, "Vert" );

SetParmValUpdate( horiz_id, "TotalArea", "WingGeom", 10.0 );
SetParmValUpdate( horiz_id, "X_Rel_Location", "XForm", 8.5 );

string elevator_id = AddSubSurf( horiz_id, SS_CONTROL );                      // Add Control Surface Sub-Surface

AutoGroupVSPAEROControlSurfaces();

int num_group = GetNumControlSurfaceGroups();

if ( num_group != 2 ) { Print( "Error: GetNumControlSurfaceGroups" ); }
```

 \endforcpponly \beginPythonOnly ```py

wid = AddGeom( "WING", "" )                             # Add Wing

aileron_id = AddSubSurf( wid, SS_CONTROL )                      # Add Control Surface Sub-Surface

#==== Add Horizontal tail and set some parameters =====//
horiz_id = AddGeom( "WING", "" )

SetGeomName( horiz_id, "Vert" )

SetParmValUpdate( horiz_id, "TotalArea", "WingGeom", 10.0 )
SetParmValUpdate( horiz_id, "X_Rel_Location", "XForm", 8.5 )

elevator_id = AddSubSurf( horiz_id, SS_CONTROL )                      # Add Control Surface Sub-Surface

AutoGroupVSPAEROControlSurfaces()

num_group = GetNumControlSurfaceGroups()

if  num_group != 2 : print( "Error: GetNumControlSurfaceGroups" )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800