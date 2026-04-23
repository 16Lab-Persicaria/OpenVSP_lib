---
title: Geom Surface Query Functions
summary: This group of API functions pertains to general surface queries for Geom surfaces, such as computing 3D location from surface coordinates, identifying curvature, and performing point projections. Click here to return to the main page. 

---

# Geom Surface Query Functions

This group of API functions pertains to general surface queries for Geom surfaces, such as computing 3D location from surface coordinates, identifying curvature, and performing point projections. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| [vec3d](Classes/classvec3d.md) | **[CompPnt01](Modules/group___surface_query.md#function-comppnt01)**(const std::string & geom_id, const int & surf_indx, const double & u, const double & w) |
| [vec3d](Classes/classvec3d.md) | **[CompNorm01](Modules/group___surface_query.md#function-compnorm01)**(const std::string & geom_id, const int & surf_indx, const double & u, const double & w) |
| [vec3d](Classes/classvec3d.md) | **[CompTanU01](Modules/group___surface_query.md#function-comptanu01)**(const std::string & geom_id, const int & surf_indx, const double & u, const double & w) |
| [vec3d](Classes/classvec3d.md) | **[CompTanW01](Modules/group___surface_query.md#function-comptanw01)**(const std::string & geom_id, const int & surf_indx, const double & u, const double & w) |
| void | **[CompCurvature01](Modules/group___surface_query.md#function-compcurvature01)**(const std::string & geom_id, const int & surf_indx, const double & u, const double & w, double & k1_out, double & k2_out, double & ka_out, double & kg_out) |
| double | **[ProjPnt01](Modules/group___surface_query.md#function-projpnt01)**(const std::string & geom_id, const int & surf_indx, const [vec3d](Classes/classvec3d.md) & pt, double & u_out, double & w_out) |
| double | **[ProjPnt01I](Modules/group___surface_query.md#function-projpnt01i)**(const std::string & geom_id, const [vec3d](Classes/classvec3d.md) & pt, int & surf_indx_out, double & u_out, double & w_out) |
| double | **[ProjPnt01Guess](Modules/group___surface_query.md#function-projpnt01guess)**(const std::string & geom_id, const int & surf_indx, const [vec3d](Classes/classvec3d.md) & pt, const double & u0, const double & w0, double & u_out, double & w_out) |
| double | **[AxisProjPnt01](Modules/group___surface_query.md#function-axisprojpnt01)**(const std::string & geom_id, const int & surf_indx, const int & iaxis, const [vec3d](Classes/classvec3d.md) & pt, double & u_out, double & w_out) |
| double | **[AxisProjPnt01I](Modules/group___surface_query.md#function-axisprojpnt01i)**(const std::string & geom_id, const int & iaxis, const [vec3d](Classes/classvec3d.md) & pt, int & surf_indx_out, double & u_out, double & w_out) |
| double | **[AxisProjPnt01Guess](Modules/group___surface_query.md#function-axisprojpnt01guess)**(const std::string & geom_id, const int & surf_indx, const int & iaxis, const [vec3d](Classes/classvec3d.md) & pt, const double & u0, const double & w0, double & u_out, double & w_out) |
| bool | **[InsideSurf](Modules/group___surface_query.md#function-insidesurf)**(const std::string & geom_id, const int & surf_indx, const [vec3d](Classes/classvec3d.md) & pt) |
| [vec3d](Classes/classvec3d.md) | **[CompPntRST](Modules/group___surface_query.md#function-comppntrst)**(const std::string & geom_id, const int & surf_indx, const double & r, const double & s, const double & t) |
| double | **[FindRST](Modules/group___surface_query.md#function-findrst)**(const std::string & geom_id, const int & surf_indx, const [vec3d](Classes/classvec3d.md) & pt, double & r_out, double & s_out, double & t_out) |
| double | **[FindRSTGuess](Modules/group___surface_query.md#function-findrstguess)**(const std::string & geom_id, const int & surf_indx, const [vec3d](Classes/classvec3d.md) & pt, const double & r0, const double & s0, const double & t0, double & r_out, double & s_out, double & t_out) |
| void | **[ConvertRSTtoLMN](Modules/group___surface_query.md#function-convertrsttolmn)**(const std::string & geom_id, const int & surf_indx, const double & r, const double & s, const double & t, double & l_out, double & m_out, double & n_out) |
| void | **[ConvertRtoL](Modules/group___surface_query.md#function-convertrtol)**(const std::string & geom_id, const int & surf_indx, const double & r, double & l_out) |
| void | **[ConvertLMNtoRST](Modules/group___surface_query.md#function-convertlmntorst)**(const std::string & geom_id, const int & surf_indx, const double & l, const double & m, const double & n, double & r_out, double & s_out, double & t_out) |
| void | **[ConvertLtoR](Modules/group___surface_query.md#function-convertltor)**(const std::string & geom_id, const int & surf_indx, const double & l, double & r_out) |
| void | **[ConvertUtoEta](Modules/group___surface_query.md#function-convertutoeta)**(const std::string & geom_id, const double & u, double & eta_out) |
| void | **[ConvertEtatoU](Modules/group___surface_query.md#function-convertetatou)**(const std::string & geom_id, const double & eta, double & u_out) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[CompVecPnt01](Modules/group___surface_query.md#function-compvecpnt01)**(const std::string & geom_id, const int & surf_indx, const std::vector< double > & u_in_vec, const std::vector< double > & w_in_vec) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[CompVecDegenPnt01](Modules/group___surface_query.md#function-compvecdegenpnt01)**(const std::string & geom_id, const int & surf_indx, const int & degen_type, const std::vector< double > & u_in_vec, const std::vector< double > & w_in_vec) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[CompVecNorm01](Modules/group___surface_query.md#function-compvecnorm01)**(const std::string & geom_id, const int & surf_indx, const std::vector< double > & us, const std::vector< double > & ws) |
| void | **[CompVecCurvature01](Modules/group___surface_query.md#function-compveccurvature01)**(const std::string & geom_id, const int & surf_indx, const std::vector< double > & us, const std::vector< double > & ws, std::vector< double > & k1_out_vec, std::vector< double > & k2_out_vec, std::vector< double > & ka_out_vec, std::vector< double > & kg_out_vec) |
| void | **[ProjVecPnt01](Modules/group___surface_query.md#function-projvecpnt01)**(const std::string & geom_id, const int & surf_indx, const std::vector< [vec3d](Classes/classvec3d.md) > & pts, std::vector< double > & u_out_vec, std::vector< double > & w_out_vec, std::vector< double > & d_out_vec) |
| void | **[ProjVecPnt01Guess](Modules/group___surface_query.md#function-projvecpnt01guess)**(const std::string & geom_id, const int & surf_indx, const std::vector< [vec3d](Classes/classvec3d.md) > & pts, const std::vector< double > & u0s, const std::vector< double > & w0s, std::vector< double > & u_out_vec, std::vector< double > & w_out_vec, std::vector< double > & d_out_vec) |
| void | **[AxisProjVecPnt01](Modules/group___surface_query.md#function-axisprojvecpnt01)**(const std::string & geom_id, const int & surf_indx, const int & iaxis, const std::vector< [vec3d](Classes/classvec3d.md) > & pts, std::vector< double > & u_out_vec, std::vector< double > & w_out_vec, std::vector< double > & d_out_vec) |
| void | **[AxisProjVecPnt01Guess](Modules/group___surface_query.md#function-axisprojvecpnt01guess)**(const std::string & geom_id, const int & surf_indx, const int & iaxis, const std::vector< [vec3d](Classes/classvec3d.md) > & pts, const std::vector< double > & u0s, const std::vector< double > & w0s, std::vector< double > & u_out_vec, std::vector< double > & w_out_vec, std::vector< double > & d_out_vec) |
| std::vector< bool > | **[VecInsideSurf](Modules/group___surface_query.md#function-vecinsidesurf)**(const std::string & geom_id, const int & surf_indx, const std::vector< [vec3d](Classes/classvec3d.md) > & pts) |
| std::vector< [vec3d](Classes/classvec3d.md) > | **[CompVecPntRST](Modules/group___surface_query.md#function-compvecpntrst)**(const std::string & geom_id, const int & surf_indx, const std::vector< double > & r_in_vec, const std::vector< double > & s_in_vec, const std::vector< double > & t_in_vec) |
| void | **[FindRSTVec](Modules/group___surface_query.md#function-findrstvec)**(const std::string & geom_id, const int & surf_indx, const std::vector< [vec3d](Classes/classvec3d.md) > & pts, std::vector< double > & r_out_vec, std::vector< double > & s_out_vec, std::vector< double > & t_out_vec, std::vector< double > & d_out_vec) |
| void | **[FindRSTVecGuess](Modules/group___surface_query.md#function-findrstvecguess)**(const std::string & geom_id, const int & surf_indx, const std::vector< [vec3d](Classes/classvec3d.md) > & pts, const std::vector< double > & r0s, const std::vector< double > & s0s, const std::vector< double > & t0s, std::vector< double > & r_out_vec, std::vector< double > & s_out_vec, std::vector< double > & t_out_vec, std::vector< double > & d_out_vec) |
| void | **[ConvertRSTtoLMNVec](Modules/group___surface_query.md#function-convertrsttolmnvec)**(const std::string & geom_id, const int & surf_indx, const std::vector< double > & r_vec, const std::vector< double > & s_vec, const std::vector< double > & t_vec, std::vector< double > & l_out_vec, std::vector< double > & m_out_vec, std::vector< double > & n_out_vec) |
| void | **[ConvertLMNtoRSTVec](Modules/group___surface_query.md#function-convertlmntorstvec)**(const std::string & geom_id, const int & surf_indx, const std::vector< double > & l_vec, const std::vector< double > & m_vec, const std::vector< double > & n_vec, std::vector< double > & r_out_vec, std::vector< double > & s_out_vec, std::vector< double > & t_out_vec) |
| void | **[GetUWTess01](Modules/group___surface_query.md#function-getuwtess01)**(const std::string & geom_id, const int & surf_indx, std::vector< double > & u_out_vec, std::vector< double > & w_out_vec) |


## Functions Documentation

### function CompPnt01

```
vec3d CompPnt01(
    const std::string & geom_id,
    const int & surf_indx,
    const double & u,
    const double & w
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **u** U (0 - 1) surface coordinate 
  * **w** W (0 - 1) surface coordinate 


**Return**: Normal vector3D coordinate point 

Calculate the 3D coordinate equivalent for the input surface coordinate point 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

vec3d pnt = CompPnt01( geom_id, surf_indx, u, w );

Print( "Point: ( " + pnt.x() + ', ' + pnt.y() + ', ' + pnt.z() + ' )' );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

pnt = CompPnt01( geom_id, surf_indx, u, w )

print( f"Point: ( {pnt.x()}, {pnt.y()}, {pnt.z()} )" )
```

  


### function CompNorm01

```
vec3d CompNorm01(
    const std::string & geom_id,
    const int & surf_indx,
    const double & u,
    const double & w
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **u** U (0 - 1) surface coordinate 
  * **w** W (0 - 1) surface coordinate 


**Return**: Normal vector 

Calculate the normal vector on the specified surface at input surface coordinate 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

vec3d norm = CompNorm01( geom_id, surf_indx, u, w );

Print( "Point: ( " + norm.x() + ', ' + norm.y() + ', ' + norm.z() + ' )' );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

norm = CompNorm01( geom_id, surf_indx, u, w )

print( "Point: ( {norm.x()}, {norm.y()}, {norm.z()} )" )
```

  


### function CompTanU01

```
vec3d CompTanU01(
    const std::string & geom_id,
    const int & surf_indx,
    const double & u,
    const double & w
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **u** U (0 - 1) surface coordinate 
  * **w** W (0 - 1) surface coordinate 


**Return**: Tangent vector in U direction 

Calculate the vector tangent to the specified surface at input surface coordinate in the U direction 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

vec3d tanu = CompTanU01( geom_id, surf_indx, u, w );

Print( "Point: ( " + tanu.x() + ', ' + tanu.y() + ', ' + tanu.z() + ' )' );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

tanu = CompTanU01( geom_id, surf_indx, u, w )

print( f"Point: ( {tanu.x()}, {tanu.y()}, {tanu.z()} )" )
```

  


### function CompTanW01

```
vec3d CompTanW01(
    const std::string & geom_id,
    const int & surf_indx,
    const double & u,
    const double & w
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **u** U (0 - 1) surface coordinate 
  * **w** W (0 - 1) surface coordinate 


**Return**: Tangent vector in W direction 

Calculate the vector tangent to the specified surface at input surface coordinate in the W direction 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

vec3d tanw = CompTanW01( geom_id, surf_indx, u, w );

Print( "Point: ( " + tanw.x() + ', ' + tanw.y() + ', ' + tanw.z() + ' )' );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

tanw = CompTanW01( geom_id, surf_indx, u, w )

print( f"Point: ( {tanw.x()}, {tanw.y()}, {tanw.z()} )" )
```

  


### function CompCurvature01

```
void CompCurvature01(
    const std::string & geom_id,
    const int & surf_indx,
    const double & u,
    const double & w,
    double & k1_out,
    double & k2_out,
    double & ka_out,
    double & kg_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **u** double U (0 - 1) surface coordinate 
  * **w** double W (0 - 1) surface coordinate 
  * **k1_out** double Output value of maximum principal curvature 
  * **k2_out** double Output value of minimum principal curvature 
  * **ka_out** double Output value of mean curvature 
  * **kg_out** double Output value of Gaussian curvature 


Determine the curvature of a specified surface at the input surface coordinate point 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double k1, k2, ka, kg;

double u, w;
u = 0.25;
w = 0.75;

CompCurvature01( geom_id, surf_indx, u, w, k1, k2, ka, kg );

Print( "Curvature : k1 " + k1 + " k2 " + k2 + " ka " + ka + " kg " + kg );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0


u = 0.25
w = 0.75

k1, k2, ka, kg = CompCurvature01( geom_id, surf_indx, u, w )

print( f"Curvature : k1 {k1} k2 {k2} ka {ka} kg {kg}" )
```

  


### function ProjPnt01

```
double ProjPnt01(
    const std::string & geom_id,
    const int & surf_indx,
    const vec3d & pt,
    double & u_out,
    double & w_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pt** [vec3d](Classes/classvec3d.md) Input 3D coordinate point 
  * **u_out** double Output closest U (0 - 1) surface coordinate 
  * **w_out** double Output closest W (0 - 1) surface coordinate 


**See**: [ProjPnt01Guess](Modules/group___surface_query.md#function-projpnt01guess), [ProjPnt01I](Modules/group___surface_query.md#function-projpnt01i)

**Return**: double Distance between the 3D point and the closest point of the surface 

Determine the nearest surface coordinate for an input 3D coordinate point and calculate the distance between the 3D point and the closest point of the surface. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

vec3d pnt = CompPnt01( geom_id, surf_indx, u, w );

vec3d norm = CompNorm01( geom_id, surf_indx, u, w );

double uout, wout;

// Offset point from surface
pnt = pnt + norm;

double d = ProjPnt01( geom_id, surf_indx, pnt, uout, wout );

Print( "Dist " + d + " u " + uout + " w " + wout );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

pnt = CompPnt01( geom_id, surf_indx, u, w )

norm = CompNorm01( geom_id, surf_indx, u, w )


# Offset point from surface
pnt.set_xyz( pnt.x() + norm.x(), pnt.y() + norm.y(), pnt.z() + norm.z() )

d, uout, wout = ProjPnt01( geom_id, surf_indx, pnt )

print( f"Dist {d} u {uout} w {wout}" )
```

  


### function ProjPnt01I

```
double ProjPnt01I(
    const std::string & geom_id,
    const vec3d & pt,
    int & surf_indx_out,
    double & u_out,
    double & w_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **pt** [vec3d](Classes/classvec3d.md) Input 3D coordinate point 
  * **surf_indx_out** int Output main surface index from the parent Geom 
  * **u_out** double Output closest U (0 - 1) surface coordinat 
  * **w_out** double Output closest W (0 - 1) surface coordinat 


**See**: [ProjPnt01](Modules/group___surface_query.md#function-projpnt01), [ProjPnt01Guess](Modules/group___surface_query.md#function-projpnt01guess)

**Return**: double Distance between the 3D point and the closest point of the surface 

Determine the nearest surface coordinate and corresponding parent Geom main surface index for an input 3D coordinate point. Return the distance between the closest point and the input. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

double d = 0;

vec3d pnt = CompPnt01( geom_id, surf_indx, u, w );

vec3d norm = CompNorm01( geom_id, surf_indx, u, w );

double uout, wout;

int surf_indx_out;

// Offset point from surface
pnt = pnt + norm;

d = ProjPnt01I( geom_id, pnt, surf_indx_out, uout, wout );

Print( "Dist " + d + " u " + uout + " w " + wout + " surf_index " + surf_indx_out );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

d = 0

pnt = CompPnt01( geom_id, surf_indx, u, w )

norm = CompNorm01( geom_id, surf_indx, u, w )



# Offset point from surface
pnt.set_xyz( pnt.x() + norm.x(), pnt.y() + norm.y(), pnt.z() + norm.z() )

d, surf_indx_out, uout, wout = ProjPnt01I( geom_id, pnt )

print( f"Dist {d} u {uout} w {wout} surf_index {surf_indx_out}" )
```

  


### function ProjPnt01Guess

```
double ProjPnt01Guess(
    const std::string & geom_id,
    const int & surf_indx,
    const vec3d & pt,
    const double & u0,
    const double & w0,
    double & u_out,
    double & w_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pt** [vec3d](Classes/classvec3d.md) Input 3D coordinate point 
  * **u0** double Input U (0 - 1) surface coordinate guess 
  * **w0** double Input W (0 - 1) surface coordinate guess 
  * **u_out** double Output closest U (0 - 1) surface coordinate 
  * **w_out** double Output closest W (0 - 1) surface coordinate 


**See**: [ProjPnt01](Modules/group___surface_query.md#function-projpnt01), [ProjPnt01I](Modules/group___surface_query.md#function-projpnt01i)

**Return**: double Distance between the 3D point and the closest point of the surface 

Determine the nearest surface coordinate for an input 3D coordinate point and calculate the distance between the 3D point and the closest point of the surface. This function takes an input surface coordinate guess for, offering a potential decrease in computation time compared to ProjPnt01. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

double d = 0;

vec3d pnt = CompPnt01( geom_id, surf_indx, u, w );

vec3d norm = CompNorm01( geom_id, surf_indx, u, w );

double uout, wout;

// Offset point from surface
pnt = pnt + norm;

d = ProjPnt01Guess( geom_id, surf_indx, pnt, u + 0.1, w + 0.1, uout, wout );

Print( "Dist " + d + " u " + uout + " w " + wout );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

d = 0

pnt = CompPnt01( geom_id, surf_indx, u, w )

norm = CompNorm01( geom_id, surf_indx, u, w )


# Offset point from surface
pnt.set_xyz( pnt.x() + norm.x(), pnt.y() + norm.y(), pnt.z() + norm.z() )

d, uout, wout = ProjPnt01Guess( geom_id, surf_indx, pnt, u + 0.1, w + 0.1 )

print( f"Dist {d} u {uout} w {wout}" )
```

  


### function AxisProjPnt01

```
double AxisProjPnt01(
    const std::string & geom_id,
    const int & surf_indx,
    const int & iaxis,
    const vec3d & pt,
    double & u_out,
    double & w_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **iaxis** int Axis direction to project point along (X_DIR, Y_DIR, or Z_DIR) 
  * **pt** Input 3D coordinate point 
  * **u_out** Output closest U (0 - 1) surface coordinate 
  * **w_out** Output closest W (0 - 1) surface coordinate 


**See**: [AxisProjPnt01Guess](Modules/group___surface_query.md#function-axisprojpnt01guess), [AxisProjPnt01I](Modules/group___surface_query.md#function-axisprojpnt01i), [AxisProjVecPnt01](Modules/group___surface_query.md#function-axisprojvecpnt01), [AxisProjVecPnt01Guess](Modules/group___surface_query.md#function-axisprojvecpnt01guess)

**Return**: Axis aligned distance between the 3D point and the projected point on the surface 

Project an input 3D coordinate point onto a surface along a specified axis. If the axis-aligned ray from the point intersects the surface multiple times, the nearest intersection is returned. If the axis-aligned ray from the point does not intersect the surface, the original point is returned and -1 is returned in the other output parameters.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

vec3d surf_pt = CompPnt01( geom_id, surf_indx, u, w );
vec3d pt = surf_pt;

pt.offset_y( -5.0 );

double u_out, w_out;

double idist = AxisProjPnt01( geom_id, surf_indx, Y_DIR, pt, u_out, w_out);

Print( "iDist " + idist + " u_out " + u_out + " w_out " + w_out );
Print( "3D Offset ", false);
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

surf_pt = CompPnt01( geom_id, surf_indx, u, w )
pt = surf_pt

pt.offset_y( -5.0 )

idist, u_out, w_out = AxisProjPnt01( geom_id, surf_indx, Y_DIR, pt )

print( f"iDist {idist} u_out {u_out} w_out {w_out}" )
print( "3D Offset ", False)
```

  


### function AxisProjPnt01I

```
double AxisProjPnt01I(
    const std::string & geom_id,
    const int & iaxis,
    const vec3d & pt,
    int & surf_indx_out,
    double & u_out,
    double & w_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **iaxis** int Axis direction to project point along (X_DIR, Y_DIR, or Z_DIR) 
  * **pt** Input 3D coordinate point 
  * **surf_indx_out** Output main surface index from the parent Geom 
  * **u_out** Output closest U (0 - 1) surface coordinate 
  * **w_out** Output closest W (0 - 1) surface coordinate 


**See**: [AxisProjPnt01](Modules/group___surface_query.md#function-axisprojpnt01), [AxisProjPnt01Guess](Modules/group___surface_query.md#function-axisprojpnt01guess), [AxisProjVecPnt01](Modules/group___surface_query.md#function-axisprojvecpnt01), [AxisProjVecPnt01Guess](Modules/group___surface_query.md#function-axisprojvecpnt01guess)

**Return**: Axis aligned distance between the 3D point and the projected point on the surface 

Project an input 3D coordinate point onto a Geom along a specified axis. The intersecting surface index is also returned. If the axis-aligned ray from the point intersects the Geom multiple times, the nearest intersection is returned. If the axis-aligned ray from the point does not intersect the Geom, the original point is returned and -1 is returned in the other output parameters.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;

vec3d surf_pt = CompPnt01( geom_id, surf_indx, u, w );
vec3d pt = surf_pt;

pt.offset_y( -5.0 );

double u_out, w_out;
int surf_indx_out;

double idist = AxisProjPnt01I( geom_id, Y_DIR, pt, surf_indx_out, u_out, w_out);

Print( "iDist " + idist + " u_out " + u_out + " w_out " + w_out + " surf_index " + surf_indx_out );
Print( "3D Offset ", false);
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890

surf_pt = CompPnt01( geom_id, surf_indx, u, w )
pt = surf_pt

pt.offset_y( -5.0 )


idist, surf_indx_out, u_out, w_out = AxisProjPnt01I( geom_id, Y_DIR, pt )

print( "iDist {idist} u_out {u_out} w_out {w_out} surf_index {surf_indx_out}" )
print( "3D Offset ", False)
```

  


### function AxisProjPnt01Guess

```
double AxisProjPnt01Guess(
    const std::string & geom_id,
    const int & surf_indx,
    const int & iaxis,
    const vec3d & pt,
    const double & u0,
    const double & w0,
    double & u_out,
    double & w_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **iaxis** int Axis direction to project point along (X_DIR, Y_DIR, or Z_DIR) 
  * **pt** Input 3D coordinate point 
  * **u0** Input U (0 - 1) surface coordinate guess 
  * **w0** Input W (0 - 1) surface coordinate guess 
  * **u_out** Output closest U (0 - 1) surface coordinate 
  * **w_out** Output closest W (0 - 1) surface coordinate 


**See**: [AxisProjPnt01](Modules/group___surface_query.md#function-axisprojpnt01), [AxisProjPnt01I](Modules/group___surface_query.md#function-axisprojpnt01i), [AxisProjVecPnt01](Modules/group___surface_query.md#function-axisprojvecpnt01), [AxisProjVecPnt01Guess](Modules/group___surface_query.md#function-axisprojvecpnt01guess)

**Return**: Distance between the 3D point and the closest point of the surface 

Project an input 3D coordinate point onto a surface along a specified axis given an initial guess of surface parameter. If the axis-aligned ray from the point intersects the surface multiple times, the nearest intersection is returned. If the axis-aligned ray from the point does not intersect the surface, the original point is returned and -1 is returned in the other output parameters. The surface parameter guess should allow this call to be faster than calling AxisProjPnt01 without a guess.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double u = 0.12345;
double w = 0.67890;



vec3d surf_pt = CompPnt01( geom_id, surf_indx, u, w );
vec3d pt = surf_pt;

pt.offset_y( -5.0 );

// Construct initial guesses near actual parameters
double u0 = u + 0.01234;
double w0 = w - 0.05678;

double uout, wout;

double d = AxisProjPnt01Guess( geom_id, surf_indx, Y_DIR, pt, u0, w0, uout, wout);

Print( "Dist " + d + " u " + uout + " w " + wout );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

u = 0.12345
w = 0.67890



surf_pt = CompPnt01( geom_id, surf_indx, u, w )
pt = surf_pt

pt.offset_y( -5.0 )

# Construct initial guesses near actual parameters
u0 = u + 0.01234
w0 = w - 0.05678

d, uout, wout = AxisProjPnt01Guess( geom_id, surf_indx, Y_DIR, pt, u0, w0 )

print( f"Dist {d} u {uout} w {wout}" )
```

  


### function InsideSurf

```
bool InsideSurf(
    const std::string & geom_id,
    const int & surf_indx,
    const vec3d & pt
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pt** Input 3D coordinate point 


**See**: [VecInsideSurf](Modules/group___surface_query.md#function-vecinsidesurf)

**Return**: Boolean true if the point is inside the surface, false otherwise. 

Test whether a given point is inside a specified surface.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double r = 0.12;
double s = 0.68;
double t = 0.56;

vec3d pnt = CompPntRST( geom_id, surf_indx, r, s, t );

bool res = InsideSurf( geom_id, surf_indx, pnt );

if ( res )
{
    Print( "Inside" );
}
else
{
    Print( "Outside" );
}
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

r = 0.12
s = 0.68
t = 0.56

pnt = CompPntRST( geom_id, surf_indx, r, s, t )

res = InsideSurf( geom_id, surf_indx, pnt )

if  res :
    print( "Inside" )
else:
    print( "Outside" )
```

  


### function CompPntRST

```
vec3d CompPntRST(
    const std::string & geom_id,
    const int & surf_indx,
    const double & r,
    const double & s,
    const double & t
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **r** R (0 - 1) volume coordinate 
  * **s** S (0 - 1) volume coordinate 
  * **t** T (0 - 1) volume coordinate 


**Return**: [vec3d](Classes/classvec3d.md) coordinate point 

Calculate the (X, Y, Z) coordinate for the input volume (R, S, T) coordinate point 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double r = 0.12;
double s = 0.68;
double t = 0.56;

vec3d pnt = CompPntRST( geom_id, surf_indx, r, s, t );

Print( "Point: ( " + pnt.x() + ', ' + pnt.y() + ', ' + pnt.z() + ' )' );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

r = 0.12
s = 0.68
t = 0.56

pnt = CompPntRST( geom_id, surf_indx, r, s, t )

print( f"Point: ( {pnt.x()}, {pnt.y()}, {pnt.z()} )" )
```

  


### function FindRST

```
double FindRST(
    const std::string & geom_id,
    const int & surf_indx,
    const vec3d & pt,
    double & r_out,
    double & s_out,
    double & t_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pt** [vec3d](Classes/classvec3d.md) Input 3D coordinate point 
  * **r_out** double Output closest R (0 - 1.0) volume coordinate 
  * **s_out** double Output closest S (0 - 1.0) volume coordinate 
  * **t_out** double Output closest T (0 - 1.0) volume coordinate 


**See**: [FindRSTGuess](Modules/group___surface_query.md#function-findrstguess)

**Return**: double Distance between the 3D point and the closest point of the volume 

Determine the nearest (R, S, T) volume coordinate for an input (X, Y, Z) 3D coordinate point and calculate the distance between the 3D point and the found volume point. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double r = 0.12;
double s = 0.68;
double t = 0.56;

vec3d pnt = CompPntRST( geom_id, surf_indx, r, s, t );

double rout, sout, tout;

double d = FindRST( geom_id, surf_indx, pnt, rout, sout, tout );

Print( "Dist " + d + " r " + rout + " s " + sout + " t " + tout );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

r = 0.12
s = 0.68
t = 0.56

pnt = CompPntRST( geom_id, surf_indx, r, s, t )


d, rout, sout, tout = FindRST( geom_id, surf_indx, pnt )

print( f"Dist {d} r {rout} s {sout} t {tout}" )
```

  


### function FindRSTGuess

```
double FindRSTGuess(
    const std::string & geom_id,
    const int & surf_indx,
    const vec3d & pt,
    const double & r0,
    const double & s0,
    const double & t0,
    double & r_out,
    double & s_out,
    double & t_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pt** [vec3d](Classes/classvec3d.md) Input 3D coordinate point 
  * **r0** double Input R (0 - 1.0) volume coordinate guess 
  * **s0** double Input S (0 - 1.0) volume coordinate guess 
  * **t0** double Input T (0 - 1.0) volume coordinate guess 
  * **r_out** double Output closest R (0 - 1.0) volume coordinate 
  * **s_out** double Output closest S (0 - 1.0) volume coordinate 
  * **t_out** double Output closest T (0 - 1.0) volume coordinate 


**See**: [FindRST](Modules/group___surface_query.md#function-findrst)

**Return**: double Distance between the 3D point and the closest point of the volume 

Determine the nearest (R, S, T) volume coordinate for an input (X, Y, Z) 3D coordinate point given an initial guess of volume coordinates. Also calculate the distance between the 3D point and the found volume point.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double r = 0.12;
double s = 0.68;
double t = 0.56;

vec3d pnt = CompPntRST( geom_id, surf_indx, r, s, t );

double rout, sout, tout;

double r0 = 0.1;
double s0 = 0.6;
double t0 = 0.5;

double d = FindRSTGuess( geom_id, surf_indx, pnt, r0, s0, t0, rout, sout, tout );

Print( "Dist " + d + " r " + rout + " s " + sout + " t " + tout );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

r = 0.12
s = 0.68
t = 0.56

pnt = CompPntRST( geom_id, surf_indx, r, s, t )


r0 = 0.1
s0 = 0.6
t0 = 0.5

d, rout, sout, tout = FindRSTGuess( geom_id, surf_indx, pnt, r0, s0, t0 )

print( f"Dist {d} r {rout} s {sout} t {tout}" )
```

  


### function ConvertRSTtoLMN

```
void ConvertRSTtoLMN(
    const std::string & geom_id,
    const int & surf_indx,
    const double & r,
    const double & s,
    const double & t,
    double & l_out,
    double & m_out,
    double & n_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **r** R (0 - 1) volume coordinate 
  * **s** S (0 - 1) volume coordinate 
  * **t** T (0 - 1) volume coordinate 
  * **l_out** L (0 - 1) linear volume coordinate 
  * **m_out** M (0 - 1) linear volume coordinate 
  * **n_out** N (0 - 1) linear volume coordinate 


Convert RST volumetric coordinates to LMN coordinates. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double r = 0.12;
double s = 0.68;
double t = 0.56;
double l_out, m_out, n_out;

ConvertRSTtoLMN( geom_id, surf_indx, r, s, t, l_out, m_out, n_out );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

r = 0.12
s = 0.68
t = 0.56

l_out, m_out, n_out = ConvertRSTtoLMN( geom_id, surf_indx, r, s, t )
```

  


### function ConvertRtoL

```
void ConvertRtoL(
    const std::string & geom_id,
    const int & surf_indx,
    const double & r,
    double & l_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **r** R (0 - 1) volume coordinate 
  * **l_out** L (0 - 1) linear volume coordinate 


Convert R volumetric coordinate to L coordinate. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double r = 0.12;
double l_out;

ConvertRtoL( geom_id, surf_indx, r, l_out );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

r = 0.12

l_out = ConvertRtoL( geom_id, surf_indx, r )
```

  


### function ConvertLMNtoRST

```
void ConvertLMNtoRST(
    const std::string & geom_id,
    const int & surf_indx,
    const double & l,
    const double & m,
    const double & n,
    double & r_out,
    double & s_out,
    double & t_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **l** L (0 - 1) linear volume coordinate 
  * **m** M (0 - 1) linear volume coordinate 
  * **n** N (0 - 1) linear volume coordinate 
  * **r_out** R (0 - 1) volume coordinate 
  * **s_out** S (0 - 1) volume coordinate 
  * **t_out** T (0 - 1) volume coordinate 


Convert LMN volumetric coordinates to RST coordinates. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double l = 0.12;
double m = 0.34;
double n = 0.56;
double r_out, s_out, t_out;

ConvertLMNtoRST( geom_id, surf_indx, l, m, n, r_out, s_out, t_out );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

l = 0.12
m = 0.34
n = 0.56

r_out, s_out, t_out = ConvertLMNtoRST( geom_id, surf_indx, l, m, n )
```

  


### function ConvertLtoR

```
void ConvertLtoR(
    const std::string & geom_id,
    const int & surf_indx,
    const double & l,
    double & r_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **l** L (0 - 1) volume coordinate 
  * **r_out** R (0 - 1) linear volume coordinate 


Convert L volumetric coordinate to R coordinate. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

double l = 0.12;
double r_out;

ConvertLtoR( geom_id, surf_indx, l, r_out );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

l = 0.12

r_out = ConvertLtoR( geom_id, surf_indx, l )
```

  


### function ConvertUtoEta

```
void ConvertUtoEta(
    const std::string & geom_id,
    const double & u,
    double & eta_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **u** U (0 - 1) surface coordinate 
  * **eta_out** Eta (0 - 1) wing spanwise coordinate 


Convert U coordinate to eta wing coordinate. 

// Add Wing Geom
string geom_id = AddGeom( "WING", "" );

int surf_indx = 0;

double u = 0.25;
double eta_out;

ConvertUtoEta( geom_id, u, eta_out );
```

 

# Add Wing Geom
geom_id = AddGeom( "WING", "" )

surf_indx = 0

u = 0.25

eta_out = ConvertUtoEta( geom_id, u )
```

  


### function ConvertEtatoU

```
void ConvertEtatoU(
    const std::string & geom_id,
    const double & eta,
    double & u_out
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **eta** Eta (0 - 1) wing spanwise coordinate 
  * **u_out** U (0 - 1) surface coordinate 


Convert eta wing coordinate to u coordinate. 

// Add Wing Geom
string geom_id = AddGeom( "WING", "" );

int surf_indx = 0;

double eta= 0.25;
double u_out;

ConvertEtatoU( geom_id, eta, u_out );
```

 

# Add Wing Geom
geom_id = AddGeom( "WING", "" )

surf_indx = 0

eta= 0.25

u = ConvertEtatoU( geom_id, eta )
```

  


### function CompVecPnt01

```
std::vector< vec3d > CompVecPnt01(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< double > & u_in_vec,
    const std::vector< double > & w_in_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **u_in_vec** vector<double> Input vector of U (0 - 1) surface coordinates 
  * **w_in_vec** vector<double> Input vector of W (0 - 1) surface coordinates 


**Return**: vector<vec3d> Vector of 3D coordinate points 

Determine 3D coordinate for each surface coordinate point in the input arrays 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPnt01( geom_id, 0, uvec, wvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)

ptvec = CompVecPnt01( geom_id, 0, uvec, wvec )
```

  


### function CompVecDegenPnt01

```
std::vector< vec3d > CompVecDegenPnt01(
    const std::string & geom_id,
    const int & surf_indx,
    const int & degen_type,
    const std::vector< double > & u_in_vec,
    const std::vector< double > & w_in_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **degen_type** int Type of degen surface (0-S, 1-V, 2-H, 3-C) 
  * **u_in_vec** vector<double> Input vector of U (0 - 1) surface coordinates 
  * **w_in_vec** vector<double> Input vector of W (0 - 1) surface coordinates 


**Return**: vector<vec3d> Vector of 3D coordinate points 

Determine 3D coordinate for each degen surface coordinate point in the input arrays 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecDegenPnt01( geom_id, 0, 0, uvec, wvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)

ptvec = CompVecDegenPnt01( geom_id, 0, 0, uvec, wvec )
```

  


### function CompVecNorm01

```
std::vector< vec3d > CompVecNorm01(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< double > & us,
    const std::vector< double > & ws
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **us** vector<double> Input vector of U (0 - 1) surface coordinates 
  * **ws** vector<double> Input vector of W (0 - 1) surface coordinates 


**Return**: vector<vec3d> Vector of 3D normal vectors 

Determine the normal vector on a surface for each surface coordinate point in the input arrays 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array< vec3d > normvec = CompVecNorm01( geom_id, 0, uvec, wvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)

normvec = CompVecNorm01( geom_id, 0, uvec, wvec )
```

  


### function CompVecCurvature01

```
void CompVecCurvature01(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< double > & us,
    const std::vector< double > & ws,
    std::vector< double > & k1_out_vec,
    std::vector< double > & k2_out_vec,
    std::vector< double > & ka_out_vec,
    std::vector< double > & kg_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **us** vector<double> Input vector of U (0 - 1) surface coordinates 
  * **ws** vector<double> Input vector of W (0 - 1) surface coordinates 
  * **k1_out_vec** vector<double> Output vector of maximum principal curvatures 
  * **k2_out_vec** vector<double> Output vector of minimum principal curvatures 
  * **ka_out_vec** vector<double> Output vector of mean curvatures 
  * **kg_out_vec** vector<double> Output vector of Gaussian curvatures 


Determine the curvature of a specified surface at each surface coordinate point in the input arrays 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array<double> k1vec, k2vec, kavec, kgvec;

CompVecCurvature01( geom_id, 0, uvec, wvec, k1vec, k2vec, kavec, kgvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)



k1vec, k2vec, kavec, kgvec = CompVecCurvature01( geom_id, 0, uvec, wvec )
```

  


### function ProjVecPnt01

```
void ProjVecPnt01(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< vec3d > & pts,
    std::vector< double > & u_out_vec,
    std::vector< double > & w_out_vec,
    std::vector< double > & d_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pts** vector<vec3d> Input vector of 3D coordinate points 
  * **u_out_vec** vector<double> Output vector of the closest U (0 - 1) surface coordinate for each 3D input point 
  * **w_out_vec** vector<double> Output vector of the closest W (0 - 1) surface coordinate for each 3D input point 
  * **d_out_vec** vector<double> Output vector of distances for each 3D point and the closest point of the surface 


**See**: [ProjVecPnt01Guess](Modules/group___surface_query.md#function-projvecpnt01guess)

Determine the nearest surface coordinates for an input array of 3D coordinate points and calculate the distance between each 3D point and the closest point of the surface. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPnt01( geom_id, 0, uvec, wvec );

array< vec3d > normvec = CompVecNorm01( geom_id, 0, uvec, wvec );

for( int i = 0 ; i < n ; i++ )
{
    ptvec[i] = ptvec[i] + normvec[i];
}

array<double> uoutv, woutv, doutv;

ProjVecPnt01( geom_id, 0, ptvec, uoutv, woutv, doutv );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)

ptvec = CompVecPnt01( geom_id, 0, uvec, wvec )

normvec = CompVecNorm01( geom_id, 0, uvec, wvec )

for i in range(n):

    ptvec[i].set_xyz( ptvec[i].x() + normvec[i].x(), ptvec[i].y() + normvec[i].y(), ptvec[i].z() + normvec[i].z() )

uoutv, woutv, doutv = ProjVecPnt01( geom_id, 0, ptvec )
```

  


### function ProjVecPnt01Guess

```
void ProjVecPnt01Guess(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< vec3d > & pts,
    const std::vector< double > & u0s,
    const std::vector< double > & w0s,
    std::vector< double > & u_out_vec,
    std::vector< double > & w_out_vec,
    std::vector< double > & d_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pts** vector<vec3d> Input vector of 3D coordinate points 
  * **u0s** vector<double> Input vector of U (0 - 1) surface coordinate guesses 
  * **w0s** vector<double> Input vector of W (0 - 1) surface coordinate guesses 
  * **u_out_vec** vector<double> Output vector of the closest U (0 - 1) surface coordinate for each 3D input point 
  * **w_out_vec** vector<double> Output vector of the closest W (0 - 1) surface coordinate for each 3D input point 
  * **d_out_vec** vector<double> Output array of distances for each 3D point and the closest point of the surface 


**See**: [ProjVecPnt01](Modules/group___surface_query.md#function-projvecpnt01), 

Determine the nearest surface coordinates for an input array of 3D coordinate points and calculate the distance between each 3D point and the closest point of the surface. This function takes an input array of surface coordinate guesses for each 3D coordinate, offering a potential decrease in computation time compared to ProjVecPnt01. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPnt01( geom_id, 0, uvec, wvec );

array< vec3d > normvec = CompVecNorm01( geom_id, 0, uvec, wvec );

for( int i = 0 ; i < n ; i++ )
{
    ptvec[i] = ptvec[i] + normvec[i];
}

array<double> uoutv, woutv, doutv, u0v, w0v;

u0v.resize( n );
w0v.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    u0v[i] = uvec[i] + 0.01234;

    w0v[i] = wvec[i] - 0.05678;
}

ProjVecPnt01Guess( geom_id, 0, ptvec, u0v,  w0v,  uoutv, woutv, doutv );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)

ptvec = CompVecPnt01( geom_id, 0, uvec, wvec )

normvec = CompVecNorm01( geom_id, 0, uvec, wvec )

for i in range(n):

    ptvec[i].set_xyz( ptvec[i].x() + normvec[i].x(), ptvec[i].y() + normvec[i].y(), ptvec[i].z() + normvec[i].z() )

u0v = [0]*n
w0v = [0]*n

for i in range(n):

    u0v[i] = uvec[i] + 0.01234

    w0v[i] = wvec[i] - 0.05678

uoutv, woutv, doutv = ProjVecPnt01Guess( geom_id, 0, ptvec, u0v,  w0v )
```

  


### function AxisProjVecPnt01

```
void AxisProjVecPnt01(
    const std::string & geom_id,
    const int & surf_indx,
    const int & iaxis,
    const std::vector< vec3d > & pts,
    std::vector< double > & u_out_vec,
    std::vector< double > & w_out_vec,
    std::vector< double > & d_out_vec
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **surf_indx** int Main surface index from the Geom 
  * **iaxis** int Axis direction to project point along (X_DIR, Y_DIR, or Z_DIR) 
  * **pts** vector<vec3d> Input vector of 3D coordinate points 
  * **u_out_vec** vector<double> Output vector of the closest U (0 - 1) surface coordinate for each 3D input point 
  * **w_out_vec** vector<double> Output vector of the closest W (0 - 1) surface coordinate for each 3D input point 
  * **d_out_vec** vector<double> Output vector of axis distances for each 3D point and the projected point of the surface 


**See**: [AxisProjPnt01](Modules/group___surface_query.md#function-axisprojpnt01), [AxisProjPnt01Guess](Modules/group___surface_query.md#function-axisprojpnt01guess), [AxisProjPnt01I](Modules/group___surface_query.md#function-axisprojpnt01i), [AxisProjVecPnt01Guess](Modules/group___surface_query.md#function-axisprojvecpnt01guess)

Project an input array of 3D coordinate points onto a surface along a specified axis. If the axis-aligned ray from the point intersects the surface multiple times, the nearest intersection is returned. If the axis-aligned ray from the point does not intersect the surface, the original point is returned and -1 is returned in the other output parameters.



   // Add Pod Geom
string geom_id = AddGeom( "POD", "" );
int surf_indx = 0;

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPnt01( geom_id, surf_indx, uvec, wvec );

for( int i = 0 ; i < n ; i++ )
{
    ptvec[i].offset_y( -5.0 );
}

array<double> uoutv, woutv, doutv;

AxisProjVecPnt01( geom_id, surf_indx, Y_DIR, ptvec, uoutv, woutv, doutv );

// Some of these outputs are expected to be non-zero because the projected point is on the opposite side of
// the pod from the originally computed point.  I.e. there were multiple solutions and the original point
// is not the closest intersection point.  We could offset those points in the +Y direction instead of -Y.
for( int i = 0 ; i < n ; i++ )
{
    Print( i, false );
    Print( "U delta ", false );
    Print( uvec[i] - uoutv[i], false );
    Print( "W delta ", false );
    Print( wvec[i] - woutv[i] );
}
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )
surf_indx = 0

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)

ptvec = CompVecPnt01( geom_id, surf_indx, uvec, wvec )

for i in range(n):

    ptvec[i].offset_y( -5.0 )

uoutv, woutv, doutv = AxisProjVecPnt01( geom_id, surf_indx, Y_DIR, ptvec )

# Some of these outputs are expected to be non-zero because the projected point is on the opposite side of
# the pod from the originally computed point.  I.e. there were multiple solutions and the original point
# is not the closest intersection point.  We could offset those points in the +Y direction instead of -Y.
for i in range(n):

    print( i, False )
    print( "U delta ", False )
    print( uvec[i] - uoutv[i], False )
    print( "W delta ", False )
    print( wvec[i] - woutv[i] )
```

  


### function AxisProjVecPnt01Guess

```
void AxisProjVecPnt01Guess(
    const std::string & geom_id,
    const int & surf_indx,
    const int & iaxis,
    const std::vector< vec3d > & pts,
    const std::vector< double > & u0s,
    const std::vector< double > & w0s,
    std::vector< double > & u_out_vec,
    std::vector< double > & w_out_vec,
    std::vector< double > & d_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **iaxis** int Axis direction to project point along (X_DIR, Y_DIR, or Z_DIR) 
  * **pts** vector<vec3d> Input vector of 3D coordinate points 
  * **u0s** vector<double> Input vector of U (0 - 1) surface coordinate guesses 
  * **w0s** vector<double> Input vector of W (0 - 1) surface coordinate guesses 
  * **u_out_vec** vector<double> Output vector of the closest U (0 - 1) surface coordinate for each 3D input point 
  * **w_out_vec** vector<double> Output vector of the closest W (0 - 1) surface coordinate for each 3D input point 
  * **d_out_vec** vector<double> Output vector of axis distances for each 3D point and the projected point of the surface 


**See**: [AxisProjPnt01](Modules/group___surface_query.md#function-axisprojpnt01), [AxisProjPnt01Guess](Modules/group___surface_query.md#function-axisprojpnt01guess), [AxisProjPnt01I](Modules/group___surface_query.md#function-axisprojpnt01i), [AxisProjVecPnt01](Modules/group___surface_query.md#function-axisprojvecpnt01)

Project an input array of 3D coordinate points onto a surface along a specified axis given initial guess arrays of surface parameter. If the axis-aligned ray from the point intersects the surface multiple times, the nearest intersection is returned. If the axis-aligned ray from the point does not intersect the surface, the original point is returned and -1 is returned in the other output parameters. The surface parameter guess should allow this call to be faster than calling AxisProjVecPnt01 without a guess. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );
int surf_indx = 0;

int n = 5;

array<double> uvec, wvec;

uvec.resize( n );
wvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    uvec[i] = (i+1)*1.0/(n+1);

    wvec[i] = (n-i)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPnt01( geom_id, surf_indx, uvec, wvec );

for( int i = 0 ; i < n ; i++ )
{
    ptvec[i].offset_y( -5.0 );
}

array<double> uoutv, woutv, doutv, u0v, w0v;

u0v.resize( n );
w0v.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    u0v[i] = uvec[i] + 0.01234;
    w0v[i] = wvec[i] - 0.05678;
}

AxisProjVecPnt01Guess( geom_id, surf_indx, Y_DIR, ptvec, u0v,  w0v,  uoutv, woutv, doutv );

for( int i = 0 ; i < n ; i++ )
{
    Print( i, false );
    Print( "U delta ", false );
    Print( uvec[i] - uoutv[i], false );
    Print( "W delta ", false );
    Print( wvec[i] - woutv[i] );
}
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )
surf_indx = 0

n = 5

uvec = [0]*n
wvec = [0]*n

for i in range(n):

    uvec[i] = (i+1)*1.0/(n+1)

    wvec[i] = (n-i)*1.0/(n+1)

ptvec = CompVecPnt01( geom_id, surf_indx, uvec, wvec )

for i in range(n):

    ptvec[i].offset_y( -5.0 )

u0v = [0]*n
w0v = [0]*n

for i in range(n):

    u0v[i] = uvec[i] + 0.01234
    w0v[i] = wvec[i] - 0.05678

uoutv, woutv, doutv = AxisProjVecPnt01Guess( geom_id, surf_indx, Y_DIR, ptvec, u0v,  w0v )

for i in range(n):

    print( i, False )
    print( "U delta ", False )
    print( uvec[i] - uoutv[i], False )
    print( "W delta ", False )
    print( wvec[i] - woutv[i] )
```

  


### function VecInsideSurf

```
std::vector< bool > VecInsideSurf(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< vec3d > & pts
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pts** vector<vec3d> Input vector of 3D coordinate points 


**See**: [VecInsideSurf](Modules/group___surface_query.md#function-vecinsidesurf)

**Return**: Boolean vector for each point. True if it is inside the surface, false otherwise. 

Test whether a vector of points are inside a specified surface.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

int n = 5;

array<double> rvec, svec, tvec;

rvec.resize( n );
svec.resize( n );
tvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    rvec[i] = (i+1)*1.0/(n+1);

    svec[i] = (n-i)*1.0/(n+1);

    tvec[i] = (i+1)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec );

array<bool> res;
res = VecInsideSurf( geom_id, surf_indx, ptvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

n = 5

rvec = [0]*n
svec = [0]*n
tvec = [0]*n

for i in range(n):

    rvec[i] = (i+1)*1.0/(n+1)

    svec[i] = (n-i)*1.0/(n+1)

    tvec[i] = (i+1)*1.0/(n+1)

ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec )


res = VecInsideSurf( geom_id, surf_indx, ptvec )
```

  


### function CompVecPntRST

```
std::vector< vec3d > CompVecPntRST(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< double > & r_in_vec,
    const std::vector< double > & s_in_vec,
    const std::vector< double > & t_in_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **r_in_vec** vector<double> Input vector of R (0 - 1.0) volume coordinates 
  * **s_in_vec** vector<double> Input vector of S (0 - 1.0) volume coordinates 
  * **t_in_vec** vector<double> Input vector of T (0 - 1.0) volume coordinates 


**Return**: vector<vec3d> Vector of 3D coordinate points 

Determine 3D coordinate for each volume coordinate point in the input arrays 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> rvec, svec, tvec;

rvec.resize( n );
svec.resize( n );
tvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    rvec[i] = (i+1)*1.0/(n+1);

    svec[i] = (n-i)*1.0/(n+1);

    tvec[i] = (i+1)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

rvec = [0]*n
svec = [0]*n
tvec = [0]*n

for i in range(n):

    rvec[i] = (i+1)*1.0/(n+1)

    svec[i] = (n-i)*1.0/(n+1)

    tvec[i] = (i+1)*1.0/(n+1)

ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec )
```

  


### function FindRSTVec

```
void FindRSTVec(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< vec3d > & pts,
    std::vector< double > & r_out_vec,
    std::vector< double > & s_out_vec,
    std::vector< double > & t_out_vec,
    std::vector< double > & d_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pts** vector<vec3d> Input vector of 3D coordinate points 
  * **r_out_vec** vector<double> Output vector of the closest R (0 - 1.0) volume coordinate for each 3D input point 
  * **s_out_vec** vector<double> Output vector of the closest S (0 - 1.0) volume coordinate for each 3D input point 
  * **t_out_vec** vector<double> Output vector of the closest T (0 - 1.0) volume coordinate for each 3D input point 
  * **d_out_vec** vector<double> Output vector of distances for each 3D point and the closest point of the volume 


**See**: [FindRSTVecGuess](Modules/group___surface_query.md#function-findrstvecguess)

Determine the nearest volume coordinates for an input array of 3D coordinate points and calculate the distance between each 3D point and the found point in the volume. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> rvec, svec, tvec;

rvec.resize( n );
svec.resize( n );
tvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    rvec[i] = (i+1)*1.0/(n+1);

    svec[i] = (n-i)*1.0/(n+1);

    tvec[i] = (i+1)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec );

array<double> routv, soutv, toutv, doutv;

FindRSTVec( geom_id, 0, ptvec, routv, soutv, toutv, doutv );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

rvec = [0]*n
svec = [0]*n
tvec = [0]*n

for i in range(n):

    rvec[i] = (i+1)*1.0/(n+1)

    svec[i] = (n-i)*1.0/(n+1)

    tvec[i] = (i+1)*1.0/(n+1)

ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec )



routv, soutv, toutv, doutv = FindRSTVec( geom_id, 0, ptvec )
```

  


### function FindRSTVecGuess

```
void FindRSTVecGuess(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< vec3d > & pts,
    const std::vector< double > & r0s,
    const std::vector< double > & s0s,
    const std::vector< double > & t0s,
    std::vector< double > & r_out_vec,
    std::vector< double > & s_out_vec,
    std::vector< double > & t_out_vec,
    std::vector< double > & d_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **pts** vector<vec3d> Input vector of 3D coordinate points 
  * **r0s** vector<double> Input vector of U (0 - 1.0) volume coordinate guesses 
  * **s0s** vector<double> Input vector of S (0 - 1.0) volume coordinate guesses 
  * **t0s** vector<double> Input vector of T (0 - 1.0) volume coordinate guesses 
  * **r_out_vec** vector<double> Output vector of the closest R (0 - 1.0) volume coordinate for each 3D input point 
  * **s_out_vec** vector<double> Output vector of the closest S (0 - 1.0) volume coordinate for each 3D input point 
  * **t_out_vec** vector<double> Output vector of the closest T (0 - 1.0) volume coordinate for each 3D input point 
  * **d_out_vec** vector<double> Output vector of distances for each 3D point and the closest point of the volume 


**See**: [FindRSTVec](Modules/group___surface_query.md#function-findrstvec), 

Determine the nearest volume coordinates for an input array of 3D coordinate points and calculate the distance between each 3D point and the closest point of the volume. This function takes an input array of volume coordinate guesses for each 3D coordinate, offering a potential decrease in computation time compared to FindRSTVec. 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> rvec, svec, tvec;

rvec.resize( n );
svec.resize( n );
tvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    rvec[i] = (i+1)*1.0/(n+1);

    svec[i] = (n-i)*1.0/(n+1);

    tvec[i] = (i+1)*1.0/(n+1);
}

array< vec3d > ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec );

array<double> routv, soutv, toutv, doutv;

for( int i = 0 ; i < n ; i++ )
{
    ptvec[i] = ptvec[i] * 0.9;
}

FindRSTVecGuess( geom_id, 0, ptvec, rvec, svec, tvec, routv, soutv, toutv, doutv );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

rvec = [0]*n
svec = [0]*n
tvec = [0]*n

for i in range(n):

    rvec[i] = (i+1)*1.0/(n+1)

    svec[i] = (n-i)*1.0/(n+1)

    tvec[i] = (i+1)*1.0/(n+1)

ptvec = CompVecPntRST( geom_id, 0, rvec, svec, tvec )

for i in range(n):

    ptvec[i].set_xyz(ptvec[i].x() * 0.9, ptvec[i].y() * 0.9, ptvec[i].z() * 0.9)

 routv, soutv, toutv, doutv = FindRSTVecGuess( geom_id, 0, ptvec, rvec, svec, tvec )
```

  


### function ConvertRSTtoLMNVec

```
void ConvertRSTtoLMNVec(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< double > & r_vec,
    const std::vector< double > & s_vec,
    const std::vector< double > & t_vec,
    std::vector< double > & l_out_vec,
    std::vector< double > & m_out_vec,
    std::vector< double > & n_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **r_vec** vector<double> Input vector of R (0 - 1) volumetric coordinate 
  * **s_vec** vector<double> Input vector of S (0 - 1) volumetric coordinate 
  * **t_vec** vector<double> Input vector of T (0 - 1) volumetric coordinate 
  * **l_out_vec** vector<double> Output vector of L (0 - 1) linear volumetric coordinate 
  * **m_out_vec** vector<double> Output vector of M (0 - 1) linear volumetric coordinate 
  * **n_out_vec** vector<double> Output vector of N (0 - 1) linear volumetric coordinate 


**See**: [ConvertLMNtoRSTVec](Modules/group___surface_query.md#function-convertlmntorstvec), [ConvertRSTtoLMN](Modules/group___surface_query.md#function-convertrsttolmn), [ConvertLMNtoRST](Modules/group___surface_query.md#function-convertlmntorst)

Convert vector of RST volumetric coordinates to LMN coordinates.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> rvec, svec, tvec;

rvec.resize( n );
svec.resize( n );
tvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    rvec[i] = (i+1)*1.0/(n+1);
    svec[i] = (n-i)*1.0/(n+1);
    tvec[i] = (i+1)*1.0/(n+1);
}

array<double> lvec, mvec, nvec;

ConvertRSTtoLMNVec( geom_id, 0, rvec, svec, tvec, lvec, mvec, nvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

rvec = [0]*n
svec = [0]*n
tvec = [0]*n

for i in range(n):

    rvec[i] = (i+1)*1.0/(n+1)
    svec[i] = (n-i)*1.0/(n+1)
    tvec[i] = (i+1)*1.0/(n+1)



lvec, mvec, nvec = ConvertRSTtoLMNVec( geom_id, 0, rvec, svec, tvec )
```

  


### function ConvertLMNtoRSTVec

```
void ConvertLMNtoRSTVec(
    const std::string & geom_id,
    const int & surf_indx,
    const std::vector< double > & l_vec,
    const std::vector< double > & m_vec,
    const std::vector< double > & n_vec,
    std::vector< double > & r_out_vec,
    std::vector< double > & s_out_vec,
    std::vector< double > & t_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **l_vec** vector<double> Input vector of L (0 - 1) linear volumetric coordinate 
  * **m_vec** vector<double> Input vector of M (0 - 1) linear volumetric coordinate 
  * **n_vec** vector<double> Input vector of N (0 - 1) linear volumetric coordinate 
  * **r_out_vec** vector<double> Output vector of R (0 - 1) volumetric coordinate 
  * **s_out_vec** vector<double> Output vector of S (0 - 1) volumetric coordinate 
  * **t_out_vec** vector<double> Output vector of T (0 - 1) volumetric coordinate 


**See**: [ConvertRSTtoLMNVec](Modules/group___surface_query.md#function-convertrsttolmnvec), [ConvertRSTtoLMN](Modules/group___surface_query.md#function-convertrsttolmn), [ConvertLMNtoRST](Modules/group___surface_query.md#function-convertlmntorst)

Convert vector of LMN volumetric coordinates to RST coordinates.



// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int n = 5;

array<double> lvec, mvec, nvec;

lvec.resize( n );
mvec.resize( n );
nvec.resize( n );

for( int i = 0 ; i < n ; i++ )
{
    lvec[i] = (i+1)*1.0/(n+1);
    mvec[i] = (n-i)*1.0/(n+1);
    nvec[i] = (i+1)*1.0/(n+1);
}

array<double> rvec, svec, tvec;

ConvertLMNtoRSTVec( geom_id, 0, lvec, mvec, nvec, rvec, svec, tvec );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

n = 5

lvec = [0]*n
mvec = [0]*n
nvec = [0]*n

for i in range(n):

    lvec[i] = (i+1)*1.0/(n+1)
    mvec[i] = (n-i)*1.0/(n+1)
    nvec[i] = (i+1)*1.0/(n+1)

rvec, svec, tvec = ConvertLMNtoRSTVec( geom_id, 0, lvec, mvec, nvec )
```

  


### function GetUWTess01

```
void GetUWTess01(
    const std::string & geom_id,
    const int & surf_indx,
    std::vector< double > & u_out_vec,
    std::vector< double > & w_out_vec
)
```


**Parameters**: 

  * **geom_id** string Parent Geom ID 
  * **surf_indx** int Main surface index from the parent Geom 
  * **u_out_vec** vector<double> Output vector of U (0 - 1) surface coordinates 
  * **w_out_vec** vector<double> Output vector of W (0 - 1) surface coordinates 


Get the surface coordinate point of each intersection of the tessellated wireframe for a particular surface 

// Add Pod Geom
string geom_id = AddGeom( "POD", "" );

int surf_indx = 0;

array<double> utess, wtess;

GetUWTess01( geom_id, surf_indx, utess, wtess );
```

 

# Add Pod Geom
geom_id = AddGeom( "POD", "" )

surf_indx = 0

utess, wtess = GetUWTess01( geom_id, surf_indx )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800