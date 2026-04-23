---
title: Modules

---

# Modules




* **group [API Error Functions](Modules/group___a_p_i_error.md)** <br>Handling of OpenVSP ErrorObj information is accomplished through this group of API functions. Click here to return to the main page. 
* **group [General API Utility Functions](Modules/group___a_p_i_utilities.md)** <br>This group of functions is provided for general API utilities, such as printing to stdout, performing basic math functions, and identifying basic OpenVSP information. Click here to return to the main page. 
* **group [Advanced Link Functions](Modules/group___advanced_link.md)** <br>The following functions are available for the Advanced Link tool. Click here to return to the main page. 
* **group [Analysis Manager Functions](Modules/group___analysis.md)** <br>This group is for functions included in the Analysis Manager. The Analysis Manager allows for OpenVSP analyses to be setup and run through the API without having to modify Parms directly. Examples are available for every available analysis type. The results of running an analysis can be accessed through the functions defined in the Results group. Click here to return to the main page. 
* **group [Attributes Manager Functions](Modules/group___attributes.md)** <br>This group is for functions included in the Attributes Manager. The Attributes Manager stores Attributes and provides methods to add, delete, get and set them. Click here to return to the main page. 
* **group [BOR Functions](Modules/group___b_o_r.md)** <br>This group of API functions provides capabilities related to the body of revolution (BOR) geometry type in OpenVSP. Click here to return to the main page. 
* **group [Background3D Functions](Modules/group___background3_d.md)** <br>This group of functions is used to work with 3D background images. Click here to return to the main page. 
* **group [CFD Mesh Functions](Modules/group___c_f_d_mesh.md)** <br>This group of functions is used to setup and run the CFD Mesh tool through the API. Click here to return to the main page. 
* **group [VSPAERO Control Surface Group Functions](Modules/group___c_s_group.md)** <br>This group of functions is available for manipulating VSPAERO control surface groups through the API. Note, VSPAERO also includes rectangle type sub-surfaces as possible control surfaces. Click here to return to the main page. 
* **group [General Computation Functions](Modules/group___computations.md)** <br>The following group of API functions are available for general computations. In general, it is best practice to perform computations through the the Analysis group instead of calling these functions directly. Click here to return to the main page. 
* **group [Custom Geometry Functions](Modules/group___custom_geom.md)** <br>This functions grouped here are used to create and manipulate Custom Components. Custom components are defined in *.vsppart files included in the /"Custom Scripts/" directory. Examples of Custom Components are available in the directory for reference. OpenVSP looks in 3 locations for the /"Custom Scripts/" folder, where Custom Components are loaded: the root directory, the VSP executable directory, and the home directory. Note, these functions are specific to defining Custom Components and can't be called from standard API scripts (i.e. *.vspscript). However, a Custom Component can be created as a *.vsppart file and then accessed through secondary API scripts. Click here to return to the main page. 
* **group [Design File Functions](Modules/group___design_file.md)** <br>This group of functions is available for managing Design Variables through the API. Click here to return to the main page. 
* **group [Edit Curve XSec Functions](Modules/group___edit_curve_x_sec.md)** <br>Functions for modifying XSecs of type XS_EDIT_CURVE are defined here. Click here to return to the main page. 
* **group [Enumerations](Modules/group___enumerations.md)** <br>All API enumerations are defined in this group. Click here to return to the main page. 
* **group [FEA Mesh Functions](Modules/group___f_e_a_mesh.md)** <br>The following group of API functions supports all functionality of the FEA Mesh Tool. Structures, FEA Parts, materials, and properties can be defined and manipulated. Mesh and output file settings can be adjusted, and an FEA mesh can be generated. Click here to return to the main page. 
* **group [File Input and Output Functions](Modules/group___file_i_o.md)** <br>This group of functions provides file input and output interfacing through the API. Click here to return to the main page. 
* **group [Geom Functions](Modules/group___geom.md)** <br>This group of functions is available for adding, deleting, and modifying OpenVSP Geoms through the API. Click here to return to the main page. 
* **group [Group Modification Functions](Modules/group___group_mod.md)** <br>The functions in this group allow for sets to be scaled, rotated, and translated. Click here to return to the main page. 
* **group [Matrix4d Functions](Modules/group___matrix4d.md)** <br>API functions that utilize the Matrix4d class are grouped here. For details of the class, including member functions, see Matrix4d. Click here to return to the main page. 
* **group [Measure Tool Functions](Modules/group___measure.md)** <br>This group of API functions can be used to control the Ruler Tool through the API. Click here to return to the main page. 
* **group [Mode Functions](Modules/group___mode.md)** <br>This group of API functions are used to manipulate Modes &ndash; a combination of Sets and Variable Presets Click here to return to the main page. 
* **group [Propeller Blade Curve Functions](Modules/group___p_curve.md)** <br>The following group of API functions may be used to control parametric propeller blade curves (PCurves). Click here to return to the main page. 
* **group [Parasite Drag Functions](Modules/group___parasite_drag.md)** <br>This group of API functions is supplemental to performing a Paraste Drag analysis through the Analysis Manager. They include functions to write out Parasite Drag Tool equations, calculate atmospheric properties, and control excrescences. Click here to return to the main page. 
* **group [Parm Functions](Modules/group___parm.md)** <br>Every Parm in OpenVSP can be accessed and modified through the functions defined in this API group. Every Parm has an associated ParmContainer. Click here to return to the main page. 
* **group [Parm Container Functions](Modules/group___parm_container.md)** <br>All Parms in OpenVSP are stored in Parm Containers. The functions in this group can be used to work with Parm Containers through the API. Click here to return to the main page. 
* **group [API Proxy Utility Functions](Modules/group___proxy_utitity.md)** <br>The API functions defined in this group enable conversion between AngelScript and OpenVSP C++ data types, such as array and vector. Click here to return to the main page. 
* **group [Results Manager Functions](Modules/group___results.md)** <br>This group is for functions included in the Results Manager. The Results Manager stores analysis results and provides methods to get, print, and export them. Click here to return to the main page. 
* **group [Functions for Sets](Modules/group___sets.md)** <br>The following group of API functions deals with set manipulation. Click here to return to the main page. 
* **group [Snap-To Functions](Modules/group___snap_to.md)** <br>This group of API functions provide the capabilities available in the Snap-To tool. Click here to return to the main page. 
* **group [Sub-Surface Functions](Modules/group___sub_surface.md)** <br>Functions related to Sub-Surfaces are defined in this group. Click here to return to the main page. 
* **group [Geom Surface Query Functions](Modules/group___surface_query.md)** <br>This group of API functions pertains to general surface queries for Geom surfaces, such as computing 3D location from surface coordinates, identifying curvature, and performing point projections. Click here to return to the main page. 
* **group [VSPAERO Functions](Modules/group___v_s_p_a_e_r_o.md)** <br>The following group of functions are specific to VSPAERO. However, their relevance has been mostly replaced by Analysis Manager capabilities. Click here to return to the main page. 
* **group [VSPAERO Actuator Disk and Propeller Functions](Modules/group___v_s_p_a_e_r_o_disk_and_prop.md)** <br>The following group of functions provide API capability for setting up actuator disks (Disk tab of VSPAERO GUI) and propellers (Propeller tab of VSPAERO GUI) for VSPAERO analysis. If a propeller geometry is used to model the actuator disk, the "PropMode" must be set to PROP_DISK or PROP_BOTH. Alternatively, the "PropMode" but be set to PROP_BLADE or PROP_BOTH for unsteady analysis. must be set to PROP_DISK or PROP_BOTH. Click here to return to the main page. 
* **group [Variable Preset Functions](Modules/group___variable_preset.md)** <br>This group of functions can be used to add, remove, and modify Variable Presets through the API. Click here to return to the main page. 
* **group [Vehicle Functions](Modules/group___vehicle.md)** <br>The Vehicle group of functions are high-level commands that pertain to the entire OpenVSP model. Click here to return to the main page. 
* **group [Visualization Functions](Modules/group___visualization.md)** <br>The following group of functions allow for the OpenVSP GUI to be manipulated through the API. Click here to return to the main page. 
* **group [XSec and Airfoil Functions](Modules/group___x_sec.md)** <br>This group of functions provides API control of cross-sections (XSecs). Airfoils are a type of XSec included in this group as well. API functions for Body of Revolution XSecs are included in the Specialized Geometry group. Click here to return to the main page. 
* **group [XSecSurf Functions](Modules/group___x_sec_surf.md)** <br>This group of API functions provides capabilities related to the XSecSurf class in OpenVSP. Click here to return to the main page. 
* **group [Vec3D Functions](Modules/group__vec3d.md)** <br>API functions that utilize the vec3d class are grouped here. For details of the class, including member functions, see vec3d. Click here to return to the main page. 



-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800
