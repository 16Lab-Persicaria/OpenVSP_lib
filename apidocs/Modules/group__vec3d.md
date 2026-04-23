---
title: Vec3D Functions
summary: API functions that utilize the vec3d class are grouped here. For details of the class, including member functions, see vec3d. Click here to return to the main page. 

---

# Vec3D Functions

API functions that utilize the [vec3d](Classes/classvec3d.md) class are grouped here. For details of the class, including member functions, see [vec3d](Classes/classvec3d.md). Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| [vec3d](Classes/classvec3d.md) | **[operator+](Modules/group__vec3d.md#function-operator+)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| [vec3d](Classes/classvec3d.md) | **[operator-](Modules/group__vec3d.md#function-operator-)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| [vec3d](Classes/classvec3d.md) | **[operator*](Modules/group__vec3d.md#function-operator*)**(const [vec3d](Classes/classvec3d.md) & a, double b) |
| [vec3d](Classes/classvec3d.md) | **[operator*](Modules/group__vec3d.md#function-operator*)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| [vec3d](Classes/classvec3d.md) | **[operator/](Modules/group__vec3d.md#function-operator/)**(const [vec3d](Classes/classvec3d.md) & a, double b) |
| double | **[dist](Modules/group__vec3d.md#function-dist)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| double | **[dist_squared](Modules/group__vec3d.md#function-dist-squared)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| double | **[dot](Modules/group__vec3d.md#function-dot)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| [vec3d](Classes/classvec3d.md) | **[cross](Modules/group__vec3d.md#function-cross)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| double | **[angle](Modules/group__vec3d.md#function-angle)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| double | **[signed_angle](Modules/group__vec3d.md#function-signed-angle)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b, const [vec3d](Classes/classvec3d.md) & ref) |
| double | **[cos_angle](Modules/group__vec3d.md#function-cos-angle)**(const [vec3d](Classes/classvec3d.md) & a, const [vec3d](Classes/classvec3d.md) & b) |
| [vec3d](Classes/classvec3d.md) | **[RotateArbAxis](Modules/group__vec3d.md#function-rotatearbaxis)**(const [vec3d](Classes/classvec3d.md) & p, double theta, const [vec3d](Classes/classvec3d.md) & r) |


## Functions Documentation

### function operator+

```
vec3d operator+(
    const vec3d & a,
    const vec3d & b
)
```


Addition operator for two [vec3d](Classes/classvec3d.md) objects, performed by the addition of each corresponding component 

vec3d a(), b();                                // Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 );
b.set_xyz( 4.0, 5.0, 6.0 );

vec3d c = a + b;

Print( "a + b = ", false );

Print( c );
```

 

    vec3d a(), b()                                # Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 )
b.set_xyz( 4.0, 5.0, 6.0 )

vec3d c = a + b

Print( "a + b = ", False )

Print( c )
```

  


### function operator-

```
vec3d operator-(
    const vec3d & a,
    const vec3d & b
)
```


\forcpponly Subtraction operator for two [vec3d](Classes/classvec3d.md) objects, performed by the subtraction of each corresponding component ```cpp

\forcpponly
\code{.cpp}
vec3d a(), b();                                // Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 );
b.set_xyz( 4.0, 5.0, 6.0 );

vec3d c = a - b;

Print( "a - b = ", false );

Print( c );
```

 

    vec3d a(), b()                                # Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 )
b.set_xyz( 4.0, 5.0, 6.0 )

vec3d c = a - b

Print( "a - b = ", False )

Print( c )
```

  


### function operator*

```
vec3d operator*(
    const vec3d & a,
    double b
)
```


Scalar multiplication operator for a [vec3d](Classes/classvec3d.md), performed by the multiplication of each [vec3d](Classes/classvec3d.md) component and the scalar 

vec3d a();                                // Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 );

double b = 1.5;

vec3d c = a * b;

Print( "a * b = ", false );

Print( c );
```

 

    vec3d a()                                # Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 )

b = 1.5

vec3d c = a * b

Print( "a * b = ", False )

Print( c )
```

  


### function operator*

```
vec3d operator*(
    const vec3d & a,
    const vec3d & b
)
```


Scalar multiplication operator for a [vec3d](Classes/classvec3d.md), performed by the multiplication of each [vec3d](Classes/classvec3d.md) component and the scalar 

vec3d a();                                // Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 );

double b = 1.5;

vec3d c = a * b;

Print( "a * b = ", false );

Print( c );
```

 

    vec3d a()                                # Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 )

b = 1.5

vec3d c = a * b

Print( "a * b = ", False )

Print( c )
```

  


### function operator/

```
vec3d operator/(
    const vec3d & a,
    double b
)
```


Scalar division operator for a [vec3d](Classes/classvec3d.md), performed by the division of of each [vec3d](Classes/classvec3d.md) component by the scalar 

vec3d a();                                // Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 );

double b = 1.5;

vec3d c = a / b;

Print( "a / b = ", false );

Print( c );
```

 

    vec3d a()                                # Default Constructor

a.set_xyz( 1.0, 2.0, 3.0 )

b = 1.5

vec3d c = a / b

Print( "a / b = ", False )

Print( c )
```

  


### function dist

```
double dist(
    const vec3d & a,
    const vec3d & b
)
```


**Parameters**: 

  * **a** First [vec3d](Classes/classvec3d.md)
  * **b** Second [vec3d](Classes/classvec3d.md)


**See**: [dist_squared](Modules/group__vec3d.md#function-dist-squared)

**Return**: Distance 

Calculate the distance between two [vec3d](Classes/classvec3d.md) inputs 

//==== Test Vec3d ====//
vec3d a(), b();                                // Default Constructor

//==== Test Dist ====//
a.set_xyz( 2.0, 2.0, 2.0 );
b.set_xyz( 3.0, 4.0, 5.0 );

double d = dist( a, b );

if ( abs( d - sqrt( 14 ) ) > 1e-6 )    { Print( "---> Error: Vec3d Dist " ); }
```

 

import math
#==== Test Vec3d ====//
vec3d a(), b()                                # Default Constructor

#==== Test Dist ====//
a.set_xyz( 2.0, 2.0, 2.0 )
b.set_xyz( 3.0, 4.0, 5.0 )

d = dist( a; b )

if  abs( d - math.sqrt( 14 ) ) > 1e-6 : Print( "---> Error: Vec3d Dist " ); }
```

  


### function dist_squared

```
double dist_squared(
    const vec3d & a,
    const vec3d & b
)
```


**Parameters**: 

  * **a** First [vec3d](Classes/classvec3d.md)
  * **b** Second [vec3d](Classes/classvec3d.md)


**See**: [dist](Modules/group__vec3d.md#function-dist)

**Return**: Distance squared 

Calculate distance squared between two [vec3d](Classes/classvec3d.md) inputs 

//==== Test Vec3d ====//
vec3d a(), b();                                // Default Constructor

//==== Test Dist ====//
a.set_xyz( 2.0, 2.0, 2.0 );
b.set_xyz( 3.0, 4.0, 5.0 );

double d2 = dist_squared( a, b );

if ( abs( d2 - 14 ) > 1e-6 )    { Print( "---> Error: Vec3d Dist " ); }
```

 

    #==== Test Vec3d ====//
vec3d a(), b()                                # Default Constructor

#==== Test Dist ====//
a.set_xyz( 2.0, 2.0, 2.0 )
b.set_xyz( 3.0, 4.0, 5.0 )

d2 = dist_squared( a; b )

if  abs( d2 - 14 ) > 1e-6 : Print( "---> Error: Vec3d Dist " ); }
```

  


### function dot

```
double dot(
    const vec3d & a,
    const vec3d & b
)
```


**Parameters**: 

  * **a** First [vec3d](Classes/classvec3d.md)
  * **b** Second [vec3d](Classes/classvec3d.md)


**Return**: Dot product 

Calculate the dot product between two [vec3d](Classes/classvec3d.md) inputs 

//==== Test Vec3d ====//
vec3d a(), b();                                // Default Constructor

//==== Test Dot ====//
a.set_xyz( 1.0, 2.0, 3.0 );
b.set_xyz( 2.0, 3.0, 4.0 );

if ( abs( dot( a, b ) - 20 ) > 1e-6 )                            { Print( "---> Error: Vec3d Dot " ); }
```

 

    #==== Test Vec3d ====//
vec3d a(), b()                                # Default Constructor

#==== Test Dot ====//
a.set_xyz( 1.0, 2.0, 3.0 )
b.set_xyz( 2.0, 3.0, 4.0 )

if  abs( dot( a, b ) - 20 ) > 1e-6 : Print( "---> Error: Vec3d Dot " ); }
```

  


### function cross

```
vec3d cross(
    const vec3d & a,
    const vec3d & b
)
```


**Parameters**: 

  * **a** First [vec3d](Classes/classvec3d.md)
  * **b** Second [vec3d](Classes/classvec3d.md)


**Return**: Cross product 

Calculate the cross product between two [vec3d](Classes/classvec3d.md) inputs 

//==== Test Vec3d ====//
vec3d a(), b(), c();                                // Default Constructor

//==== Test Cross ====//
a.set_xyz( 4.0, 0.0, 0.0 );
b.set_xyz( 0.0, 3.0, 0.0 );

c = cross( a, b );

c.normalize();
```

 

    #==== Test Vec3d ====//
vec3d a(), b(), c()                                # Default Constructor

#==== Test Cross ====//
a.set_xyz( 4.0, 0.0, 0.0 )
b.set_xyz( 0.0, 3.0, 0.0 )

c = cross( a, b )

c.normalize()
```

  


### function angle

```
double angle(
    const vec3d & a,
    const vec3d & b
)
```


**Parameters**: 

  * **a** First [vec3d](Classes/classvec3d.md)
  * **b** Second [vec3d](Classes/classvec3d.md)


**Return**: Angle in Radians 

Calculate the angle between two [vec3d](Classes/classvec3d.md) inputs (dot product divided by their magnitudes multiplied) 

//==== Test Vec3d ====//
vec3d a(), b();                                // Default Constructor
float PI = 3.14159265359;

//==== Test Angle ====//
a.set_xyz( 1.0, 1.0, 0.0 );
b.set_xyz( 1.0, 0.0, 0.0 );

if ( abs( angle( a, b ) - PI / 4 ) > 1e-6 )                    { Print( "---> Error: Vec3d Angle " ); }
```

 

    #==== Test Vec3d ====//
vec3d a(), b()                                # Default Constructor
PI = 3.14159265359

#==== Test Angle ====//
a.set_xyz( 1.0, 1.0, 0.0 )
b.set_xyz( 1.0, 0.0, 0.0 )

if  abs( angle( a, b ) - PI / 4 ) > 1e-6 : Print( "---> Error: Vec3d Angle " ); }
```

  


### function signed_angle

```
double signed_angle(
    const vec3d & a,
    const vec3d & b,
    const vec3d & ref
)
```


**Parameters**: 

  * **a** First [vec3d](Classes/classvec3d.md)
  * **b** Second [vec3d](Classes/classvec3d.md)
  * **ref** Reference axis 


**Return**: Angle in Radians 

Calculate the signed angle between two [vec3d](Classes/classvec3d.md) inputs (dot product divided by their magnitudes multiplied) and an input reference axis 

//==== Test Vec3d ====//
vec3d a(), b(), c();                                // Default Constructor
float PI = 3.14159265359;

//==== Test Angle ====//
a.set_xyz( 1.0, 1.0, 0.0 );
b.set_xyz( 1.0, 0.0, 0.0 );
c.set_xyz( 0.0, 0.0, 1.0 );

if ( abs( signed_angle( a, b, c ) - -PI / 4 ) > 1e-6 )            { Print( "---> Error: Vec3d SignedAngle " ); }
```

 

    #==== Test Vec3d ====//
vec3d a(), b(), c()                                # Default Constructor
PI = 3.14159265359

#==== Test Angle ====//
a.set_xyz( 1.0, 1.0, 0.0 )
b.set_xyz( 1.0, 0.0, 0.0 )
c.set_xyz( 0.0, 0.0, 1.0 )

if  abs( signed_angle( a, b, c ) - -PI / 4 ) > 1e-6 : Print( "---> Error: Vec3d SignedAngle " ); }
```

  


### function cos_angle

```
double cos_angle(
    const vec3d & a,
    const vec3d & b
)
```


**Parameters**: 

  * **a** First [vec3d](Classes/classvec3d.md)
  * **b** Second [vec3d](Classes/classvec3d.md)


**See**: [angle](Modules/group__vec3d.md#function-angle)

**Return**: Angle in Radians 

Calculate the cosine of angle between two [vec3d](Classes/classvec3d.md) inputs 

vec3d pnt = vec3d( 2, 4, 6);

vec3d line_pt1(), line_pt2();

line_pt1.set_z( 4 );
line_pt2.set_y( 3 );

vec3d p_ln1 = pnt - line_pt1;

vec3d ln2_ln1 = line_pt2 - line_pt1;

double numer =  cos_angle( p_ln1, ln2_ln1 ) * p_ln1.mag();
```

 

    vec3d pnt = vec3d( 2, 4, 6)

