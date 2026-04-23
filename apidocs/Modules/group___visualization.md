---
title: Visualization Functions
summary: The following group of functions allow for the OpenVSP GUI to be manipulated through the API. Click here to return to the main page. 

---

# Visualization Functions

The following group of functions allow for the OpenVSP GUI to be manipulated through the API. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[InitGUI](Modules/group___visualization.md#function-initgui)**() |
| void | **[StartGUI](Modules/group___visualization.md#function-startgui)**() |
| void | **[EnableStopGUIMenuItem](Modules/group___visualization.md#function-enablestopguimenuitem)**() |
| void | **[DisableStopGUIMenuItem](Modules/group___visualization.md#function-disablestopguimenuitem)**() |
| void | **[StopGUI](Modules/group___visualization.md#function-stopgui)**() |
| void | **[PopupMsg](Modules/group___visualization.md#function-popupmsg)**(const std::string & msg) |
| void | **[UpdateGUI](Modules/group___visualization.md#function-updategui)**() |
| bool | **[IsGUIBuild](Modules/group___visualization.md#function-isguibuild)**() |
| void | **[Lock](Modules/group___visualization.md#function-lock)**() |
| void | **[Unlock](Modules/group___visualization.md#function-unlock)**() |
| bool | **[IsEventLoopRunning](Modules/group___visualization.md#function-iseventlooprunning)**() |
| void | **[ScreenGrab](Modules/group___visualization.md#function-screengrab)**(const string & fname, int w, int h, bool transparentBG, bool autocrop =false) |
| void | **[SetViewAxis](Modules/group___visualization.md#function-setviewaxis)**(bool vaxis) |
| void | **[SetShowBorders](Modules/group___visualization.md#function-setshowborders)**(bool brdr) |
| void | **[SetGeomDrawType](Modules/group___visualization.md#function-setgeomdrawtype)**(const string & geom_id, int type) |
| void | **[SetGeomWireColor](Modules/group___visualization.md#function-setgeomwirecolor)**(const string & geom_id, int r, int g, int b) |
| void | **[SetGeomDisplayType](Modules/group___visualization.md#function-setgeomdisplaytype)**(const string & geom_id, int type) |
| void | **[SetGeomMaterialName](Modules/group___visualization.md#function-setgeommaterialname)**(const string & geom_id, const string & name) |
| void | **[AddMaterial](Modules/group___visualization.md#function-addmaterial)**(const string & name, const [vec3d](Classes/classvec3d.md) & ambient, const [vec3d](Classes/classvec3d.md) & diffuse, const [vec3d](Classes/classvec3d.md) & specular, const [vec3d](Classes/classvec3d.md) & emissive, const double & alpha, const double & shininess) |
| vector< string > | **[GetMaterialNames](Modules/group___visualization.md#function-getmaterialnames)**() |
| void | **[SetBackground](Modules/group___visualization.md#function-setbackground)**(double r, double g, double b) |
| void | **[SetAllViews](Modules/group___visualization.md#function-setallviews)**(int view) |
| void | **[SetView](Modules/group___visualization.md#function-setview)**(int viewport, int view) |
| void | **[FitAllViews](Modules/group___visualization.md#function-fitallviews)**() |
| void | **[ResetViews](Modules/group___visualization.md#function-resetviews)**() |
| void | **[SetWindowLayout](Modules/group___visualization.md#function-setwindowlayout)**(int r, int c) |
| void | **[SetGUIElementDisable](Modules/group___visualization.md#function-setguielementdisable)**(int e, bool state) |
| void | **[SetGUIScreenDisable](Modules/group___visualization.md#function-setguiscreendisable)**(int s, bool state) |
| void | **[SetGeomScreenDisable](Modules/group___visualization.md#function-setgeomscreendisable)**(int s, bool state) |
| void | **[HideScreen](Modules/group___visualization.md#function-hidescreen)**(int s) |
| void | **[ShowScreen](Modules/group___visualization.md#function-showscreen)**(int s) |


## Functions Documentation

### function InitGUI

```
void InitGUI()
```


Low level routine that should be called to set up GUI before running [StartGUI()](Modules/group___visualization.md#function-startgui) 

InitGUI();
```

 

InitGUI()
```

  


### function StartGUI

```
void StartGUI()
```


Launch the interactive OpenVSP GUI. In a multi-threaded environment, this must be called from the main thread only. This starts the GUI event loop. It will also show the main screen and screens displayed when [StopGUI()](Modules/group___visualization.md#function-stopgui) was previously called. 

StartGUI();
```

 

StartGUI()
```

  


### function EnableStopGUIMenuItem

```
void EnableStopGUIMenuItem()
```


**See**: [DisableStopGUIMenuItem](Modules/group___visualization.md#function-disablestopguimenuitem)

Enable Stop GUI Menu Item from the OpenVSP GUI.

Typically used for the blocking-mode OpenVSP GUI from the API.

This will add a "Stop GUI" option to the file pulldown menu and will also cause the exit button on the window frame to have the same effect. When selected, these options will stop the OpenVSP GUI event loop, returning control to the API program. OpenVSP will not terminate, the model will remain in memory and will be responsive to subsequent API calls.



EnableStopGUIMenuItem();
StartGUI();
```

 

EnableStopGUIMenuItem()
StartGUI()
```

 


### function DisableStopGUIMenuItem

```
void DisableStopGUIMenuItem()
```


**See**: [EnableStopGUIMenuItem](Modules/group___visualization.md#function-enablestopguimenuitem)

Disable Stop GUI Menu Item from the OpenVSP GUI.

This reverses the operation of EnableStopGUIMenuItem.



EnableStopGUIMenuItem();
StartGUI();
```

 

EnableStopGUIMenuItem()
DisableStopGUIMenuItem()
StartGUI()
```

 


### function StopGUI

```
void StopGUI()
```


**See**: [StartGUI](Modules/group___visualization.md#function-startgui)

Stop OpenVSP GUI event loop and hide screens. Keep OpenVSP running and in memory. 

StartGUI();

StopGUI();

StartGUI();
```

 

StartGUI()

StopGUI()

StartGUI()
```

 


### function PopupMsg

```
void PopupMsg(
    const std::string & msg
)
```


**Parameters**: 

  * **msg** string Message to display. 


Cause OpenVSP to display a popup message. 

StartGUI();

PopupMsg( "This is a popup message." );
```

 

StartGUI()

PopupMsg( "This is a popup message." )
```

 


### function UpdateGUI

```
void UpdateGUI()
```


**See**: [StartGUI](Modules/group___visualization.md#function-startgui)

Tell OpenVSP that the GUI needs to be updated. 

StartGUI();

string pod_id = AddGeom( "POD" );

string length = FindParm( pod_id, "Length", "Design" );

SetParmVal( length, 13.0 );

UpdateGUI();
```

 

StartGUI()

pod_id = AddGeom( "POD" )

length = FindParm( pod_id, "Length", "Design" )

SetParmVal( length, 13.0 )

UpdateGUI()
```

 


### function IsGUIBuild

```
bool IsGUIBuild()
```


**Return**: bool True if the current OpenVSP build includes graphics capabilities. False otherwise. 

Test if the current OpenVSP build includes graphics capabilities. 

if ( IsGUIBuild() )
{
    Print( "OpenVSP build is graphics capable." );
}
else
{
    Print( "OpenVSP build is not graphics capable." );
}
```

 

if ( IsGUIBuild() ):
    print( "OpenVSP build is graphics capable." )
else:
    print( "OpenVSP build is not graphics capable." )
```

 


### function Lock

```
void Lock()
```


**See**: [Unlock](Modules/group___visualization.md#function-unlock)

Obtain the lock on the OpenVSP GUI event loop. This will prevent the interactive GUI from updating or accepting user input until the lock is released &ndash; thereby allowing longer-time commands including analyses to execute without the chance of the OpenVSP state changing during execution.



StartGUI();

string pod_id = AddGeom( "POD" );

Lock();
string rid = ExecAnalysis( "CompGeom" );

array<string>@ mesh_id_vec = GetStringResults( rid, "Mesh_GeomID" );

DeleteGeomVec( mesh_id_vec );
Unlock();
```

 

StartGUI()

pod_id = AddGeom( "POD" )

Lock()
rid = ExecAnalysis( "CompGeom" )

mesh_id_vec = GetStringResults( rid, "Mesh_GeomID" )

DeleteGeomVec( mesh_id_vec )
Unlock()
```

 


### function Unlock

```
void Unlock()
```


**See**: [Lock](Modules/group___visualization.md#function-lock)

Release the lock on the OpenVSP GUI event loop.



StartGUI();

string pod_id = AddGeom( "POD" );

Lock();
string rid = ExecAnalysis( "CompGeom" );

array<string>@ mesh_id_vec = GetStringResults( rid, "Mesh_GeomID" );

DeleteGeomVec( mesh_id_vec );
Unlock();
```

 

StartGUI()

pod_id = AddGeom( "POD" )

Lock()
rid = ExecAnalysis( "CompGeom" )

mesh_id_vec = GetStringResults( rid, "Mesh_GeomID" )

DeleteGeomVec( mesh_id_vec )
Unlock()
```

 


### function IsEventLoopRunning

```
bool IsEventLoopRunning()
```


**Return**: bool True if the OpenVSP GUI event loop is running. False otherwise. 

Test if the OpenVSP GUI event loop is running.



StartGUI();

if ( IsEventLoopRunning() )
{
    Print( "Event loop is running." );
}
```

 

StartGUI()

if ( IsEventLoopRunning() ):
    print( "Event loop is running." )
```

  


### function ScreenGrab

```
void ScreenGrab(
    const string & fname,
    int w,
    int h,
    bool transparentBG,
    bool autocrop =false
)
```


**Parameters**: 

  * **fname** string Output file name 
  * **w** int Width of screen grab 
  * **h** int Height of screen grab 
  * **transparentBG** bool Transparent background flag 
  * **autocrop** bool Automatically crop transparent background flag 


Capture the specified screen and save to file. Note, VSP_USE_FLTK must be defined 

int screenw = 2000;                                             // Set screenshot width and height
int screenh = 2000;

string fname = "test_screen_grab.png";

ScreenGrab( fname, screenw, screenh, true, true );                // Take PNG screenshot
```

 

screenw = 2000                                             # Set screenshot width and height
screenh = 2000

fname = "test_screen_grab.png"

ScreenGrab( fname, screenw, screenh, True, True )                # Take PNG screenshot
```

  


### function SetViewAxis

```
void SetViewAxis(
    bool vaxis
)
```


**Parameters**: 

  * **vaxis** True to show the axis, false to hide the axis 


Toggle viewing the axis 

SetViewAxis( false );                                           // Turn off axis marker in corner of viewscreen
```

 

SetViewAxis( False )                                           # Turn off axis marker in corner of viewscreen
```

  


### function SetShowBorders

```
void SetShowBorders(
    bool brdr
)
```


**Parameters**: 

  * **brdr** True to show the border frame, false to hide the border frame 


Toggle viewing the border frame 

SetShowBorders( false );                                        // Turn off red/black border on active window
```

 

SetShowBorders( False )                                        # Turn off red/black border on active window
```

  


### function SetGeomDrawType

```
void SetGeomDrawType(
    const string & geom_id,
    int type
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **type** Draw type enum (i.e. GEOM_DRAW_SHADE) 


**See**: [DRAW_TYPE](Modules/group___enumerations.md#enum-draw-type)

Set the draw type of the specified geometry 

string pid = AddGeom( "POD", "" );                             // Add Pod for testing

SetGeomDrawType( pid, GEOM_DRAW_SHADE );                       // Make pod appear as shaded
```

 

pid = AddGeom( "POD", "" )                             # Add Pod for testing

SetGeomDrawType( pid, GEOM_DRAW_SHADE )                       # Make pod appear as shaded
```

  


### function SetGeomWireColor

```
void SetGeomWireColor(
    const string & geom_id,
    int r,
    int g,
    int b
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **r** int Red component of color [0, 255] 
  * **g** int Green component of color [0, 255] 
  * **b** int Blue component of color [0, 255] 


Set the wireframe color of the specified geometry 

string pid = AddGeom( "POD", "" );

SetGeomWireColor( pid, 0, 0, 255 );
```

 

pid = AddGeom( "POD", "" )

SetGeomWireColor( pid, 0, 0, 255 )
```

  


### function SetGeomDisplayType

```
void SetGeomDisplayType(
    const string & geom_id,
    int type
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **type** Display type enum (i.e. DISPLAY_BEZIER) 


**See**: [DISPLAY_TYPE](Modules/group___enumerations.md#enum-display-type)

Set the display type of the specified geometry 

string pid = AddGeom( "POD" );                             // Add Pod for testing

SetGeomDisplayType( pid, DISPLAY_DEGEN_PLATE );                       // Make pod appear as Bezier plate (Degen Geom)
```

 

pid = AddGeom( "POD" )                             # Add Pod for testing

SetGeomDisplayType( pid, DISPLAY_DEGEN_PLATE )                       # Make pod appear as Bezier plate (Degen Geom)
```

  


### function SetGeomMaterialName

```
void SetGeomMaterialName(
    const string & geom_id,
    const string & name
)
```


**Parameters**: 

  * **geom_id** string Geom ID 
  * **name** string Material name 


Set the visualization material the specified geometry 

string pid = AddGeom( "POD" );

SetGeomMaterialName( pid, "Ruby" );
```

 

pid = AddGeom( "POD" )

SetGeomMaterialName( pid, "Ruby" )
```

  


### function AddMaterial

```
void AddMaterial(
    const string & name,
    const vec3d & ambient,
    const vec3d & diffuse,
    const vec3d & specular,
    const vec3d & emissive,
    const double & alpha,
    const double & shininess
)
```


**Parameters**: 

  * **name** string Material name 
  * **ambient** [vec3d](Classes/classvec3d.md) Ambient color RGB triple on scale [0, 255] 
  * **diffuse** [vec3d](Classes/classvec3d.md) Diffuse color RGB triple on scale [0, 255] 
  * **specular** [vec3d](Classes/classvec3d.md) Specular color RGB triple on scale [0, 255] 
  * **emissive** [vec3d](Classes/classvec3d.md) Emissive color RGB triple on scale [0, 255] 
  * **shininess** double Shininess exponent on scale [0, 127] 
  * **alpha** double Transparency factor on scale [0, 1] 


Set the visualization material the specified geometry 

string pid = AddGeom( "POD" );

AddMaterial( "RedGlass", vec3d( 44, 2, 2 ), vec3d( 156, 10, 10 ), vec3d( 185, 159, 159 ), vec3d( 44, 2, 2 ), 30, 0.4 );

SetGeomMaterialName( pid, "RedGlass" );
```

 

pid = AddGeom( "POD" )

AddMaterial( "RedGlass", vec3d( 44, 2, 2 ), vec3d( 156, 10, 10 ), vec3d( 185, 159, 159 ), vec3d( 44, 2, 2 ), 30, 0.4 )

SetGeomMaterialName( pid, "RedGlass" )
```

  


### function GetMaterialNames

```
vector< string > GetMaterialNames()
```


**Return**: vector<string> Array of material names 

Get the names of all visualization materials 

array< string > @mat_array = GetMaterialNames();

for ( int i = 0; i < int( mat_array.size() ); i++ )
{
    Print( mat_array[i] );
}
```

 

mat_array = GetMaterialNames()

for i in range(int( len(mat_array) )):
    print( mat_array[i] )
```

  


### function SetBackground

```
void SetBackground(
    double r,
    double g,
    double b
)
```


**Parameters**: 

  * **r** Red 8-bit unsigned integer (range: 0-255) 
  * **g** Green 8-bit unsigned integer (range: 0-255) 
  * **b** Blue 8-bit unsigned integer (range: 0-255) 


Set the background color 

SetBackground( 1.0, 1.0, 1.0 );                                 // Set background to bright white
```

 

SetBackground( 1.0, 1.0, 1.0 )                                 # Set background to bright white
```

  


### function SetAllViews

```
void SetAllViews(
    int view
)
```


**Parameters**: 

  * **view** int [CAMERA_VIEW](Modules/group___enumerations.md#enum-camera-view) enum 


Set the view of all viewports 

SetAllViews( CAM_CENTER );
```

 

SetAllViews( CAM_CENTER )
```

  


### function SetView

```
void SetView(
    int viewport,
    int view
)
```


**Parameters**: 

  * **viewport** int Viewport to set view 
  * **view** int [CAMERA_VIEW](Modules/group___enumerations.md#enum-camera-view) enum 


Set the view of a particular viewports 

SetView( 0, CAM_CENTER );
```

 

SetView( 0, CAM_CENTER )
```

  


### function FitAllViews

```
void FitAllViews()
```


Fit contents to all viewports 

FitAllViews();
```

 

FitAllViews()
```

  


### function ResetViews

```
void ResetViews()
```


Reset views of all viewports 

ResetViews();
```

 

ResetViews()
```

  


### function SetWindowLayout

```
void SetWindowLayout(
    int r,
    int c
)
```


**Parameters**: 

  * **r** int Number of viewport rows 
  * **c** int Number of viewport columns 


Set the rows and columns of the window layout 

SetWindowLayout( 2, 2 );
```

 

SetWindowLayout( 2, 2 )
```

  


### function SetGUIElementDisable

```
void SetGUIElementDisable(
    int e,
    bool state
)
```


**Parameters**: 

  * **e** int [GDEV](Modules/group___enumerations.md#enum-gdev) enum for GUI device type 
  * **state** bool True to disable GUI device type 


Set whether all instances of GUI device type are disabled 

SetGUIElementDisable( GDEV_INPUT, true );
```

 

SetGUIElementDisable( GDEV_INPUT, True )
```

  


### function SetGUIScreenDisable

```
void SetGUIScreenDisable(
    int s,
    bool state
)
```


**Parameters**: 

  * **s** int [GUI_VSP_SCREEN](Modules/group___enumerations.md#enum-gui-vsp-screen) enum for screen 
  * **state** bool True to disable screen 


Set whether screen is disabled 

SetGUIScreenDisable( VSP_CFD_MESH_SCREEN, true );
```

 

SetGUIScreenDisable( VSP_CFD_MESH_SCREEN, True )
```

  


### function SetGeomScreenDisable

```
void SetGeomScreenDisable(
    int s,
    bool state
)
```


**Parameters**: 

  * **s** int [GUI_GEOM_SCREEN](Modules/group___enumerations.md#enum-gui-geom-screen) enum for geom screen 
  * **state** bool True to disable geom screen 


Set whether geom screen is disabled 

SetGeomScreenDisable( ALL_GEOM_SCREENS, true );
```

 

SetGeomScreenDisable( ALL_GEOM_SCREENS, True )
```

  


### function HideScreen

```
void HideScreen(
    int s
)
```


**Parameters**: 

  * **s** int [GUI_VSP_SCREEN](Modules/group___enumerations.md#enum-gui-vsp-screen) enum for screen 


Hide an OpenVSP GUI screen 

HideScreen( VSP_CFD_MESH_SCREEN );
```

 

HideScreen( VSP_CFD_MESH_SCREEN )
```

  


### function ShowScreen

```
void ShowScreen(
    int s
)
```


**Parameters**: 

  * **s** int [GUI_VSP_SCREEN](Modules/group___enumerations.md#enum-gui-vsp-screen) enum for screen 


Show an OpenVSP GUI screen 

ShowScreen( VSP_CFD_MESH_SCREEN );
```

 

ShowScreen( VSP_CFD_MESH_SCREEN )
```

  






-------------------------------

Updated on 2026-04-23 at 15:22:24 +0800