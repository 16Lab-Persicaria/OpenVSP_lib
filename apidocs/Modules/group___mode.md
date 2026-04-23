---
title: Mode Functions
summary: This group of API functions are used to manipulate Modes  a combination of Sets and Variable Presets Click here to return to the main page. 

---

# Mode Functions

This group of API functions are used to manipulate Modes &ndash; a combination of Sets and Variable Presets Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| string | **[CreateAndAddMode](Modules/group___mode.md#function-createandaddmode)**(const string & name, int normal_set, int degen_set) |
| int | **[GetNumModes](Modules/group___mode.md#function-getnummodes)**() |
| vector< string > | **[GetAllModes](Modules/group___mode.md#function-getallmodes)**() |
| void | **[DelMode](Modules/group___mode.md#function-delmode)**(const string & mid) |
| void | **[DelAllModes](Modules/group___mode.md#function-delallmodes)**() |
| void | **[ApplyModeSettings](Modules/group___mode.md#function-applymodesettings)**(const string & mid) |
| void | **[ShowOnlyMode](Modules/group___mode.md#function-showonlymode)**(const string & mid) |
| void | **[ModeAddGroupSetting](Modules/group___mode.md#function-modeaddgroupsetting)**(const string & mid, const string & gid, const string & sid) |
| string | **[ModeGetGroup](Modules/group___mode.md#function-modegetgroup)**(const string & mid, int indx) |
| string | **[ModeGetSetting](Modules/group___mode.md#function-modegetsetting)**(const string & mid, int indx) |
| vector< string > | **[ModeGetAllGroups](Modules/group___mode.md#function-modegetallgroups)**(const string & mid) |
| vector< string > | **[ModeGetAllSettings](Modules/group___mode.md#function-modegetallsettings)**(const string & mid) |
| void | **[RemoveGroupSetting](Modules/group___mode.md#function-removegroupsetting)**(const string & mid, int indx) |
| void | **[RemoveAllGroupSettings](Modules/group___mode.md#function-removeallgroupsettings)**(const string & mid) |


## Functions Documentation

### function CreateAndAddMode

```
string CreateAndAddMode(
    const string & name,
    int normal_set,
    int degen_set
)
```


**Parameters**: 

  * **name** string Name for new Mode 
  * **normal_set** int Normal set for Mode 
  * **degen_set** int Degen set for Mode 


**Return**: string Mode ID for new Mode 

Create a Mode &ndash; a combination of Sets and Variable Presets 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()
```

  


### function GetNumModes

```
int GetNumModes()
```


**Return**: int Number of Modes in model. 

Get number of Modes in model. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

int nmod = GetNumModes();
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

nmod = GetNumModes()
```

  


### function GetAllModes

```
vector< string > GetAllModes()
```


**Return**: array<string> array of Mode IDs 

Get all ModeID's in model. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

array<string> modids = GetAllModes();
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

modids = GetAllModes();
```

  


### function DelMode

```
void DelMode(
    const string & mid
)
```


**Parameters**: 

  * **mid** string Mode ID of mode to delete 


Delete a mode from the model. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

DelMode( mid1 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

DelMode( mid1 )
```

  


### function DelAllModes

```
void DelAllModes()
```


Delete all modes from the model. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

DelAllModes();
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

DelAllModes()
```

  


### function ApplyModeSettings

```
void ApplyModeSettings(
    const string & mid
)
```


**Parameters**: 

  * **mid** string Mode ID of mode to apply 


Apply Parm settings corresponding to a Mode. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()
```

  


### function ShowOnlyMode

```
void ShowOnlyMode(
    const string & mid
)
```


**Parameters**: 

  * **mid** string Mode ID of mode to show-only 


Show-only a mode in a model. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

ShowOnlyMode( mid1 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

ShowOnlyMode( mid1 )
```

  


### function ModeAddGroupSetting

```
void ModeAddGroupSetting(
    const string & mid,
    const string & gid,
    const string & sid
)
```


**Parameters**: 

  * **mid** string Mode ID to add variable preset to 
  * **gid** string Variable preset group ID to add to mode 
  * **sid** string Variable preset setting ID to add to mode 


Add a variable preset group and setting to a mode. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()
```

  


### function ModeGetGroup

```
string ModeGetGroup(
    const string & mid,
    int indx
)
```


**Parameters**: 

  * **mid** string Mode ID to return GroupID 
  * **indx** int Index of Variable preset to return GroupID 


**Return**: string Group ID for Mode Variable preset indx 

Get the group ID of var preset indx from a mode. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

string gid3 = ModeGetGroup( mid1, 0 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

gid3 = ModeGetGroup( mid1, 0 )
```

  


### function ModeGetSetting

```
string ModeGetSetting(
    const string & mid,
    int indx
)
```


**Parameters**: 

  * **mid** string Mode ID to return settingID 
  * **indx** int Index of Variable preset to return SettingID 


**Return**: string Setting ID for Mode Variable preset indx 

Get the setting ID of var preset indx from a mode. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

string sid6 = ModeGetSetting( mid1, 0 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

sid6 = ModeGetSetting( mid1, 0 )
```

  


### function ModeGetAllGroups

```
vector< string > ModeGetAllGroups(
    const string & mid
)
```


**Parameters**: 

  * **mid** string Mode ID to return all group IDs 


**Return**: array<string> array of Group IDs 

Get all var preset group IDs in model. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

array<string> gids = ModeGetAllGroups( mid1 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

gids = ModeGetAllGroups( mid1 )
```

  


### function ModeGetAllSettings

```
vector< string > ModeGetAllSettings(
    const string & mid
)
```


**Parameters**: 

  * **mid** string Mode ID to return all group IDs 


**Return**: array<string> array of Group IDs 

Get all var preset setting IDs in model. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

array<string> sids = ModeGetAllSettings( mid1 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

sids = ModeGetAllSettings( mid1 )
```

  


### function RemoveGroupSetting

```
void RemoveGroupSetting(
    const string & mid,
    int indx
)
```


**Parameters**: 

  * **mid** string Mode ID to remove varible preset group and setting from 
  * **indx** int Index of Variable preset to remove 


Remove the indx'th variable preset group and setting from the specified mode. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

RemoveGroupSetting( mid1, 0 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

RemoveGroupSetting( mid1, 0 )
```

  


### function RemoveAllGroupSettings

```
void RemoveAllGroupSettings(
    const string & mid
)
```


**Parameters**: 

  * **mid** string Mode ID to remove all variable presets from 


Remove all variable preset groups and settings from mode. 

// Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
//
// Setup boiler plate.
string pod1 = AddGeom( "POD", "" );
string wing = AddGeom( "WING", pod1 );

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN );
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 );

SetSetName( SET_FIRST_USER, "NonLifting" );
SetSetName( SET_FIRST_USER + 1, "Lifting" );

SetSetFlag( pod1, SET_FIRST_USER, true );
SetSetFlag( wing, SET_FIRST_USER + 1, true );


string gid = AddVarPresetGroup( "Tess" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );
AddVarPresetParm( gid, p1 );

string p2 = FindParm( pod1, "Tess_W", "Shape" );
AddVarPresetParm( gid, p2 );

string sid = AddVarPresetSetting( gid, "Default" );
SaveVarPresetParmVals( gid, sid );

string sid1 = AddVarPresetSetting( gid, "Coarse" );
SetVarPresetParmVal( gid, sid1, p1, 3 );
SetVarPresetParmVal( gid, sid1, p2, 5 );

string sid2 = AddVarPresetSetting( gid, "Fine" );
SetVarPresetParmVal( gid, sid, p1, 35 );
SetVarPresetParmVal( gid, sid, p2, 21 );


string gid2 = AddVarPresetGroup( "Design" );

string p3 = FindParm( pod1, "Length", "Design" );
AddVarPresetParm( gid2, p3 );

string p4 = FindParm( pod1, "FineRatio", "Design" );
AddVarPresetParm( gid2, p4 );

string sid3 = AddVarPresetSetting( gid2, "Normal" );
SaveVarPresetParmVals( gid2, sid3 );

string sid4 = AddVarPresetSetting( gid2, "ShortFat" );
SetVarPresetParmVal( gid2, sid4, p3, 3.0 );
SetVarPresetParmVal( gid2, sid4, p4, 5.0 );

string sid5 = AddVarPresetSetting( gid2, "LongThin" );
SetVarPresetParmVal( gid2, sid5, p3, 20.0 );
SetVarPresetParmVal( gid2, sid5, p4, 35.0 );

// End of setup boiler plate.

string mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE );
ModeAddGroupSetting( mid1, gid, sid1 );
ModeAddGroupSetting( mid1, gid2, sid4 );

string mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 );
ModeAddGroupSetting( mid2, gid, sid2 );
ModeAddGroupSetting( mid1, gid2, sid5 );

ApplyModeSettings( mid2 );
Update();

RemoveAllGroupSettings( mid1 );
```

 

# Illustrating use of Modes requires substantial setup of the model including components, sets, and variable presets.
#
# Setup boiler plate.
pod1 = AddGeom( "POD", "" )
wing = AddGeom( "WING", pod1 )

SetParmVal( wing, "Trans_Attach_Flag", "Attach", ATTACH_TRANS_LMN )
SetParmVal( wing, "L_Attach_Location", "Attach", 0.35 )

SetSetName( SET_FIRST_USER, "NonLifting" )
SetSetName( SET_FIRST_USER + 1, "Lifting" )

SetSetFlag( pod1, SET_FIRST_USER, True )
SetSetFlag( wing, SET_FIRST_USER + 1, True )


gid = AddVarPresetGroup( "Tess" )

p1 = FindParm( pod1, "Tess_U", "Shape" )
AddVarPresetParm( gid, p1 )

p2 = FindParm( pod1, "Tess_W", "Shape" )
AddVarPresetParm( gid, p2 )

sid = AddVarPresetSetting( gid, "Default" )
SaveVarPresetParmVals( gid, sid )

sid1 = AddVarPresetSetting( gid, "Coarse" )
SetVarPresetParmVal( gid, sid1, p1, 3 )
SetVarPresetParmVal( gid, sid1, p2, 5 )

sid2 = AddVarPresetSetting( gid, "Fine" )
SetVarPresetParmVal( gid, sid, p1, 35 )
SetVarPresetParmVal( gid, sid, p2, 21 )


gid2 = AddVarPresetGroup( "Design" )

p3 = FindParm( pod1, "Length", "Design" )
AddVarPresetParm( gid2, p3 )

p4 = FindParm( pod1, "FineRatio", "Design" )
AddVarPresetParm( gid2, p4 )

sid3 = AddVarPresetSetting( gid2, "Normal" )
SaveVarPresetParmVals( gid2, sid3 )

sid4 = AddVarPresetSetting( gid2, "ShortFat" )
SetVarPresetParmVal( gid2, sid4, p3, 3.0 )
SetVarPresetParmVal( gid2, sid4, p4, 5.0 )

sid5 = AddVarPresetSetting( gid2, "LongThin" )
SetVarPresetParmVal( gid2, sid5, p3, 20.0 )
SetVarPresetParmVal( gid2, sid5, p4, 35.0 )

# End of setup boiler plate.

mid1 = CreateAndAddMode( "FatWetAreas", SET_ALL, SET_NONE )
ModeAddGroupSetting( mid1, gid, sid1 )
ModeAddGroupSetting( mid1, gid2, sid4 )

mid2 = CreateAndAddMode( "ThinAero", SET_FIRST_USER, SET_FIRST_USER + 1 )
ModeAddGroupSetting( mid2, gid, sid2 )
ModeAddGroupSetting( mid1, gid2, sid5 )

ApplyModeSettings( mid2 )
Update()

RemoveAllGroupSettings( mid1 )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800