vec3d line_pt1(), line_pt2()

line_pt1.set_z( 4 )
line_pt2.set_y( 3 )

vec3d p_ln1 = pnt - line_pt1

vec3d ln2_ln1 = line_pt2 - line_pt1

numer =  cos_angle( p_ln1; ln2_ln1 ) * p_ln1.mag()
```

  


### function RotateArbAxis

```
vec3d RotateArbAxis(
    const vec3d & p,
    double theta,
    const vec3d & r
)
```


**Parameters**: 

  * **p** Coordinate point to rotate 
  * **theta** Angle of rotation in Radians 
  * **r** Reference axis for rotation 


**Return**: Coordinates of rotated point 

Rotate a input point by specified angle around an arbitrary axis. Assume right hand coordinate system 

//==== Test Vec3d ====//
vec3d a(), b(), c();                                // Default Constructor
float PI = 3.14;

//==== Test Rotate ====//
a.set_xyz( 1.0, 1.0, 0.0 );
b.set_xyz( 1.0, 0.0, 0.0 );
c.set_xyz( 0.0, 0.0, 1.0 );

c = RotateArbAxis( b, PI, a );
```

 

    #==== Test Vec3d ====//
vec3d a(), b(), c()                                # Default Constructor
PI = 3.14

#==== Test Rotate ====//
a.set_xyz( 1.0, 1.0, 0.0 )
b.set_xyz( 1.0, 0.0, 0.0 )
c.set_xyz( 0.0, 0.0, 1.0 )

c = RotateArbAxis( b, PI, a )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800