---
title: Matrix4d Functions
summary: API functions that utilize the Matrix4d class are grouped here. For details of the class, including member functions, see Matrix4d. Click here to return to the main page. 

---

# Matrix4d Functions

API functions that utilize the [Matrix4d](Classes/class_matrix4d.md) class are grouped here. For details of the class, including member functions, see [Matrix4d](Classes/class_matrix4d.md). Click here to return to the main page. 

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[Matrix4d](Classes/class_matrix4d.md)**  |

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[loadIdentity](Modules/group___matrix4d.md#function-loadidentity)**() |
| void | **[translatef](Modules/group___matrix4d.md#function-translatef)**(const double & x, const double & y, const double & z) |
| void | **[rotateX](Modules/group___matrix4d.md#function-rotatex)**(const double & ang) |
| void | **[rotateY](Modules/group___matrix4d.md#function-rotatey)**(const double & ang) |
| void | **[rotateZ](Modules/group___matrix4d.md#function-rotatez)**(const double & ang) |
| void | **[rotate](Modules/group___matrix4d.md#function-rotate)**(const double & angle, const [vec3d](Classes/classvec3d.md) & axis) |
| void | **[affineInverse](Modules/group___matrix4d.md#function-affineinverse)**() |
| void | **[scale](Modules/group___matrix4d.md#function-scale)**(const double & scale) |
| void | **[loadXZRef](Modules/group___matrix4d.md#function-loadxzref)**() |
| void | **[loadXYRef](Modules/group___matrix4d.md#function-loadxyref)**() |
| void | **[loadYZRef](Modules/group___matrix4d.md#function-loadyzref)**() |
| void | **[mirrory](Modules/group___matrix4d.md#function-mirrory)**() |
| [vec3d](Classes/classvec3d.md) | **[getAngles](Modules/group___matrix4d.md#function-getangles)**() const |
| void | **[buildXForm](Modules/group___matrix4d.md#function-buildxform)**(const [vec3d](Classes/classvec3d.md) & pos, const [vec3d](Classes/classvec3d.md) & rot, const [vec3d](Classes/classvec3d.md) & cent_rot) |


## Functions Documentation

### function loadIdentity

```
void loadIdentity()
```


**Return**: Identity [Matrix4d](Classes/class_matrix4d.md)

Create a 4x4 identity matrix 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor
m.loadIdentity();
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor
m.loadIdentity()
```

  


### function translatef

```
void translatef(
    const double & x,
    const double & y,
    const double & z
)
```


**Parameters**: 

  * **x** Translation along the X axis 
  * **y** Translation along the Y axis 
  * **z** Translation along the Z axis 


**Return**: Translated [Matrix4d](Classes/class_matrix4d.md)

Translate the [Matrix4d](Classes/class_matrix4d.md) along the given axes values 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadIdentity();

m.translatef( 1.0, 0.0, 0.0 );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadIdentity()

m.translatef( 1.0, 0.0, 0.0 )
```

  


### function rotateX

```
void rotateX(
    const double & ang
)
```


**Parameters**: 

  * **ang** Angle of rotation (degrees) 


Rotate the [Matrix4d](Classes/class_matrix4d.md) about the X axis 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadIdentity();

m.rotateX( 90.0 );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadIdentity()

m.rotateX( 90.0 )
```

  


### function rotateY

```
void rotateY(
    const double & ang
)
```


**Parameters**: 

  * **ang** Angle of rotation (degrees) 


Rotate the [Matrix4d](Classes/class_matrix4d.md) about the Y axis 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadIdentity();

m.rotateY( 90.0 );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadIdentity()

m.rotateY( 90.0 )
```

  


### function rotateZ

```
void rotateZ(
    const double & ang
)
```


**Parameters**: 

  * **ang** Angle of rotation (degrees) 


Rotate the [Matrix4d](Classes/class_matrix4d.md) about the Z axis 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadIdentity();

m.rotateZ( 90.0 );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadIdentity()

m.rotateZ( 90.0 )
```

  


### function rotate

```
void rotate(
    const double & angle,
    const vec3d & axis
)
```


**Parameters**: 

  * **[angle](Modules/group__vec3d.md#function-angle)** Angle of rotation (rad) 
  * **axis** Vector to rotate about 


Rotate the [Matrix4d](Classes/class_matrix4d.md) about an arbitrary axis 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor
float PI = 3.14;

m.loadIdentity();

m.rotate( PI / 4, vec3d( 0.0, 0.0, 1.0 ) );      // Radians
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor
PI = 3.14

m.loadIdentity()

m.rotate( PI / 4, vec3d( 0.0, 0.0, 1.0 ) )      # Radians
```

  


### function affineInverse

```
void affineInverse()
```


Perform an affine transform on the [Matrix4d](Classes/class_matrix4d.md) 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadIdentity();

m.rotateY( 10.0 );
m.rotateX( 20.0 );
m.rotateZ( 30.0 );

vec3d c = m.xform( vec3d( 1.0, 1.0, 1.0 ) );

m.affineInverse();
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadIdentity()

m.rotateY( 10.0 )
m.rotateX( 20.0 )
m.rotateZ( 30.0 )

vec3d c = m.xform( vec3d( 1.0, 1.0, 1.0 ) )

m.affineInverse()
```

  


### function scale

```
void scale(
    const double & scale
)
```


**Parameters**: 

  * **[scale](Modules/group___matrix4d.md#function-scale)** Value to scale by 


Multiply the [Matrix4d](Classes/class_matrix4d.md) by a scalar value 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadXZRef();

m.scale( 10.0 );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadXZRef()

m.scale( 10.0 )
```

  


### function loadXZRef

```
void loadXZRef()
```


Load an identy [Matrix4d](Classes/class_matrix4d.md) and set the Y coordinate of the diagonal (index 5) to -1 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadXZRef();

vec3d b = m.xform( vec3d( 1, 2, 3 ) );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadXZRef()

vec3d b = m.xform( vec3d( 1, 2, 3 ) )
```

  


### function loadXYRef

```
void loadXYRef()
```


Load an identy [Matrix4d](Classes/class_matrix4d.md) and set the Z coordinate of the diagonal (index 10) to -1 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadXYRef();

vec3d b = m.xform( vec3d( 1, 2, 3 ) );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadXYRef()

vec3d b = m.xform( vec3d( 1, 2, 3 ) )
```

  


### function loadYZRef

```
void loadYZRef()
```


Load an identy [Matrix4d](Classes/class_matrix4d.md) and set the X coordinate of the diagonal (index 0) to -1 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadYZRef();

vec3d b = m.xform( vec3d( 1, 2, 3 ) );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadYZRef()

vec3d b = m.xform( vec3d( 1, 2, 3 ) )
```

  


### function mirrory

```
void mirrory()
```


**Parameters**: 

  * **in** Transformation vector 


Transform the [Matrix4d](Classes/class_matrix4d.md) by the given vector 

//==== Test Matrix4d ====//
Matrix4d m();                            // Default Constructor

m.loadIdentity();

vec3d a = m.xform( vec3d( 1.0, 2.0, 3.0 ) );
```

 

    #==== Test Matrix4d ====//
Matrix4d m()                            # Default Constructor

m.loadIdentity()

vec3d a = m.xform( vec3d( 1.0, 2.0, 3.0 ) )
```

  


### function getAngles

```
vec3d getAngles() const
```


**Return**: Angle measurement between each axis (degrees) 

Calculate the [Matrix4d](Classes/class_matrix4d.md)'s angles between the X, Y and Z axes 

Matrix4d mat;
float PI = 3.14;

mat.loadIdentity();

m.rotate( PI / 4, vec3d( 0.0, 0.0, 1.0 ) );      // Radians

vec3d angles = mat.getAngles();
```

 

    Matrix4d mat
PI = 3.14

mat.loadIdentity()

m.rotate( PI / 4, vec3d( 0.0, 0.0, 1.0 ) )      # Radians

vec3d angles = mat.getAngles()
```

  


### function buildXForm

```
void buildXForm(
    const vec3d & pos,
    const vec3d & rot,
    const vec3d & cent_rot
)
```


**Parameters**: 

  * **pos** Position to translate to 
  * **rot** Angle of rotation (degrees) 
  * **cent_rot** Center of rotation 


Translate the [Matrix4d](Classes/class_matrix4d.md) to a given position and rotate it a about a given center of rotation 






-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800