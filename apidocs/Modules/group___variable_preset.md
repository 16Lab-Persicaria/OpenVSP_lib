---
title: Variable Preset Functions
summary: This group of functions can be used to add, remove, and modify Variable Presets through the API. Click here to return to the main page. 

---

# Variable Preset Functions

This group of functions can be used to add, remove, and modify Variable Presets through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| string | **[AddVarPresetGroup](Modules/group___variable_preset.md#function-addvarpresetgroup)**(const std::string & group_name) |
| string | **[AddVarPresetSetting](Modules/group___variable_preset.md#function-addvarpresetsetting)**(const std::string & group_id, const std::string & setting_name) |
| void | **[AddVarPresetParm](Modules/group___variable_preset.md#function-addvarpresetparm)**(const std::string & group_id, const std::string & parm_id) |
| void | **[DeleteVarPresetGroup](Modules/group___variable_preset.md#function-deletevarpresetgroup)**(const std::string & group_id) |
| void | **[DeleteVarPresetSetting](Modules/group___variable_preset.md#function-deletevarpresetsetting)**(const std::string & group_id, const std::string & setting_id) |
| void | **[DeleteVarPresetParm](Modules/group___variable_preset.md#function-deletevarpresetparm)**(const std::string & group_id, const std::string & parm_id) |
| void | **[SetVarPresetParmVal](Modules/group___variable_preset.md#function-setvarpresetparmval)**(const std::string & group_id, const std::string & setting_id, const std::string & parm_id, double parm_val) |
| double | **[GetVarPresetParmVal](Modules/group___variable_preset.md#function-getvarpresetparmval)**(const std::string & group_id, const std::string & setting_id, const std::string & parm_id) |
| std::string | **[GetGroupName](Modules/group___variable_preset.md#function-getgroupname)**(const std::string & group_id) |
| std::string | **[GetSettingName](Modules/group___variable_preset.md#function-getsettingname)**(const std::string & setting_id) |
| void | **[SetGroupName](Modules/group___variable_preset.md#function-setgroupname)**(const std::string & group_id, const std::string & group_name) |
| void | **[SetSettingName](Modules/group___variable_preset.md#function-setsettingname)**(const std::string & setting_id, const std::string & setting_name) |
| std::vector< std::string > | **[GetVarPresetGroups](Modules/group___variable_preset.md#function-getvarpresetgroups)**() |
| std::vector< std::string > | **[GetVarPresetSettings](Modules/group___variable_preset.md#function-getvarpresetsettings)**(const std::string & group_id) |
| std::vector< std::string > | **[GetVarPresetParmIDs](Modules/group___variable_preset.md#function-getvarpresetparmids)**(const std::string & group_id) |
| std::vector< double > | **[GetVarPresetParmVals](Modules/group___variable_preset.md#function-getvarpresetparmvals)**(const std::string & setting_id) |
| void | **[SetVarPresetParmVals](Modules/group___variable_preset.md#function-setvarpresetparmvals)**(const std::string & setting_id, const std::vector< double > & parm_vals) |
| void | **[SaveVarPresetParmVals](Modules/group___variable_preset.md#function-savevarpresetparmvals)**(const std::string & group_id, const std::string & setting_id) |
| void | **[ApplyVarPresetSetting](Modules/group___variable_preset.md#function-applyvarpresetsetting)**(const std::string & group_id, const std::string & setting_id) |


## Functions Documentation

### function AddVarPresetGroup

```
string AddVarPresetGroup(
    const std::string & group_name
)
```


**Parameters**: 

  * **group_name** string Name for Var Preset Group 


**Return**: string Var Preset Group ID 

Add a Variable Preset Group 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )
```

  


### function AddVarPresetSetting

```
string AddVarPresetSetting(
    const std::string & group_id,
    const std::string & setting_name
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **setting_name** string Var Preset Setting Name 


**Return**: string Var Preset Setting ID 

Add a Setting to the Variable Preset Group 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid =AddVarPresetSetting( gid, "Coarse" );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )
```

  


### function AddVarPresetParm

```
void AddVarPresetParm(
    const std::string & group_id,
    const std::string & parm_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **parm_id** string Parm ID 


Add a Parm to the Variable Preset Group 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )
```

  


### function DeleteVarPresetGroup

```
void DeleteVarPresetGroup(
    const std::string & group_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 


Delete Variable Preset Group (and all contained settings) 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

DeleteVarPresetGroup( gid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

DeleteVarPresetGroup( gid )
```

  


### function DeleteVarPresetSetting

```
void DeleteVarPresetSetting(
    const std::string & group_id,
    const std::string & setting_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **setting_id** string Var Preset Setting ID 


Delete Variable Preset Setting 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

DeleteVarPresetSetting( gid, sid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

DeleteVarPresetSetting( gid, sid )
```

  


### function DeleteVarPresetParm

```
void DeleteVarPresetParm(
    const std::string & group_id,
    const std::string & parm_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **parm_id** string Var Parm ID 


Delete Parm from Variable Preset Group 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

DeleteVarPresetParm( gid, p1 );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

DeleteVarPresetParm( gid, p1 )
```

  


### function SetVarPresetParmVal

```
void SetVarPresetParmVal(
    const std::string & group_id,
    const std::string & setting_id,
    const std::string & parm_id,
    double parm_val
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **setting_id** string Var Preset Setting ID 
  * **parm_id** string Var Parm ID 
  * **parm_val** double Parm value 


Set value for Parm in Var Preset Setting 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

SetVarPresetParmVal( gid, sid, p1, 51 );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

SetVarPresetParmVal( gid, sid, p1, 51 )
```

  


### function GetVarPresetParmVal

```
double GetVarPresetParmVal(
    const std::string & group_id,
    const std::string & setting_id,
    const std::string & parm_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **setting_id** string Var Preset Setting ID 
  * **parm_id** string Var Parm ID 


**Return**: double Var Preset Parm value 

Get value for Parm in Var Preset Setting 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

double val = GetVarPresetParmVal( gid, sid, p1 );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

val = GetVarPresetParmVal( gid, sid, p1 )
```

  


### function GetGroupName

```
std::string GetGroupName(
    const std::string & group_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 


**Return**: string Var Preset Group name 

Get Variable Preset group name 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string name = GetGroupName( gid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

name = GetGroupName( gid )
```

  


### function GetSettingName

```
std::string GetSettingName(
    const std::string & setting_id
)
```


**Parameters**: 

  * **setting_id** string Var Preset Setting ID 


**Return**: string Var Preset Setting name 

Get Variable Preset Setting name 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string name = GetSettingName( sid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

name = GetSettingName( sid )
```

  


### function SetGroupName

```
void SetGroupName(
    const std::string & group_id,
    const std::string & group_name
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **group_name** string New Var Preset Group name 


Set Variable Preset group name 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

SetGroupName( gid, "Resolution" );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

SetGroupName( gid, "Resolution" )
```

  


### function SetSettingName

```
void SetSettingName(
    const std::string & setting_id,
    const std::string & setting_name
)
```


**Parameters**: 

  * **setting_id** string Var Preset Setting ID 
  * **setting_name** string New Var Preset Setting name 


Set Variable Preset Setting name 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

SetSettingName( sid, "Low" );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

SetSettingName( sid, "Low" )
```

  


### function GetVarPresetGroups

```
std::vector< std::string > GetVarPresetGroups()
```


**Return**: array<string> Array of Variable Preset Group IDs 

Get group_ids for Variable Preset Groups 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

array <string> group_ids = GetVarPresetGroups();
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

group_ids = GetVarPresetGroups()
```

  


### function GetVarPresetSettings

```
std::vector< std::string > GetVarPresetSettings(
    const std::string & group_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 


**Return**: array<string> Array of Variable Preset Group ParmIDs 

Get Setting IDs for Variable Preset Group 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

array <string> settingids = GetVarPresetSettings( gid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

settingds = GetVarPresetSettings( gid )
```

  


### function GetVarPresetParmIDs

```
std::vector< std::string > GetVarPresetParmIDs(
    const std::string & group_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 


**Return**: array<string> Array of Variable Preset Group ParmIDs 

Get ParmIDs for Variable Preset Group 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

array <string> parmids = GetVarPresetParmIDs( gid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

parmids = GetVarPresetParmIDs( gid )
```

  


### function GetVarPresetParmVals

```
std::vector< double > GetVarPresetParmVals(
    const std::string & setting_id
)
```


**Parameters**: 

  * **setting_id** string Var Preset Setting ID 


**Return**: array<double> Var Preset Parm values for Setting 

Get Parm values for Variable Preset Setting 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

array < double > parmval_vec = GetVarPresetParmVals( sid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

parmval_vec = GetVarPresetParmVals( sid )
```

  


### function SetVarPresetParmVals

```
void SetVarPresetParmVals(
    const std::string & setting_id,
    const std::vector< double > & parm_vals
)
```


**Parameters**: 

  * **setting_id** string Var Preset Setting ID 
  * **parm_vals** array<double> Array of Variable Preset Group Parm values 


Set Parm values for Variable Preset Setting 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

array <double> vals = { 45 };

SetVarPresetParmVals( sid, vals );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

vals = [ 45 ]

SetVarPresetParmVals( sid, vals )
```

  


### function SaveVarPresetParmVals

```
void SaveVarPresetParmVals(
    const std::string & group_id,
    const std::string & setting_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **setting_id** string Var Preset Setting ID 


Save current Parm values to Variable Preset Setting 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

SaveVarPresetParmVals( gid, sid );
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

SaveVarPresetParmVals( gid, sid )
```

  


### function ApplyVarPresetSetting

```
void ApplyVarPresetSetting(
    const std::string & group_id,
    const std::string & setting_id
)
```


**Parameters**: 

  * **group_id** string Var Preset Group ID 
  * **setting_id** string Var Preset Setting ID 


Apply Parm values for Var Preset Setting 

// Add Pod Geom
string pod1 = AddGeom( "POD", "" );

string gid = AddVarPresetGroup( "Tess" );

string sid = AddVarPresetSetting( gid, "Coarse" );

string p1 = FindParm( pod1, "Tess_U", "Shape" );

AddVarPresetParm( gid, p1 );

ApplyVarPresetSetting( gid, sid );

Update();
```

 

# Add Pod Geom
pod1 = AddGeom( "POD", "" )

gid = AddVarPresetGroup( "Tess" )

sid = AddVarPresetSetting( gid, "Coarse" )

p1 = FindParm( pod1, "Tess_U", "Shape" )

AddVarPresetParm( gid, p1 )

ApplyVarPresetSetting( gid, sid )

Update()
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800