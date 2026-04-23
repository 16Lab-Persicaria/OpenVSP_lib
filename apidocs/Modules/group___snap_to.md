---
title: Snap-To Functions
summary: This group of API functions provide the capabilities available in the Snap-To tool. Click here to return to the main page. 

---

# Snap-To Functions

This group of API functions provide the capabilities available in the Snap-To tool. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| double | **[ComputeMinClearanceDistance](Modules/group___snap_to.md#function-computeminclearancedistance)**(const std::string & geom_id, int set =SET_ALL, bool useMode =false, const string & modeID =string()) |
| double | **[SnapParm](Modules/group___snap_to.md#function-snapparm)**(const std::string & parm_id, double target_min_dist, bool inc_flag, int set =SET_ALL, bool useMode =false, const string & modeID =string()) |


## Functions Documentation

### function ComputeMinClearanceDistance

```
double ComputeMinClearanceDistance(
    const std::string & geom_id,
    int set =SET_ALL,
    bool useMode =false,
    const string & modeID =string()
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **set** Collision set enum (i.e. SET_ALL) 
  * **useMode** bool Flag determine if mode is used instead of sets 
  * **modeID** string ID of Mode to use 


**Return**: Minimum clearance distance 

Compute the minimum clearance distance for the specified geometry 

string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string pid = AddGeom( "POD", "" );                     // Add Pod

string x = GetParm( pid, "X_Rel_Location", "XForm" );

SetParmVal( x, 3.0 );

Update();

double min_dist = ComputeMinClearanceDistance( pid, SET_ALL );
```

 

fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

pid = AddGeom( "POD", "" )                     # Add Pod

x = GetParm( pid, "X_Rel_Location", "XForm" )

SetParmVal( x, 3.0 )

Update()

min_dist = ComputeMinClearanceDistance( pid, SET_ALL )
```

  


### function SnapParm

```
double SnapParm(
    const std::string & parm_id,
    double target_min_dist,
    bool inc_flag,
    int set =SET_ALL,
    bool useMode =false,
    const string & modeID =string()
)
```


**Parameters**: 

  * **parm_id** string Parm ID 
  * **target_min_dist** Target minimum clearance distance 
  * **inc_flag** Direction indication flag. If true, upper parm limit is used and direction is set to positive 
  * **set** Collision set enum (i.e. SET_ALL) 
  * **useMode** bool Flag determine if mode is used instead of sets 
  * **modeID** string ID of Mode to use 


**Return**: Minimum clearance distance 

Snap the specified Parm to input target minimum clearance distance 

//Add Geoms
string fid = AddGeom( "FUSELAGE", "" );             // Add Fuselage

string pid = AddGeom( "POD", "" );                     // Add Pod

string x = GetParm( pid, "X_Rel_Location", "XForm" );

SetParmVal( x, 3.0 );

Update();

double min_dist = SnapParm( x, 0.1, true, SET_ALL );
```

 

#Add Geoms
fid = AddGeom( "FUSELAGE", "" )             # Add Fuselage

pid = AddGeom( "POD", "" )                     # Add Pod

x = GetParm( pid, "X_Rel_Location", "XForm" )

SetParmVal( x, 3.0 )

Update()

min_dist = SnapParm( x, 0.1, True, SET_ALL )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800