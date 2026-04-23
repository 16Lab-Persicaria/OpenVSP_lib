---
title: Group Modification Functions
summary: The functions in this group allow for sets to be scaled, rotated, and translated. Click here to return to the main page. 

---

# Group Modification Functions

The functions in this group allow for sets to be scaled, rotated, and translated. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[ScaleSet](Modules/group___group_mod.md#function-scaleset)**(int set_index, double scale) |
| void | **[RotateSet](Modules/group___group_mod.md#function-rotateset)**(int set_index, double x_rot_deg, double y_rot_deg, double z_rot_deg) |
| void | **[TranslateSet](Modules/group___group_mod.md#function-translateset)**(int set_index, const vec3d & translation_vec) |
| void | **[TransformSet](Modules/group___group_mod.md#function-transformset)**(int set_index, const vec3d & translation_vec, double x_rot_deg, double y_rot_deg, double z_rot_deg, double scale, bool scale_translations_flag) |


## Functions Documentation

### function ScaleSet

```
void ScaleSet(
    int set_index,
    double scale
)
```


**Parameters**: 

  * **set_index** Set index 
  * **scale** Scale factor 


Apply a scale factor to a set 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE" );

SetSetFlag( fuseid, 3, true );

// Scale by a factor of 2
ScaleSet( 3, 2.0 );
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE" )

SetSetFlag( fuseid, 3, True )

# Scale by a factor of 2
ScaleSet( 3, 2.0 )
```

  


### function RotateSet

```
void RotateSet(
    int set_index,
    double x_rot_deg,
    double y_rot_deg,
    double z_rot_deg
)
```


**Parameters**: 

  * **set_index** Set index 
  * **x_rot_deg** Rotation about the X axis (degrees) 
  * **y_rot_deg** Rotation about the Y axis (degrees) 
  * **z_rot_deg** Rotation about the Z axis (degrees) 


Rotate a set about the global X, Y, and Z axes 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE" );

SetSetFlag( fuseid, 3, true );

// Rotate 90 degrees about Y
RotateSet( 3, 0, 90, 0 );
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE" )

SetSetFlag( fuseid, 3, True )

# Rotate 90 degrees about Y
RotateSet( 3, 0, 90, 0 )
```

  


### function TranslateSet

```
void TranslateSet(
    int set_index,
    const vec3d & translation_vec
)
```


**Parameters**: 

  * **set_index** Set index 
  * **translation_vec** Translation vector 


Translate a set along a given vector 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE" );

SetSetFlag( fuseid, 3, true );

// Translate 2 units in X and 3 units in Y
TranslateSet( 3, vec3d( 2, 3, 0 ) );
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE" )

SetSetFlag( fuseid, 3, True )

# Translate 2 units in X and 3 units in Y
TranslateSet( 3, vec3d( 2, 3, 0 ) )
```

  


### function TransformSet

```
void TransformSet(
    int set_index,
    const vec3d & translation_vec,
    double x_rot_deg,
    double y_rot_deg,
    double z_rot_deg,
    double scale,
    bool scale_translations_flag
)
```


**Parameters**: 

  * **set_index** Set index 
  * **translation_vec** Translation vector 
  * **x_rot_deg** Rotation about the X axis (degrees) 
  * **y_rot_deg** Rotation about the Y axis (degrees) 
  * **z_rot_deg** Rotation about the Z axis (degrees) 
  * **scale** Scale factor 
  * **scale_translations_flag** Flag to apply the scale factor to translations 


**See**: [TranslateSet](Modules/group___group_mod.md#function-translateset), [RotateSet](Modules/group___group_mod.md#function-rotateset), [ScaleSet](Modules/group___group_mod.md#function-scaleset)

Apply translation, rotation, and scale transformations to a set 

// Add Fuselage Geom
string fuseid = AddGeom( "FUSELAGE" );

SetSetFlag( fuseid, 3, true );

// Translate 2 units in X and 3 units in Y, rotate 90 degrees about Y, and scale by a factor of 2
TransformSet( 3, vec3d( 2, 3, 0 ), 0, 90, 0, 2.0, true );
```

 \endforcpponly \beginPythonOnly ```py

# Add Fuselage Geom
fuseid = AddGeom( "FUSELAGE" )

SetSetFlag( fuseid, 3, True )

# Translate 2 units in X and 3 units in Y, rotate 90 degrees about Y, and scale by a factor of 2
TransformSet( 3, vec3d( 2, 3, 0 ), 0, 90, 0, 2.0, True )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800