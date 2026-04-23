---
title: GuiInterface

---

# GuiInterface






`#include <GuiInterface.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| [GuiInterface](Classes/class_gui_interface.md) & | **[getInstance](Classes/class_gui_interface.md#function-getinstance)**() |
| void | **[InitGUI](Classes/class_gui_interface.md#function-initgui)**(Vehicle * vPtr) |
| void | **[StartGUI](Classes/class_gui_interface.md#function-startgui)**() |
| void | **[StartGUIAPI](Classes/class_gui_interface.md#function-startguiapi)**() |
| void | **[StopGUI](Classes/class_gui_interface.md#function-stopgui)**() |
| void | **[PopupMsg](Classes/class_gui_interface.md#function-popupmsg)**(const std::string & message) |
| void | **[UpdateGUI](Classes/class_gui_interface.md#function-updategui)**() |
| void | **[Lock](Classes/class_gui_interface.md#function-lock)**() |
| void | **[Unlock](Classes/class_gui_interface.md#function-unlock)**() |
| bool | **[IsEventLoopRunning](Classes/class_gui_interface.md#function-iseventlooprunning)**() const |
| void | **[ScreenGrab](Classes/class_gui_interface.md#function-screengrab)**(const std::string & fname, int w, int h, bool transparentBG, bool autocrop) |
| void | **[SetViewAxis](Classes/class_gui_interface.md#function-setviewaxis)**(bool vaxis) |
| void | **[SetShowBorders](Classes/class_gui_interface.md#function-setshowborders)**(bool brdr) |
| void | **[SetBackground](Classes/class_gui_interface.md#function-setbackground)**(double r, double g, double b) |
| void | **[SetAllViews](Classes/class_gui_interface.md#function-setallviews)**(int view) |
| void | **[SetView](Classes/class_gui_interface.md#function-setview)**(int viewport, int view) |
| void | **[FitAllViews](Classes/class_gui_interface.md#function-fitallviews)**() |
| void | **[ResetViews](Classes/class_gui_interface.md#function-resetviews)**() |
| void | **[SetWindowLayout](Classes/class_gui_interface.md#function-setwindowlayout)**(int r, int c) |
| void | **[EnableStopGUIMenuItem](Classes/class_gui_interface.md#function-enablestopguimenuitem)**() |
| void | **[DisableStopGUIMenuItem](Classes/class_gui_interface.md#function-disablestopguimenuitem)**() |
| void | **[SetGUIElementDisable](Classes/class_gui_interface.md#function-setguielementdisable)**(int e, bool state) |
| void | **[SetGUIScreenDisable](Classes/class_gui_interface.md#function-setguiscreendisable)**(int s, bool state) |
| void | **[SetGeomScreenDisable](Classes/class_gui_interface.md#function-setgeomscreendisable)**(int s, bool state) |
| void | **[HideScreen](Classes/class_gui_interface.md#function-hidescreen)**(int s) |
| void | **[ShowScreen](Classes/class_gui_interface.md#function-showscreen)**(int s) |

## Public Functions Documentation

### function getInstance

```cpp
static inline GuiInterface & getInstance()
```


### function InitGUI

```cpp
void InitGUI(
    Vehicle * vPtr
)
```


### function StartGUI

```cpp
void StartGUI()
```


### function StartGUIAPI

```cpp
void StartGUIAPI()
```


### function StopGUI

```cpp
void StopGUI()
```


### function PopupMsg

```cpp
void PopupMsg(
    const std::string & message
)
```


### function UpdateGUI

```cpp
void UpdateGUI()
```


### function Lock

```cpp
void Lock()
```


### function Unlock

```cpp
void Unlock()
```


### function IsEventLoopRunning

```cpp
bool IsEventLoopRunning() const
```


### function ScreenGrab

```cpp
void ScreenGrab(
    const std::string & fname,
    int w,
    int h,
    bool transparentBG,
    bool autocrop
)
```


### function SetViewAxis

```cpp
void SetViewAxis(
    bool vaxis
)
```


### function SetShowBorders

```cpp
void SetShowBorders(
    bool brdr
)
```


### function SetBackground

```cpp
void SetBackground(
    double r,
    double g,
    double b
)
```


### function SetAllViews

```cpp
void SetAllViews(
    int view
)
```


### function SetView

```cpp
void SetView(
    int viewport,
    int view
)
```


### function FitAllViews

```cpp
void FitAllViews()
```


### function ResetViews

```cpp
void ResetViews()
```


### function SetWindowLayout

```cpp
void SetWindowLayout(
    int r,
    int c
)
```


### function EnableStopGUIMenuItem

```cpp
void EnableStopGUIMenuItem()
```


### function DisableStopGUIMenuItem

```cpp
void DisableStopGUIMenuItem()
```


### function SetGUIElementDisable

```cpp
void SetGUIElementDisable(
    int e,
    bool state
)
```


### function SetGUIScreenDisable

```cpp
void SetGUIScreenDisable(
    int s,
    bool state
)
```


### function SetGeomScreenDisable

```cpp
void SetGeomScreenDisable(
    int s,
    bool state
)
```


### function HideScreen

```cpp
void HideScreen(
    int s
)
```


### function ShowScreen

```cpp
void ShowScreen(
    int s
)
```


-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800