---
title: VSPAERO Functions
summary: The following group of functions are specific to VSPAERO. However, their relevance has been mostly replaced by Analysis Manager capabilities. Click here to return to the main page. 

---

# VSPAERO Functions

The following group of functions are specific to VSPAERO. However, their relevance has been mostly replaced by Analysis Manager capabilities. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| string | **[GetVSPAERORefWingID](Modules/group___v_s_p_a_e_r_o.md#function-getvspaerorefwingid)**() |
| string | **[SetVSPAERORefWingID](Modules/group___v_s_p_a_e_r_o.md#function-setvspaerorefwingid)**(const std::string & geom_id) |


## Functions Documentation

### function GetVSPAERORefWingID

```
string GetVSPAERORefWingID()
```


**Return**: Reference Geom ID 

Get ID of the current VSPAERO reference Geom 


### function SetVSPAERORefWingID

```
string SetVSPAERORefWingID(
    const std::string & geom_id
)
```


**Parameters**: 

  * **geom_id** Reference Geom ID 


Set the current VSPAERO reference Geom ID 

//==== Add Wing Geom and set some parameters =====//
string wing_id = AddGeom( "WING" );

SetGeomName( wing_id, "MainWing" );

//==== Add Vertical tail and set some parameters =====//
string vert_id = AddGeom( "WING" );

SetGeomName( vert_id, "Vert" );

SetParmValUpdate( vert_id, "TotalArea", "WingGeom", 10.0 );
SetParmValUpdate( vert_id, "X_Rel_Location", "XForm", 8.5 );
SetParmValUpdate( vert_id, "X_Rel_Rotation", "XForm", 90 );

//==== Set VSPAERO Reference lengths & areas ====//
SetVSPAERORefWingID( wing_id ); // Set as reference wing for VSPAERO

Print( "VSPAERO Reference Wing ID: ", false );

Print( GetVSPAERORefWingID() );
```

 \endforcpponly \beginPythonOnly ```py

#==== Add Wing Geom and set some parameters =====//
wing_id = AddGeom( "WING" )

SetGeomName( wing_id, "MainWing" )

#==== Add Vertical tail and set some parameters =====//
vert_id = AddGeom( "WING" )

SetGeomName( vert_id, "Vert" )

SetParmValUpdate( vert_id, "TotalArea", "WingGeom", 10.0 )
SetParmValUpdate( vert_id, "X_Rel_Location", "XForm", 8.5 )
SetParmValUpdate( vert_id, "X_Rel_Rotation", "XForm", 90 )

#==== Set VSPAERO Reference lengths & areas ====//
SetVSPAERORefWingID( wing_id ) # Set as reference wing for VSPAERO

print( "VSPAERO Reference Wing ID: ", False )

print( GetVSPAERORefWingID() )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800