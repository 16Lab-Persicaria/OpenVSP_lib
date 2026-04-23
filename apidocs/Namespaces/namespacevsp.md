---
title: vsp

---

# vsp



## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[vsp::ErrorObj](Classes/classvsp_1_1_error_obj.md)**  |
| class | **[vsp::ErrorMgrSingleton](Classes/classvsp_1_1_error_mgr_singleton.md)**  |
| class | **[vsp::UpdateCountMgrSingleton](Classes/classvsp_1_1_update_count_mgr_singleton.md)**  |

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[RegisterCFDMeshAnalyses](Namespaces/namespacevsp.md#function-registercfdmeshanalyses)**() |
| void | **[LimitedIntersectSurfaces](Namespaces/namespacevsp.md#function-limitedintersectsurfaces)**(const vector< string > & geomvec, vector< vector< vec3d > > & ptchains, vector< vector< vec3d > > & uwchains) |
| std::string | **[GetResultsEntryDoc](Namespaces/namespacevsp.md#function-getresultsentrydoc)**(const std::string & results_id, const std::string & data_name) |
| double | **[IntegrateEllipsoidFlow](Namespaces/namespacevsp.md#function-integrateellipsoidflow)**(const vec3d & abc_rad, const int & abc_index) |
| int | **[GetNumRoutingPts](Namespaces/namespacevsp.md#function-getnumroutingpts)**(const string & routing_id) |
| string | **[AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt)**(const string & routing_id, const string & geom_id, int surf_index) |
| string | **[InsertRoutingPt](Namespaces/namespacevsp.md#function-insertroutingpt)**(const string & routing_id, int index, const string & geom_id, int surf_index) |
| void | **[DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt)**(const string & routing_id, int index) |
| void | **[DelAllRoutingPt](Namespaces/namespacevsp.md#function-delallroutingpt)**(const string & routing_id) |
| int | **[MoveRoutingPt](Namespaces/namespacevsp.md#function-moveroutingpt)**(const string & routing_id, int index, int reorder_type) |
| string | **[GetRoutingPtID](Namespaces/namespacevsp.md#function-getroutingptid)**(const string & routing_id, int index) |
| vector< string > | **[GetAllRoutingPtIds](Namespaces/namespacevsp.md#function-getallroutingptids)**(const string & routing_id) |
| string | **[GetRoutingPtParentID](Namespaces/namespacevsp.md#function-getroutingptparentid)**(const string & pt_id) |
| void | **[SetRoutingPtParentID](Namespaces/namespacevsp.md#function-setroutingptparentid)**(const string & pt_id, const string & parent_id) |
| vec3d | **[GetMainRoutingPtCoord](Namespaces/namespacevsp.md#function-getmainroutingptcoord)**(const string & pt_id) |
| vec3d | **[GetRoutingPtCoord](Namespaces/namespacevsp.md#function-getroutingptcoord)**(const string & routing_id, int index, int symm_index) |
| vector< vec3d > | **[GetAllRoutingPtCoords](Namespaces/namespacevsp.md#function-getallroutingptcoords)**(const string & routing_id, int symm_index) |
| vector< vec3d > | **[GetRoutingCurve](Namespaces/namespacevsp.md#function-getroutingcurve)**(const string & routing_id, int symm_index) |


## Functions Documentation

### function RegisterCFDMeshAnalyses

```cpp
void RegisterCFDMeshAnalyses()
```


### function LimitedIntersectSurfaces

```cpp
void LimitedIntersectSurfaces(
    const vector< string > & geomvec,
    vector< vector< vec3d > > & ptchains,
    vector< vector< vec3d > > & uwchains
)
```


### function GetResultsEntryDoc

```cpp
std::string GetResultsEntryDoc(
    const std::string & results_id,
    const std::string & data_name
)
```


### function IntegrateEllipsoidFlow

```cpp
double IntegrateEllipsoidFlow(
    const vec3d & abc_rad,
    const int & abc_index
)
```


### function GetNumRoutingPts

```cpp
int GetNumRoutingPts(
    const string & routing_id
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt)

**Return**: int Number of routing points in specified RoutingGeom 

Get the number of routing points in a RoutingGeom 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

int npt = GetNumRoutingPts(routing_geom);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

npt = vsp.GetNumRoutingPts(routing_geom)
```

  


### function AddRoutingPt

```cpp
string AddRoutingPt(
    const string & routing_id,
    const string & geom_id,
    int surf_index
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **geom_id** string Geom ID of geom to anchor new routing point to 
  * **surf_index** int Index of surf to anchor new routing point to 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt), [InsertRoutingPt](Namespaces/namespacevsp.md#function-insertroutingpt)

**Return**: string ParmContainer ID for the newly added routing point 

Add a routing point to a RoutingGeom. The new point will be the last point in the route. The new point will be anchored to the specified geom and surface. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)
```

  


### function InsertRoutingPt

```cpp
string InsertRoutingPt(
    const string & routing_id,
    int index,
    const string & geom_id,
    int surf_index
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **index** int Index of routing point to insert new point before 
  * **geom_id** string Geom ID of geom to anchor new routing point to 
  * **surf_index** int Index of surf to anchor new routing point to 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt)

**Return**: string ParmContainer ID for the newly added routing point 

Add a routing point to a RoutingGeom. The new point will be inserted before the specified index. The new point will be anchored to the specified geom and surface. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

int npt = GetNumRoutingPts(routing_geom);

string rptPre2 = InsertRoutingPt(routing_geom, 2, pod2, 0);
string uPre2 = GetParm( rptPre2, "U", "RoutePt");
SetParmVal(uPre2, 0.);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

npt = vsp.GetNumRoutingPts(routing_geom)
rptPre2 = vsp.InsertRoutingPt(routing_geom, 2, pod2, 0)
uPre2 = vsp.GetParm( rptPre2, 'U', 'RoutePt')
vsp.SetParmVal(uPre2, 0.)
```

  


### function DelRoutingPt

```cpp
void DelRoutingPt(
    const string & routing_id,
    int index
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **index** int Index of routing point to delete 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelAllRoutingPt](Namespaces/namespacevsp.md#function-delallroutingpt)

Delete a specified routing point from a RoutingGeom. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

DelRoutingPt( routing_geom, 1 );
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

vsp.DelRoutingPt( routing_geom, 1 )
```

  


### function DelAllRoutingPt

```cpp
void DelAllRoutingPt(
    const string & routing_id
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt)

Delete all routing points from a RoutingGeom. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

DelAllRoutingPt( routing_geom );
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

vsp.DelAllRoutingPt( routing_geom )
```

  


### function MoveRoutingPt

```cpp
int MoveRoutingPt(
    const string & routing_id,
    int index,
    int reorder_type
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **index** int Index of routing point to move 
  * **reorder_type** int Enum specifying reordering type (i.e. REORDER_MOVE_UP, REORDER_MOVE_DOWN, REORDER_MOVE_TOP, REORDER_MOVE_BOTTOM) 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt), [REORDER_TYPE](Modules/group___enumerations.md#enum-reorder-type)

Move a specified routing point within the route of a RoutingGeom. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

int newindx = MoveRoutingPt( routing_geom, 1, REORDER_MOVE_DOWN );
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

newindx = vsp.MoveRoutingPt( routing_geom, 1, vsp.REORDER_MOVE_DOWN )
```

  


### function GetRoutingPtID

```cpp
string GetRoutingPtID(
    const string & routing_id,
    int index
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **index** int Index of routing point to ID to retreive 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelAllRoutingPt](Namespaces/namespacevsp.md#function-delallroutingpt), [GetAllRoutingPtIds](Namespaces/namespacevsp.md#function-getallroutingptids)

**Return**: string ParmContainer ID for the specified routing point 

Get the ParmContainer ID of a routing point within a RoutingGeom. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

string rid = GetRoutingPtID(routing_geom, 2);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

rid = vsp.GetRoutingPtID(routing_geom, 2)
```

  


### function GetAllRoutingPtIds

```cpp
vector< string > GetAllRoutingPtIds(
    const string & routing_id
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelAllRoutingPt](Namespaces/namespacevsp.md#function-delallroutingpt), GetRoutingPtId 

**Return**: vector<string> Vector of routing point ParmConatiner IDs 

Get the ParmContainer IDs of all the routing points within a RoutingGeom. The vector will contain the IDs in order. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

array<string> @rpts = GetAllRoutingPtIds(routing_geom);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

rpts = vsp.GetAllRoutingPtIds(routing_geom)
```

  


### function GetRoutingPtParentID

```cpp
string GetRoutingPtParentID(
    const string & pt_id
)
```


**Parameters**: 

  * **pt_id** string ParmContainer ID of desired routing point 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelAllRoutingPt](Namespaces/namespacevsp.md#function-delallroutingpt), [GetAllRoutingPtIds](Namespaces/namespacevsp.md#function-getallroutingptids)

**Return**: string Geom ID for the geom the routing point is anchored to 

Get the Geom ID of the geom a routing point is anchored to. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

string gid = GetRoutingPtParentID(rpt1);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

gid = vsp.GetRoutingPtParentID(rpt1)
```

  


### function SetRoutingPtParentID

```cpp
void SetRoutingPtParentID(
    const string & pt_id,
    const string & parent_id
)
```


**Parameters**: 

  * **pt_id** string ParmContainer ID of desired routing point 
  * **parent_id** string Geom ID for the geom to anchor the routing point to 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelAllRoutingPt](Namespaces/namespacevsp.md#function-delallroutingpt), [GetAllRoutingPtIds](Namespaces/namespacevsp.md#function-getallroutingptids)

Set the Geom ID of the geom a routing point is anchored to. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

SetRoutingPtParentID(rpt1, pod1);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

vsp.SetRoutingPtParentID(rpt1, pod1)
```

  


### function GetMainRoutingPtCoord

```cpp
vec3d GetMainRoutingPtCoord(
    const string & pt_id
)
```


**Parameters**: 

  * **pt_id** string ParmContainer ID of desired routing point 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt), [GetRoutingPtCoord](Namespaces/namespacevsp.md#function-getroutingptcoord), [GetAllRoutingPtCoords](Namespaces/namespacevsp.md#function-getallroutingptcoords), [GetRoutingCurve](Namespaces/namespacevsp.md#function-getroutingcurve)

**Return**: vec3d coordinate of main routing point 

Get the main coordinate location a routing point. The main location is the location of the base copy before symmetry has been applied. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

Update();
vec3d p1 = GetMainRoutingPtCoord(rpt1);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

vsp.Update()
p1 = vsp.GetMainRoutingPtCoord(rpt1)
```

  


### function GetRoutingPtCoord

```cpp
vec3d GetRoutingPtCoord(
    const string & routing_id,
    int index,
    int symm_index
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **index** int Index of routing point to get cordinate of 
  * **symm_index** int Symmetry index to get coordinate of 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt), [GetMainRoutingPtCoord](Namespaces/namespacevsp.md#function-getmainroutingptcoord), [GetAllRoutingPtCoords](Namespaces/namespacevsp.md#function-getallroutingptcoords), [GetRoutingCurve](Namespaces/namespacevsp.md#function-getroutingcurve)

**Return**: vec3d coordinate of routing point 

Get the coordinate location a routing point in a RoutingGeom. The main location is symm_index = 0. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

Update();
vec3d p1 = GetRoutingPtCoord(routing_geom, 1, 0);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

vsp.Update()
p1 = vsp.GetRoutingPtCoord(rpt1, 1, 0)
```

  


### function GetAllRoutingPtCoords

```cpp
vector< vec3d > GetAllRoutingPtCoords(
    const string & routing_id,
    int symm_index
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **symm_index** int Symmetry index to get coordinate of 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt), [GetMainRoutingPtCoord](Namespaces/namespacevsp.md#function-getmainroutingptcoord), [GetRoutingPtCoord](Namespaces/namespacevsp.md#function-getroutingptcoord), [GetRoutingCurve](Namespaces/namespacevsp.md#function-getroutingcurve)

**Return**: vector < vec3d > coordinate of routing points along RoutingGeom 

Get the coordinate locations along a RoutingGeom. The main copy is symm_index = 0. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

Update();
array<vec3d> pvec = GetAllRoutingPtCoords(routing_geom, 0);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

vsp.Update()
pvec = vsp.GetAllRoutingPtCoords(rpt1, 0)
```

  


### function GetRoutingCurve

```cpp
vector< vec3d > GetRoutingCurve(
    const string & routing_id,
    int symm_index
)
```


**Parameters**: 

  * **routing_id** string RoutingGeom Geom ID 
  * **symm_index** int Symmetry index to get coordinate of 


**See**: [AddRoutingPt](Namespaces/namespacevsp.md#function-addroutingpt), [DelRoutingPt](Namespaces/namespacevsp.md#function-delroutingpt), [GetMainRoutingPtCoord](Namespaces/namespacevsp.md#function-getmainroutingptcoord), [GetRoutingPtCoord](Namespaces/namespacevsp.md#function-getroutingptcoord), [GetAllRoutingPtCoords](Namespaces/namespacevsp.md#function-getallroutingptcoords)

**Return**: vector < vec3d > coordinate of points along RoutingGeom curve 

Get points along a RoutingGeom. These points will follow the curve of a RoutingGeom with radiused routing points. The main copy is symm_index = 0. 

string pod1 = AddGeom("POD", "");

string pod2 = AddGeom("POD", "");
string ypod2 = GetParm(pod2, "Y_Rel_Location", "XForm");
SetParmVal(ypod2, 2.0);

string routing_geom = AddGeom("ROUTING", "");

string rpt0 = AddRoutingPt(routing_geom, pod1, 0);
string u0 = GetParm( rpt0, "U", "RoutePt");
SetParmVal(u0, 0.0);

string rpt1 = AddRoutingPt(routing_geom, pod2, 0);

string rpt2 = AddRoutingPt(routing_geom, pod1, 0);
string u2 = GetParm( rpt2, "U", "RoutePt");
SetParmVal(u2, 1.0);

Update();
array<vec3d> pvec = GetRoutingCurve(routing_geom, 0);
```

 \endforcpponly \beginPythonOnly ```py

pod1 = vsp.AddGeom('POD', '')

pod2 = vsp.AddGeom('POD', '')
ypod2 = vsp.GetParm(pod2, 'Y_Rel_Location', 'XForm')
vsp.SetParmVal(ypod2, 2.0)

routing_geom = vsp.AddGeom('ROUTING', '')

rpt0 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u0 = vsp.GetParm( rpt0, 'U', 'RoutePt')
vsp.SetParmVal(u0, 0.0)

rpt1 = vsp.AddRoutingPt(routing_geom, pod2, 0)

rpt2 = vsp.AddRoutingPt(routing_geom, pod1, 0)
u2 = vsp.GetParm( rpt2, 'U', 'RoutePt')
vsp.SetParmVal(u2, 1.0)

vsp.Update()
pvec = vsp.GetRoutingCurve(rpt1, 0)
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800