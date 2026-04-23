---
title: Measure Tool Functions
summary: This group of API functions can be used to control the Ruler Tool through the API. Click here to return to the main page. 

---

# Measure Tool Functions

This group of API functions can be used to control the Ruler Tool through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| string | **[AddRuler](Modules/group___measure.md#function-addruler)**(const string & startgeomid, int startsurfindx, double startu, double startw, const string & endgeomid, int endsurfindx, double endu, double endw, const string & name) |
| std::vector< string > | **[GetAllRulers](Modules/group___measure.md#function-getallrulers)**() |
| void | **[DelRuler](Modules/group___measure.md#function-delruler)**(const string & id) |
| void | **[DeleteAllRulers](Modules/group___measure.md#function-deleteallrulers)**() |
| string | **[AddProbe](Modules/group___measure.md#function-addprobe)**(const string & geomid, int surfindx, double u, double w, const string & name) |
| std::vector< string > | **[GetAllProbes](Modules/group___measure.md#function-getallprobes)**() |
| void | **[DelProbe](Modules/group___measure.md#function-delprobe)**(const string & id) |
| void | **[DeleteAllProbes](Modules/group___measure.md#function-deleteallprobes)**() |


## Functions Documentation

### function AddRuler

```
string AddRuler(
    const string & startgeomid,
    int startsurfindx,
    double startu,
    double startw,
    const string & endgeomid,
    int endsurfindx,
    double endu,
    double endw,
    const string & name
)
```


**Parameters**: 

  * **startgeomid** string Start parent Geom ID 
  * **startsurfindx** int Main surface index from the staring parent Geom 
  * **startu** double Surface u (0 - 1) start coordinate 
  * **startw** double Surface w (0 - 1) start coordinate 
  * **endgeomid** string End parent Geom ID 
  * **endsurfindx** int Main surface index on the end parent Geom 
  * **endu** double Surface u (0 - 1) end coordinate 
  * **endw** double Surface w (0 - 1) end coordinate 
  * **name** string Ruler name 


**Return**: string Ruler ID 

Create a new Ruler and add it to the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string pid2 = AddGeom( "POD", "" );

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 );

string rid = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" );

SetParmVal( FindParm( rid, "X_Offset", "Measure" ), 6.0 );
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

pid2 = AddGeom( "POD", "" )

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 )

rid = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" )

SetParmVal( FindParm( rid, "X_Offset", "Measure" ), 6.0 )
```

  


### function GetAllRulers

```
std::vector< string > GetAllRulers()
```


**Return**: vector<string> Vector of Ruler IDs 

Get an array of all Ruler IDs from the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string pid2 = AddGeom( "POD", "" );

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 );

string rid1 = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" );

string rid2 = AddRuler( pid1, 0, 0.4, 0.6, pid1, 1, 0.8, 0.9, "Ruler 2" );

array< string > @ruler_array = GetAllRulers();

Print("Two Rulers");

for( int n = 0 ; n < int( ruler_array.length() ) ; n++ )
{
    Print( ruler_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

pid2 = AddGeom( "POD", "" )

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 )

rid1 = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" )

rid2 = AddRuler( pid1, 0, 0.4, 0.6, pid1, 1, 0.8, 0.9, "Ruler 2" )

ruler_array = GetAllRulers()

print("Two Rulers")

for n in range(len(ruler_array)):

    print( ruler_array[n] )
```

  


### function DelRuler

```
void DelRuler(
    const string & id
)
```


**Parameters**: 

  * **id** string Ruler ID 


Delete a particular Ruler from the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string pid2 = AddGeom( "POD", "" );

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 );

string rid1 = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" );

string rid2 = AddRuler( pid1, 0, 0.4, 0.6, pid1, 1, 0.8, 0.9, "Ruler 2" );

array< string > @ruler_array = GetAllRulers();

DelRuler( ruler_array[0] );
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

pid2 = AddGeom( "POD", "" )

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 )

rid1 = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" )

rid2 = AddRuler( pid1, 0, 0.4, 0.6, pid1, 1, 0.8, 0.9, "Ruler 2" )

ruler_array = GetAllRulers()

DelRuler( ruler_array[0] )
```

  


### function DeleteAllRulers

```
void DeleteAllRulers()
```


Delete all Rulers from the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string pid2 = AddGeom( "POD", "" );

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 );

string rid1 = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" );

string rid2 = AddRuler( pid1, 0, 0.4, 0.6, pid1, 1, 0.8, 0.9, "Ruler 2" );

DeleteAllRulers();
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

pid2 = AddGeom( "POD", "" )

SetParmVal( pid2, "Z_Rel_Location", "XForm", 4.0 )

rid1 = AddRuler( pid1, 1, 0.2, 0.3, pid2, 0, 0.2, 0.3, "Ruler 1" )

rid2 = AddRuler( pid1, 0, 0.4, 0.6, pid1, 1, 0.8, 0.9, "Ruler 2" )

DeleteAllRulers()
```

  


### function AddProbe

```
string AddProbe(
    const string & geomid,
    int surfindx,
    double u,
    double w,
    const string & name
)
```


**Parameters**: 

  * **geomid** string Parent Geom ID 
  * **surfindx** int Main surface index from the parent Geom 
  * **u** double Surface u (0 - 1) coordinate 
  * **w** double Surface w (0 - 1) coordinate 
  * **name** string Probe name 


**Return**: string Probe ID 

Create a new Probe and add it to the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string probe_id = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" );

SetParmVal( FindParm( probe_id, "Len", "Measure" ), 3.0 );
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

probe_id = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" )

SetParmVal( FindParm( probe_id, "Len", "Measure" ), 3.0 )
```

  


### function GetAllProbes

```
std::vector< string > GetAllProbes()
```


**Return**: [in] Array of Probe IDs 

Get an array of all Probe IDs from the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string probe_id = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" );

array< string > @probe_array = GetAllProbes();

Print( "One Probe: ", false );

Print( probe_array[0] );
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

probe_id = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" )

probe_array = GetAllProbes()

print( "One Probe: ", False )

print( probe_array[0] )
```

  


### function DelProbe

```
void DelProbe(
    const string & id
)
```


**Parameters**: 

  * **id** Probe ID 


Delete a specific Probe from the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string probe_id_1 = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" );
string probe_id_2 = AddProbe( pid1, 0, 0.2, 0.3, "Probe 2" );

DelProbe( probe_id_1 );

array< string > @probe_array = GetAllProbes();

if ( probe_array.size() != 1 ) { Print( "Error: DelProbe" ); }
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

probe_id_1 = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" )
probe_id_2 = AddProbe( pid1, 0, 0.2, 0.3, "Probe 2" )

DelProbe( probe_id_1 )

probe_array = GetAllProbes()

if  len(probe_array) != 1 : print( "Error: DelProbe" )
```

  


### function DeleteAllProbes

```
void DeleteAllProbes()
```


Delete all Probes from the Measure Tool 

string pid1 = AddGeom( "POD", "" );

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 );

string probe_id_1 = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" );
string probe_id_2 = AddProbe( pid1, 0, 0.2, 0.3, "Probe 2" );

DeleteAllProbes();

array< string > @probe_array = GetAllProbes();

if ( probe_array.size() != 0 ) { Print( "Error: DeleteAllProbes" ); }
```

 \endforcpponly \beginPythonOnly ```py

pid1 = AddGeom( "POD", "" )

SetParmVal( pid1, "Y_Rel_Location", "XForm", 2.0 )

probe_id_1 = AddProbe( pid1, 0, 0.5, 0.8, "Probe 1" )
probe_id_2 = AddProbe( pid1, 0, 0.2, 0.3, "Probe 2" )

DeleteAllProbes()

probe_array = GetAllProbes()

if  len(probe_array) != 0 : print( "Error: DeleteAllProbes" )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800