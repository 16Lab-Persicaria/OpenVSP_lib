---
title: Enumerations
summary: All API enumerations are defined in this group. Click here to return to the main page. 

---

# Enumerations

All API enumerations are defined in this group. Click here to return to the main page. 

## Types

|                | Name           |
| -------------- | -------------- |
| enum| **[ABS_REL_FLAG](Modules/group___enumerations.md#enum-abs-rel-flag)** { ABS, REL} |
| enum| **[AIRFOIL_EXPORT_TYPE](Modules/group___enumerations.md#enum-airfoil-export-type)** { SELIG_AF_EXPORT, BEZIER_AF_EXPORT} |
| enum| **[ALIGN_TYPE](Modules/group___enumerations.md#enum-align-type)** { ALIGN_LEFT, ALIGN_CENTER, ALIGN_RIGHT, ALIGN_PIXEL, ALIGN_TOP, ALIGN_MIDDLE, ALIGN_BOTTOM, NUM_ALIGN_TYPE} |
| enum| **[ANG_UNITS](Modules/group___enumerations.md#enum-ang-units)** { ANG_RAD, ANG_DEG} |
| enum| **[ANGLE](Modules/group___enumerations.md#enum-angle)** { ANG_0, ANG_90, ANG_180, ANG_270, NUM_ANG} |
| enum| **[ATMOS_TYPE](Modules/group___enumerations.md#enum-atmos-type)** { ATMOS_TYPE_US_STANDARD_1976 = 0, ATMOS_TYPE_HERRINGTON_1966, ATMOS_TYPE_MANUAL_P_R, ATMOS_TYPE_MANUAL_P_T, ATMOS_TYPE_MANUAL_R_T, ATMOS_TYPE_MANUAL_RE_L} |
| enum| **[ATTACH_TRANS_TYPE](Modules/group___enumerations.md#enum-attach-trans-type)** { ATTACH_TRANS_NONE = 0, ATTACH_TRANS_COMP, ATTACH_TRANS_UV, ATTACH_TRANS_RST, ATTACH_TRANS_LMN, ATTACH_TRANS_EtaMN, ATTACH_TRANS_NUM_TYPES} |
| enum| **[ATTACH_ROT_TYPE](Modules/group___enumerations.md#enum-attach-rot-type)** { ATTACH_ROT_NONE = 0, ATTACH_ROT_COMP, ATTACH_ROT_UV, ATTACH_ROT_RST, ATTACH_ROT_LMN, ATTACH_ROT_EtaMN, ATTACH_ROT_NUM_TYPES} |
| enum| **[ATTRIBUTABLE_TYPE](Modules/group___enumerations.md#enum-attributable-type)** { ATTROBJ_PARM = 0, ATTROBJ_GEOM, ATTROBJ_VEH, ATTROBJ_SUBSURF, ATTROBJ_MEASURE, ATTROBJ_LINK, ATTROBJ_ADVLINK, ATTROBJ_ATTR, ATTROBJ_COLLECTION, ATTROBJ_XSEC, ATTROBJ_SEC, ATTROBJ_MODE, ATTROBJ_SET, ATTROBJ_VARGROUP, ATTROBJ_VARSETTING, ATTROBJ_FREE} |
| enum| **[ATTRIBUTE_EVENT_GROUP](Modules/group___enumerations.md#enum-attribute-event-group)** { ATTR_GROUP_NONE = -1, ATTR_GROUP_WATERMARK, NUM_ATTR_EVENT_GROUPS} |
| enum| **[AUX_GEOM_MODE](Modules/group___enumerations.md#enum-aux-geom-mode)** { AUX_GEOM_ROTOR_TIP_PATH, AUX_GEOM_ROTOR_BURST, AUX_GEOM_THREE_PT_GROUND, AUX_GEOM_TWO_PT_GROUND, AUX_GEOM_ONE_PT_GROUND, AUX_GEOM_THREE_PT_CCE, AUX_GEOM_SUPER_CONE, AUX_GEOM_SINGLE_GEAR, NUM_AUX_GEOM_MODES} |
| enum| **[BOGIE_SPACING_TYPE](Modules/group___enumerations.md#enum-bogie-spacing-type)** { BOGIE_CENTER_DIST, BOGIE_CENTER_DIST_FRAC, BOGIE_GAP, BOGIE_GAP_FRAC, NUM_BOGIE_SPACING_TYPE} |
| enum| **[BOR_MODE](Modules/group___enumerations.md#enum-bor-mode)** { BOR_FLOWTHROUGH, BOR_UPPER, BOR_LOWER, BOR_NUM_MODES} |
| enum| **[CAMBER_INPUT_FLAG](Modules/group___enumerations.md#enum-camber-input-flag)** { MAX_CAMB, DESIGN_CL} |
| enum| **[CAMERA_VIEW](Modules/group___enumerations.md#enum-camera-view)** { CAM_TOP, CAM_FRONT, CAM_FRONT_YUP, CAM_LEFT, CAM_LEFT_ISO, CAM_BOTTOM, CAM_REAR, CAM_RIGHT, CAM_RIGHT_ISO, CAM_CENTER} |
| enum| **[CAP_TYPE](Modules/group___enumerations.md#enum-cap-type)** { NO_END_CAP, FLAT_END_CAP, ROUND_END_CAP, EDGE_END_CAP, SHARP_END_CAP, POINT_END_CAP, ROUND_EXT_END_CAP_NONE, ROUND_EXT_END_CAP_LE, ROUND_EXT_END_CAP_TE, ROUND_EXT_END_CAP_BOTH, NUM_END_CAP_OPTIONS} |
| enum| **[CFD_CONTROL_TYPE](Modules/group___enumerations.md#enum-cfd-control-type)** { CFD_MIN_EDGE_LEN, CFD_MAX_EDGE_LEN, CFD_MAX_GAP, CFD_NUM_CIRCLE_SEGS, CFD_GROWTH_RATIO, CFD_LIMIT_GROWTH_FLAG, CFD_INTERSECT_SUBSURFACE_FLAG, CFD_HALF_MESH_FLAG, CFD_FAR_FIELD_FLAG, CFD_FAR_MAX_EDGE_LEN, CFD_FAR_MAX_GAP, CFD_FAR_NUM_CIRCLE_SEGS, CFD_FAR_SIZE_ABS_FLAG, CFD_FAR_LENGTH, CFD_FAR_WIDTH, CFD_FAR_HEIGHT, CFD_FAR_X_SCALE, CFD_FAR_Y_SCALE, CFD_FAR_Z_SCALE, CFD_FAR_LOC_MAN_FLAG, CFD_FAR_LOC_X, CFD_FAR_LOC_Y, CFD_FAR_LOC_Z, CFD_SRF_XYZ_FLAG} |
| enum| **[CFD_MESH_EXPORT_TYPE](Modules/group___enumerations.md#enum-cfd-mesh-export-type)** { CFD_STL_FILE_NAME, CFD_POLY_FILE_NAME, CFD_TRI_FILE_NAME, CFD_OBJ_FILE_NAME, CFD_DAT_FILE_NAME, CFD_KEY_FILE_NAME, CFD_GMSH_FILE_NAME, CFD_TKEY_FILE_NAME, CFD_FACET_FILE_NAME, CFD_VSPGEOM_FILE_NAME, CFD_NUM_FILE_NAMES} |
| enum| **[CFD_MESH_SOURCE_TYPE](Modules/group___enumerations.md#enum-cfd-mesh-source-type)** { POINT_SOURCE, LINE_SOURCE, BOX_SOURCE, ULINE_SOURCE, WLINE_SOURCE, NUM_SOURCE_TYPES} |
| enum| **[CFD_VIS_TYPE](Modules/group___enumerations.md#enum-cfd-vis-type)** { TAG, REASON} |
| enum| **[CF_LAM_EQN](Modules/group___enumerations.md#enum-cf-lam-eqn)** { CF_LAM_BLASIUS = 0, CF_LAM_BLASIUS_W_HEAT} |
| enum| **[CF_TURB_EQN](Modules/group___enumerations.md#enum-cf-turb-eqn)** { CF_TURB_EXPLICIT_FIT_SPALDING = 0, CF_TURB_EXPLICIT_FIT_SPALDING_CHI, CF_TURB_EXPLICIT_FIT_SCHOENHERR, DO_NOT_USE_CF_TURB_IMPLICIT_KARMAN, CF_TURB_IMPLICIT_SCHOENHERR, CF_TURB_IMPLICIT_KARMAN_SCHOENHERR, CF_TURB_POWER_LAW_BLASIUS, CF_TURB_POWER_LAW_PRANDTL_LOW_RE, CF_TURB_POWER_LAW_PRANDTL_MEDIUM_RE, CF_TURB_POWER_LAW_PRANDTL_HIGH_RE, CF_TURB_SCHLICHTING_COMPRESSIBLE, DO_NOT_USE_CF_TURB_SCHLICHTING_INCOMPRESSIBLE, DO_NOT_USE_CF_TURB_SCHLICHTING_PRANDTL, DO_NOT_USE_CF_TURB_SCHULTZ_GRUNOW_HIGH_RE, CF_TURB_SCHULTZ_GRUNOW_SCHOENHERR, DO_NOT_USE_CF_TURB_WHITE_CHRISTOPH_COMPRESSIBLE, CF_TURB_ROUGHNESS_SCHLICHTING_AVG, DO_NOT_USE_CF_TURB_ROUGHNESS_SCHLICHTING_LOCAL, DO_NOT_USE_CF_TURB_ROUGHNESS_WHITE, CF_TURB_ROUGHNESS_SCHLICHTING_AVG_FLOW_CORRECTION, CF_TURB_HEATTRANSFER_WHITE_CHRISTOPH} |
| enum| **[CHEVRON_TYPE](Modules/group___enumerations.md#enum-chevron-type)** { CHEVRON_NONE, CHEVRON_PARTIAL, CHEVRON_FULL, CHEVRON_NUM_TYPES} |
| enum| **[CHEVRON_W01_MODES](Modules/group___enumerations.md#enum-chevron-w01-modes)** { CHEVRON_W01_SE, CHEVRON_W01_CW, CHEVRON_W01_NUM_MODES} |
| enum| **[COLLISION_ERRORS](Modules/group___enumerations.md#enum-collision-errors)** { COLLISION_OK, COLLISION_INTERSECT_NO_SOLUTION, COLLISION_CLEAR_NO_SOLUTION} |
| enum| **[COMPUTATION_FILE_TYPE](Modules/group___enumerations.md#enum-computation-file-type)** { NO_FILE_TYPE = 0, COMP_GEOM_TXT_TYPE = 1, COMP_GEOM_CSV_TYPE = 1<<1, DRAG_BUILD_TSV_TYPE_DEPRECATED = 1<<2, SLICE_TXT_TYPE = 1<<3, MASS_PROP_TXT_TYPE = 1<<4, DEGEN_GEOM_CSV_TYPE = 1<<5, DEGEN_GEOM_M_TYPE = 1<<6, CFD_STL_TYPE = 1<<7, CFD_POLY_TYPE = 1<<8, CFD_TRI_TYPE = 1<<9, CFD_OBJ_TYPE = 1<<10, CFD_DAT_TYPE = 1<<11, CFD_KEY_TYPE = 1<<12, CFD_GMSH_TYPE = 1<<13, CFD_SRF_TYPE_DEPRECATED = 1<<14, CFD_TKEY_TYPE = 1<<15, PROJ_AREA_CSV_TYPE = 1<<16, WAVE_DRAG_TXT_TYPE = 1<<17, VSPAERO_PANEL_TRI_TYPE = 1<<18, DRAG_BUILD_CSV_TYPE = 1<<19, CFD_FACET_TYPE = 1<<20, CFD_CURV_TYPE_DEPRECATED = 1<<21, CFD_PLOT3D_TYPE_DEPRECATED = 1<<22, CFD_VSPGEOM_TYPE = 1<<23, VSPAERO_VSPGEOM_TYPE = 1<<24} |
| enum| **[CONFORMAL_TRIM_TYPE](Modules/group___enumerations.md#enum-conformal-trim-type)** { U_TRIM, L_TRIM, ETA_TRIM, NUM_TRIM_TYPES} |
| enum| **[DELIM_TYPE](Modules/group___enumerations.md#enum-delim-type)** { DELIM_COMMA, DELIM_USCORE, DELIM_SPACE, DELIM_NONE, DELIM_NUM_TYPES} |
| enum| **[DEPTH_TYPE](Modules/group___enumerations.md#enum-depth-type)** { DEPTH_FRONT, DEPTH_REAR, DEPTH_FREE, NUM_DEPTH_TYPE} |
| enum| **[DIMENSION_SET](Modules/group___enumerations.md#enum-dimension-set)** { SET_3D, SET_2D} |
| enum| **[DIR_INDEX](Modules/group___enumerations.md#enum-dir-index)** { X_DIR = 0, Y_DIR = 1, Z_DIR = 2, ALL_DIR = 3} |
| enum| **[DISPLAY_TYPE](Modules/group___enumerations.md#enum-display-type)** { DISPLAY_BEZIER, DISPLAY_DEGEN_SURF, DISPLAY_DEGEN_PLATE, DISPLAY_DEGEN_CAMBER} |
| enum| **[DRAW_TYPE](Modules/group___enumerations.md#enum-draw-type)** { GEOM_DRAW_WIRE, GEOM_DRAW_HIDDEN, GEOM_DRAW_SHADE, GEOM_DRAW_TEXTURE, GEOM_DRAW_NONE} |
| enum| **[ENGINE_GEOM_IO_TYPE](Modules/group___enumerations.md#enum-engine-geom-io-type)** { ENGINE_GEOM_NONE, ENGINE_GEOM_INLET, ENGINE_GEOM_INLET_OUTLET, ENGINE_GEOM_OUTLET, ENGINE_GEOM_IO_NUM_TYPES} |
| enum| **[ENGINE_GEOM_TYPE](Modules/group___enumerations.md#enum-engine-geom-type)** { ENGINE_GEOM_FLOWTHROUGH, ENGINE_GEOM_TO_LIP, ENGINE_GEOM_FLOWPATH, ENGINE_GEOM_TO_FACE, ENGINE_GEOM_NUM_TYPES} |
| enum| **[ENGINE_LOC_MODE](Modules/group___enumerations.md#enum-engine-loc-mode)** { ENGINE_LOC_INDEX, ENGINE_LOC_U} |
| enum| **[ENGINE_LOC_INDEX_TYPES](Modules/group___enumerations.md#enum-engine-loc-index-types)** { ENGINE_LOC_INLET_LIP, ENGINE_LOC_INLET_FACE, ENGINE_LOC_OUTLET_LIP, ENGINE_LOC_OUTLET_FACE, ENGINE_LOC_NUM} |
| enum| **[ENGINE_MODE_TYPE](Modules/group___enumerations.md#enum-engine-mode-type)** { ENGINE_MODE_FLOWTHROUGH, ENGINE_MODE_FLOWTHROUGH_NEG, ENGINE_MODE_FLOWTHROUGH_NEG_ONLY, ENGINE_MODE_TO_LIP, ENGINE_MODE_TO_FACE, ENGINE_MODE_TO_FACE_NEG, ENGINE_MODE_TO_FACE_NEG_ONLY, ENGINE_MODE_EXTEND, ENGINE_MODE_NUM_TYPES} |
| enum| **[ERROR_CODE](Modules/group___enumerations.md#enum-error-code)** { VSP_OK, VSP_INVALID_PTR, VSP_INVALID_TYPE, VSP_CANT_FIND_TYPE, VSP_CANT_FIND_PARM, VSP_CANT_FIND_NAME, VSP_INVALID_GEOM_ID, VSP_FILE_DOES_NOT_EXIST, VSP_FILE_WRITE_FAILURE, VSP_FILE_READ_FAILURE, VSP_WRONG_GEOM_TYPE, VSP_WRONG_XSEC_TYPE, VSP_WRONG_FILE_TYPE, VSP_INDEX_OUT_RANGE, VSP_INVALID_XSEC_ID, VSP_INVALID_ID, VSP_CANT_SET_NOT_EQ_PARM, VSP_AMBIGUOUS_SUBSURF, VSP_INVALID_VARPRESET_SETNAME, VSP_INVALID_VARPRESET_GROUPNAME, VSP_CONFORMAL_PARENT_UNSUPPORTED, VSP_UNEXPECTED_RESET_REMAP_ID, VSP_INVALID_INPUT_VAL, VSP_INVALID_CF_EQN, VSP_INVALID_DRIVERS, VSP_ADV_LINK_BUILD_FAIL, VSP_DEPRECATED, VSP_LINK_LOOP_DETECTED, VSP_LINK_OUTPUT_NOT_ASSIGNED, VSP_DUPLICATE_NAME, VSP_GUI_DEVICE_DEACTIVATED, VSP_COULD_NOT_CREATE_BACKGROUND3D, VSP_NUM_ERROR_CODE} |
| enum| **[EXCRES_TYPE](Modules/group___enumerations.md#enum-excres-type)** { EXCRESCENCE_COUNT = 0, EXCRESCENCE_CD, EXCRESCENCE_PERCENT_GEOM, EXCRESCENCE_MARGIN, EXCRESCENCE_DRAGAREA} |
| enum| **[EXPORT_TYPE](Modules/group___enumerations.md#enum-export-type)** { EXPORT_FELISA, EXPORT_XSEC, EXPORT_STL, EXPORT_AWAVE, EXPORT_NASCART, EXPORT_POVRAY, EXPORT_CART3D, EXPORT_VSPGEOM, EXPORT_VORXSEC, EXPORT_XSECGEOM, EXPORT_GMSH, EXPORT_X3D, EXPORT_STEP, EXPORT_PLOT3D, EXPORT_IGES, EXPORT_BEM, EXPORT_DXF, EXPORT_FACET, EXPORT_SVG, EXPORT_PMARC, EXPORT_OBJ, EXPORT_SELIG_AIRFOIL, EXPORT_BEZIER_AIRFOIL, EXPORT_IGES_STRUCTURE, EXPORT_STEP_STRUCTURE} |
| enum| **[FEA_BC_MODE](Modules/group___enumerations.md#enum-fea-bc-mode)** { FEA_BCM_USER, FEA_BCM_ALL, FEA_BCM_PIN, FEA_BCM_SYMM, FEA_BCM_ASYMM, FEA_NUM_BCM_MODES} |
| enum| **[FEA_BC_TYPE](Modules/group___enumerations.md#enum-fea-bc-type)** { FEA_BC_STRUCTURE, FEA_BC_PART, FEA_BC_SUBSURF, FEA_NUM_BC_TYPES} |
| enum| **[FEA_CROSS_SECT_TYPE](Modules/group___enumerations.md#enum-fea-cross-sect-type)** { FEA_XSEC_GENERAL = 0, FEA_XSEC_CIRC, FEA_XSEC_PIPE, FEA_XSEC_I, FEA_XSEC_RECT, FEA_XSEC_BOX} |
| enum| **[FEA_EXPORT_TYPE](Modules/group___enumerations.md#enum-fea-export-type)** { FEA_MASS_FILE_NAME, FEA_NASTRAN_FILE_NAME, FEA_NKEY_FILE_NAME, FEA_CALCULIX_FILE_NAME, FEA_STL_FILE_NAME, FEA_GMSH_FILE_NAME, FEA_SRF_FILE_NAME, FEA_CURV_FILE_NAME, FEA_PLOT3D_FILE_NAME, FEA_IGES_FILE_NAME, FEA_STEP_FILE_NAME, FEA_NUM_FILE_NAMES} |
| enum| **[FEA_FIX_PT_TYPE](Modules/group___enumerations.md#enum-fea-fix-pt-type)** { FEA_FIX_PT_ON_BODY, FEA_FIX_PT_GLOBAL_XYZ, FEA_FIX_PT_DELTA_XYZ, FEA_FIX_PT_DELTA_UVN, FEA_FIX_PT_GEOM_ORIGIN, FEA_FIX_PT_GEOM_CG, FEA_NUM_FIX_PT_TYPES} |
| enum| **[FEA_MATERIAL_TYPE](Modules/group___enumerations.md#enum-fea-material-type)** { FEA_ISOTROPIC, FEA_ENG_ORTHO, FEA_ENG_ORTHO_TRANS_ISO, FEA_LAMINATE, FEA_NUM_MAT_TYPES} |
| enum| **[FEA_ORIENTATION_TYPE](Modules/group___enumerations.md#enum-fea-orientation-type)** { FEA_ORIENT_GLOBAL_X, FEA_ORIENT_GLOBAL_Y, FEA_ORIENT_GLOBAL_Z, FEA_ORIENT_COMP_X, FEA_ORIENT_COMP_Y, FEA_ORIENT_COMP_Z, FEA_ORIENT_PART_U, FEA_ORIENT_PART_V, FEA_ORIENT_OML_U, FEA_ORIENT_OML_V, FEA_ORIENT_OML_R, FEA_ORIENT_OML_S, FEA_ORIENT_OML_T, FEA_NUM_ORIENT_TYPES} |
| enum| **[FEA_PART_ELEMENT_TYPE](Modules/group___enumerations.md#enum-fea-part-element-type)** { FEA_DEPRECATED = -1, FEA_SHELL = 0, FEA_BEAM, FEA_SHELL_AND_BEAM, FEA_NO_ELEMENTS, FEA_NUM_ELEMENT_TYPES} |
| enum| **[FEA_PART_TYPE](Modules/group___enumerations.md#enum-fea-part-type)** { FEA_SLICE = 0, FEA_RIB, FEA_SPAR, FEA_FIX_POINT, FEA_DOME, FEA_RIB_ARRAY, FEA_SLICE_ARRAY, FEA_SKIN, FEA_TRIM, FEA_POLY_SPAR, FEA_NUM_TYPES} |
| enum| **[FEA_RIB_NORMAL](Modules/group___enumerations.md#enum-fea-rib-normal)** { NO_NORMAL, LE_NORMAL, TE_NORMAL, SPAR_NORMAL} |
| enum| **[FEA_SHELL_TREATMENT_TYPE](Modules/group___enumerations.md#enum-fea-shell-treatment-type)** { FEA_KEEP = 0, FEA_DELETE, FEA_NUM_SHELL_TREATMENT_TYPES} |
| enum| **[FEA_SLICE_TYPE](Modules/group___enumerations.md#enum-fea-slice-type)** { XY_BODY = 0, YZ_BODY, XZ_BODY, XY_ABS, YZ_ABS, XZ_ABS, SPINE_NORMAL} |
| enum| **[FEA_POLY_SPAR_POINT](Modules/group___enumerations.md#enum-fea-poly-spar-point)** { POLY_SPAR_POINT_U01, POLY_SPAR_POINT_U0N, POLY_SPAR_POINT_ETA, NUM_POLY_SPAR_POINT_TYPES} |
| enum| **[FEA_UNIT_TYPE](Modules/group___enumerations.md#enum-fea-unit-type)** { SI_UNIT = 0, CGS_UNIT, MPA_UNIT, BFT_UNIT, BIN_UNIT} |
| enum| **[FF_B_EQN](Modules/group___enumerations.md#enum-ff-b-eqn)** { FF_B_MANUAL = 0, FF_B_SCHEMENSKY_FUSE, FF_B_SCHEMENSKY_NACELLE, FF_B_HOERNER_STREAMBODY, FF_B_TORENBEEK, FF_B_SHEVELL, FF_B_COVERT, FF_B_JENKINSON_FUSE, FF_B_JENKINSON_WING_NACELLE, FF_B_JENKINSON_AFT_FUSE_NACELLE} |
| enum| **[FF_W_EQN](Modules/group___enumerations.md#enum-ff-w-eqn)** { FF_W_MANUAL = 0, FF_W_EDET_CONV, FF_W_EDET_ADV, FF_W_HOERNER, FF_W_COVERT, FF_W_SHEVELL, FF_W_KROO, FF_W_TORENBEEK, FF_W_DATCOM, FF_W_SCHEMENSKY_6_SERIES_AF, FF_W_SCHEMENSKY_4_SERIES_AF, FF_W_JENKINSON_WING, FF_W_JENKINSON_TAIL, FF_W_SCHEMENSKY_SUPERCRITICAL_AF} |
| enum| **[FREESTREAM_PD_UNITS](Modules/group___enumerations.md#enum-freestream-pd-units)** { PD_UNITS_IMPERIAL = 0, PD_UNITS_METRIC} |
| enum| **[FILE_CHOOSER_MODE](Modules/group___enumerations.md#enum-file-chooser-mode)** { OPEN, SAVE, NUM_FILE_CHOOSER_MODES} |
| enum| **[FILE_CHOOSER_TYPE](Modules/group___enumerations.md#enum-file-chooser-type)** { FC_OPENVSP, FC_NATIVE, NUM_FILE_CHOOSER_TYPES} |
| enum| **[GDEV](Modules/group___enumerations.md#enum-gdev)** { GDEV_TAB, GDEV_SCROLL_TAB, GDEV_GROUP, GDEV_PARM_BUTTON, GDEV_INPUT, GDEV_OUTPUT, GDEV_SLIDER, GDEV_SLIDER_ADJ_RANGE, GDEV_CHECK_BUTTON, GDEV_CHECK_BUTTON_BIT, GDEV_RADIO_BUTTON, GDEV_TOGGLE_BUTTON, GDEV_TOGGLE_BUTTON_FREE, GDEV_TOGGLE_RADIO_GROUP, GDEV_TRIGGER_BUTTON, GDEV_COUNTER, GDEV_CHOICE, GDEV_ADD_CHOICE_ITEM, GDEV_SLIDER_INPUT, GDEV_SLIDER_ADJ_RANGE_INPUT, GDEV_SLIDER_ADJ_RANGE_TWO_INPUT, GDEV_FRACT_PARM_SLIDER, GDEV_STRING_INPUT, GDEV_INDEX_SELECTOR, GDEV_COLOR_PICKER, GDEV_YGAP, GDEV_DIVIDER_BOX, GDEV_BEGIN_SAME_LINE, GDEV_END_SAME_LINE, GDEV_FORCE_WIDTH, GDEV_SET_FORMAT, NUM_GDEV_TYPES, ALL_GDEV_TYPES} |
| enum| **[GEAR_CONFIGURATION_MODES](Modules/group___enumerations.md#enum-gear-configuration-modes)** { GEAR_CONFIGURATION_DOWN, GEAR_CONFIGURATION_UP, GEAR_CONFIGURATION_UP_AND_DOWN, GEAR_CONFIGURATION_INTERMEDIATE, GEAR_CONFIGURATION_ALL, NUM_GEAR_CONFIGURATION_MODES} |
| enum| **[GEAR_RETRACT_MODES](Modules/group___enumerations.md#enum-gear-retract-modes)** { GEAR_STOWED_POSITION, GEAR_MECHANISM, NUM_GEAR_RETRACT_MODES} |
| enum| **[GEAR_SUSPENSION_MODES](Modules/group___enumerations.md#enum-gear-suspension-modes)** { GEAR_SUSPENSION_NOMINAL, GEAR_SUSPENSION_COMPRESSED, GEAR_SUSPENSION_EXTENDED, NUM_GEAR_SUSPENSION_MODES} |
| enum| **[GENDER](Modules/group___enumerations.md#enum-gender)** { MALE, FEMALE} |
| enum| **[GEOMETRY_ANALYSIS_TYPE](Modules/group___enumerations.md#enum-geometry-analysis-type)** { EXTERNAL_INTERFERENCE, PACKAGING_INTERFERENCE, EXTERNAL_SELF_INTERFERENCE, PLANE_STATIC_DISTANCE_INTERFERENCE, PLANE_2PT_ANGLE_INTERFERENCE, GEAR_CG_TIPBACK_ANALYSIS, PLANE_1PT_ANGLE_INTERFERENCE, GEAR_WEIGHT_DISTRIBUTION_ANALYSIS, GEAR_TIPOVER_ANALYSIS, GEAR_TURN_ANALYSIS, VISIBLE_FROM_POINT_ANALYSIS, CCE_INTERFERENCE, LINEAR_SWEPT_VOLUME_ANALYSIS, VISIBLE_AT_SURF_ANALYSIS, NUM_INTERFERENCE_TYPES} |
| enum| **[GUI_GEOM_SCREEN](Modules/group___enumerations.md#enum-gui-geom-screen)** { POD_GEOM_SCREEN, FUSELAGE_GEOM_SCREEN, MS_WING_GEOM_SCREEN, BLANK_GEOM_SCREEN, MESH_GEOM_SCREEN, NGON_MESH_GEOM_SCREEN, STACK_GEOM_SCREEN, CUSTOM_GEOM_SCREEN, PT_CLOUD_GEOM_SCREEN, PROP_GEOM_SCREEN, HINGE_GEOM_SCREEN, MULT_GEOM_SCREEN, CONFORMAL_SCREEN, ELLIPSOID_GEOM_SCREEN, BOR_GEOM_SCREEN, WIRE_FRAME_GEOM_SCREEN, HUMAN_GEOM_SCREEN, ROUTING_GEOM_SCREEN, AUXILIARY_GEOM_SCREEN, GEAR_GEOM_SCREEN, COBRA_GEOM_SCREEN, NUM_GEOM_SCREENS, ALL_GEOM_SCREENS} |
| enum| **[GUI_VSP_SCREEN](Modules/group___enumerations.md#enum-gui-vsp-screen)** { VSP_ADV_LINK_SCREEN, VSP_ADV_LINK_VAR_RENAME_SCREEN, VSP_AERO_STRUCT_SCREEN, VSP_AIRFOIL_CURVES_EXPORT_SCREEN, VSP_AIRFOIL_POINTS_EXPORT_SCREEN, VSP_ATTRIBUTE_EXPLORER_SCREEN, VSP_BACKGROUND_SCREEN, VSP_BACKGROUND3D_SCREEN, VSP_BACKGROUND3D_PREVIEW_SCREEN, VSP_BEM_OPTIONS_SCREEN, VSP_CFD_MESH_SCREEN, VSP_CLIPPING_SCREEN, VSP_COMP_GEOM_SCREEN, VSP_COR_SCREEN, VSP_CURVE_EDIT_SCREEN, VSP_DEGEN_GEOM_SCREEN, VSP_DESIGN_VAR_SCREEN, VSP_DXF_OPTIONS_SCREEN, VSP_EXPORT_SCREEN, VSP_FEA_PART_EDIT_SCREEN, VSP_FEA_XSEC_SCREEN, VSP_FIT_MODEL_SCREEN, VSP_IGES_OPTIONS_SCREEN, VSP_IGES_STRUCTURE_OPTIONS_SCREEN, VSP_EXPORT_CUSTOM_SCRIPT, VSP_GEOMETRY_ANALYSIS_SCREEN, VSP_IMPORT_SCREEN, VSP_LIGHTING_SCREEN, VSP_MANAGE_GEOM_SCREEN, VSP_MANAGE_TEXTURE_SCREEN, VSP_MASS_PROP_SCREEN, VSP_MATERIAL_EDIT_SCREEN, VSP_MEASURE_SCREEN, VSP_MODE_EDITOR_SCREEN, VSP_NERF_MANAGE_GEOM_SCREEN, VSP_SNAP_TO_SCREEN, VSP_PARASITE_DRAG_SCREEN, VSP_PARM_DEBUG_SCREEN, VSP_PARM_LINK_SCREEN, VSP_PARM_SCREEN, VSP_PICK_SET_SCREEN, VSP_PREFERENCES_SCREEN, VSP_PROJECTION_SCREEN, VSP_PSLICE_SCREEN, VSP_RESULTS_VIEWER_SCREEN, VSP_SCREENSHOT_SCREEN, VSP_SELECT_FILE_SCREEN, VSP_SET_EDITOR_SCREEN, VSP_STEP_OPTIONS_SCREEN, VSP_STEP_STRUCTURE_OPTIONS_SCREEN, VSP_STL_OPTIONS_SCREEN, VSP_STRUCT_SCREEN, VSP_STRUCT_ASSEMBLY_SCREEN, VSP_SURFACE_INTERSECTION_SCREEN, VSP_SVG_OPTIONS_SCREEN, VSP_USER_PARM_SCREEN, VSP_VAR_PRESET_SCREEN, VSP_VEH_NOTES_SCREEN, VSP_VEH_SCREEN, VSP_VIEW_SCREEN, VSP_VSPAERO_PLOT_SCREEN, VSP_VSPAERO_SCREEN, VSP_XSEC_SCREEN, VSP_WAVEDRAG_SCREEN, VSP_MAIN_SCREEN, VSP_NUM_SCREENS, VSP_ALL_SCREENS} |
| enum| **[INIT_EDIT_XSEC_TYPE](Modules/group___enumerations.md#enum-init-edit-xsec-type)** { EDIT_XSEC_CIRCLE, EDIT_XSEC_ELLIPSE, EDIT_XSEC_RECTANGLE, NUM_INIT_EDIT_XSEC_TYPES} |
| enum| **[IMPORT_TYPE](Modules/group___enumerations.md#enum-import-type)** { IMPORT_STL, IMPORT_NASCART, IMPORT_CART3D_TRI, IMPORT_XSEC_MESH, IMPORT_PTS, IMPORT_V2, IMPORT_BEM, IMPORT_XSEC_WIRE, IMPORT_P3D_WIRE} |
| enum| **[INTERSECT_EXPORT_TYPE](Modules/group___enumerations.md#enum-intersect-export-type)** { INTERSECT_SRF_FILE_NAME, INTERSECT_CURV_FILE_NAME, INTERSECT_PLOT3D_FILE_NAME, INTERSECT_IGES_FILE_NAME, INTERSECT_STEP_FILE_NAME, INTERSECT_NUM_FILE_NAMES} |
| enum| **[LEN_UNITS](Modules/group___enumerations.md#enum-len-units)** { LEN_MM, LEN_CM, LEN_M, LEN_IN, LEN_FT, LEN_YD, LEN_UNITLESS, NUM_LEN_UNIT} |
| enum| **[MASS_UNIT](Modules/group___enumerations.md#enum-mass-unit)** { MASS_UNIT_G = 0, MASS_UNIT_KG, MASS_UNIT_TONNE, MASS_UNIT_LBM, MASS_UNIT_SLUG, MASS_LBFSEC2IN, NUM_MASS_UNIT} |
| enum| **[MESH_REASON](Modules/group___enumerations.md#enum-mesh-reason)** { NO_REASON, MAX_LEN_CONSTRAINT, CURV_GAP, CURV_NCIRCSEG, SOURCES, MIN_LEN_CONSTRAINT, MIN_LEN_CONSTRAINT_CURV_GAP, MIN_LEN_CONSTRAINT_CURV_NCIRCSEG, MIN_LEN_CONSTRAINT_SOURCES, GROW_LIMIT_MAX_LEN_CONSTRAINT, GROW_LIMIT_CURV_GAP, GROW_LIMIT_CURV_NCIRCSEG, GROW_LIMIT_SOURCES, GROW_LIMIT_MIN_LEN_CONSTRAINT, GROW_LIMIT_MIN_LEN_CONSTRAINT_CURV_GAP, GROW_LIMIT_MIN_LEN_CONSTRAINT_CURV_NCIRCSEG, GROW_LIMIT_MIN_LEN_CONSTRAINT_SOURCES, NUM_MESH_REASON, MIN_LEN_INCREMENT = MIN_LEN_CONSTRAINT - MAX_LEN_CONSTRAINT, GROW_LIMIT_INCREMENT = GROW_LIMIT_CURV_GAP - CURV_GAP, MIN_GROW_LIMIT = GROW_LIMIT_CURV_GAP} |
| enum| **[MESH_TYPE](Modules/group___enumerations.md#enum-mesh-type)** { TRI_MESH_TYPE, QUAD_MESH_TYPE, NGON_MESH_TYPE, NUM_MESH_TYPE} |
| enum| **[MOTION_EXTENT_TYPE](Modules/group___enumerations.md#enum-motion-extent-type)** { EXTENT_FORWARD_INF, EXTENT_REVERSE_INF, EXTENT_FORWARD_FINITE, EXTENT_REVERSE_FINITE, EXTENT_SLIDER_FULL, EXTENT_SLIDER_BEFORE, EXTENT_SLIDER_AFTER, MOTION_NUM_EXTENT_TYPES} |
| enum| **[OBJ_ID_LENGTH](Modules/group___enumerations.md#enum-obj-id-length)** { ID_LENGTH_PRESET_GROUP = 5, ID_LENGTH_PRESET_SETTING = 6, ID_LENGTH_ATTR = 8, ID_LENGTH_ATTRCOLL = 9, ID_LENGTH_PARMCONTAINER = 10, ID_LENGTH_PARM = 11} |
| enum| **[PARM_TYPE](Modules/group___enumerations.md#enum-parm-type)** { PARM_DOUBLE_TYPE, PARM_INT_TYPE, PARM_BOOL_TYPE, PARM_FRACTION_TYPE, PARM_LIMITED_INT_TYPE, PARM_NOTEQ_TYPE, PARM_POWER_INT_TYPE} |
| enum| **[PATCH_TYPE](Modules/group___enumerations.md#enum-patch-type)** { PATCH_NONE, PATCH_POINT, PATCH_LINE, PATCH_COPY, PATCH_HALFWAY, PATCH_NUM_TYPES} |
| enum| **[PCURV_TYPE](Modules/group___enumerations.md#enum-pcurv-type)** { LINEAR, PCHIP, CEDIT, APPROX_CEDIT, NUM_PCURV_TYPE} |
| enum| **[PRES_UNITS](Modules/group___enumerations.md#enum-pres-units)** { PRES_UNIT_PSF = 0, PRES_UNIT_PSI, PRES_UNIT_BA, PRES_UNIT_PA, PRES_UNIT_KPA, PRES_UNIT_MPA, PRES_UNIT_INCHHG, PRES_UNIT_MMHG, PRES_UNIT_MMH20, PRES_UNIT_MB, PRES_UNIT_ATM, NUM_PRES_UNIT} |
| enum| **[PROJ_BNDY_TYPE](Modules/group___enumerations.md#enum-proj-bndy-type)** { NO_BOUNDARY, SET_BOUNDARY, GEOM_BOUNDARY, NUM_PROJ_BNDY_OPTIONS} |
| enum| **[PROJ_DIR_TYPE](Modules/group___enumerations.md#enum-proj-dir-type)** { X_PROJ, Y_PROJ, Z_PROJ, GEOM_PROJ, VEC_PROJ, NUM_PROJ_DIR_OPTIONS} |
| enum| **[PROJ_TGT_TYPE](Modules/group___enumerations.md#enum-proj-tgt-type)** { SET_TARGET, GEOM_TARGET, MODE_TARGET, Z_TARGET, XYZ_TARGET, NUM_PROJ_TGT_OPTIONS} |
| enum| **[PROP_AZIMUTH_MODE](Modules/group___enumerations.md#enum-prop-azimuth-mode)** { PROP_AZI_UNIFORM, PROP_AZI_FREE, PROP_AZI_BALANCED, NUM_PROP_AZI} |
| enum| **[PROP_DRIVERS](Modules/group___enumerations.md#enum-prop-drivers)** { RPM_PROP_DRIVER, CT_PROP_DRIVER, CP_PROP_DRIVER, T_PROP_DRIVER, ETA_PROP_DRIVER, J_PROP_DRIVER, P_PROP_DRIVER, CQ_PROP_DRIVER, Q_PROP_DRIVER, NUM_PROP_DRIVER} |
| enum| **[PROP_MODE](Modules/group___enumerations.md#enum-prop-mode)** { PROP_BLADES, PROP_BOTH, PROP_DISK} |
| enum| **[PROP_PCURVE](Modules/group___enumerations.md#enum-prop-pcurve)** { PROP_CHORD, PROP_TWIST, PROP_RAKE, PROP_SKEW, PROP_SWEEP, PROP_THICK, PROP_CLI, PROP_AXIAL, PROP_TANGENTIAL, NUM_PROP_PCURVE} |
| enum| **[REORDER_TYPE](Modules/group___enumerations.md#enum-reorder-type)** { REORDER_MOVE_UP, REORDER_MOVE_DOWN, REORDER_MOVE_TOP, REORDER_MOVE_BOTTOM, NUM_REORDER_TYPES} |
| enum| **[REF_WING_TYPE](Modules/group___enumerations.md#enum-ref-wing-type)** { MANUAL_REF = 0, COMPONENT_REF, NUM_REF_TYPES} |
| enum| **[RES_DATA_TYPE](Modules/group___enumerations.md#enum-res-data-type)** { INVALID_TYPE = -1, BOOL_DATA = 0, INT_DATA = 1, DOUBLE_DATA = 2, STRING_DATA = 3, VEC3D_DATA = 4, INT_MATRIX_DATA = 5, DOUBLE_MATRIX_DATA = 6, ATTR_COLLECTION_DATA = 8, PARM_REFERENCE_DATA = 9} |
| enum| **[RES_GEOM_TYPE](Modules/group___enumerations.md#enum-res-geom-type)** { MESH_INDEXED_TRI, MESH_SLICE_TRI, GEOM_XSECS, MESH_INDEX_AND_SLICE_TRI} |
| enum| **[RHO_UNITS](Modules/group___enumerations.md#enum-rho-units)** { RHO_UNIT_SLUG_FT3 = 0, RHO_UNIT_G_CM3, RHO_UNIT_KG_M3, RHO_UNIT_TONNE_MM3, RHO_UNIT_LBM_FT3, RHO_UNIT_LBFSEC2_IN4, RHO_UNIT_LBM_IN3, NUM_RHO_UNIT} |
| enum| **[ROUTE_PT_TYPE](Modules/group___enumerations.md#enum-route-pt-type)** { ROUTE_PT_COMP, ROUTE_PT_UV, ROUTE_PT_RST, ROUTE_PT_LMN, ROUTE_PT_EtaMN, ROUTE_PT_NUM_TYPES} |
| enum| **[ROUTE_PT_DELTA_TYPE](Modules/group___enumerations.md#enum-route-pt-delta-type)** { ROUTE_PT_DELTA_XYZ, ROUTE_PT_DELTA_COMP, ROUTE_PT_DELTA_UVN, ROUTE_PT_DELTA_NUM_TYPES} |
| enum| **[SCALE_TYPE](Modules/group___enumerations.md#enum-scale-type)** { SCALE_WIDTH, SCALE_HEIGHT, SCALE_WIDTH_HEIGHT, SCALE_RESOLUTION, NUM_SCALE_TYPES} |
| enum| **[SET_TYPE](Modules/group___enumerations.md#enum-set-type)** { SET_NONE = -1, SET_ALL = 0, SET_SHOWN = 1, SET_NOT_SHOWN = 2, SET_FIRST_USER = 3, MIN_NUM_USER = 20, MAX_NUM_SETS = 1000} |
| enum| **[STEP_REPRESENTATION](Modules/group___enumerations.md#enum-step-representation)** { STEP_SHELL, STEP_BREP} |
| enum| **[SUBSURF_INCLUDE](Modules/group___enumerations.md#enum-subsurf-include)** { SS_INC_TREAT_AS_PARENT, SS_INC_SEPARATE_TREATMENT, SS_INC_ZERO_DRAG} |
| enum| **[SUBSURF_INOUT](Modules/group___enumerations.md#enum-subsurf-inout)** { INSIDE, OUTSIDE, NONE} |
| enum| **[SUBSURF_LINE_TYPE](Modules/group___enumerations.md#enum-subsurf-line-type)** { CONST_U, CONST_W} |
| enum| **[SUBSURF_TYPE](Modules/group___enumerations.md#enum-subsurf-type)** { SS_LINE, SS_RECTANGLE, SS_ELLIPSE, SS_CONTROL, SS_LINE_ARRAY, SS_FINITE_LINE, SS_XSEC_CURVE, SS_INTERSECT, SS_NUM_TYPES} |
| enum| **[SYM_FLAG](Modules/group___enumerations.md#enum-sym-flag)** { SYM_XY = ( 1 << 0 ), SYM_XZ = ( 1 << 1 ), SYM_YZ = ( 1 << 2 ), SYM_ROT_X = ( 1 << 3 ), SYM_ROT_Y = ( 1 << 4 ), SYM_ROT_Z = ( 1 << 5 ), SYM_PLANAR_TYPES = 3, SYM_NUM_TYPES = 6} |
| enum| **[SYM_XSEC_TYP](Modules/group___enumerations.md#enum-sym-xsec-typ)** { SYM_NONE, SYM_RL, SYM_TB, SYM_ALL} |
| enum| **[TEMP_UNITS](Modules/group___enumerations.md#enum-temp-units)** { TEMP_UNIT_K = 0, TEMP_UNIT_C, TEMP_UNIT_F, TEMP_UNIT_R, NUM_TEMP_UNIT} |
| enum| **[TIRE_CLEARANCE_MODES](Modules/group___enumerations.md#enum-tire-clearance-modes)** { TIRE_NOMINAL_CLEARANCE, TIRE_GROWTH_CLEARANCE, TIRE_CLEARANCE, NUM_TIRE_CLEARANCE_MODES} |
| enum| **[TIRE_CONTACT_MODES](Modules/group___enumerations.md#enum-tire-contact-modes)** { TIRE_STATIC_LODED_CONTACT, TIRE_NOMINAL_CONTACT, TIRE_GROWTH_CONTACT, TIRE_FLAT_CONTACT, NUM_TIRE_CONTACT_MODES} |
| enum| **[TIRE_DIM_MODES](Modules/group___enumerations.md#enum-tire-dim-modes)** { TIRE_DIM_IN, TIRE_DIM_MODEL, TIRE_DIM_FRAC, NUM_TIRE_DIM_MODES} |
| enum| **[TIRE_MODES](Modules/group___enumerations.md#enum-tire-modes)** { TIRE_TRA, TIRE_FAIR_FLANGE, TIRE_FAIR_WHEEL, TIRE_BALLOON, TIRE_BALLOON_WHEEL, TIRE_BALLOON_FAIR_WHEEL, NUM_TIRE_MODES} |
| enum| **[VEL_UNITS](Modules/group___enumerations.md#enum-vel-units)** { V_UNIT_FT_S = 0, V_UNIT_M_S, V_UNIT_MPH, V_UNIT_KM_HR, V_UNIT_KEAS, V_UNIT_KTAS, V_UNIT_MACH} |
| enum| **[VIEW_NUM](Modules/group___enumerations.md#enum-view-num)** { VIEW_1, VIEW_2HOR, VIEW_2VER, VIEW_4} |
| enum| **[VIEW_ROT](Modules/group___enumerations.md#enum-view-rot)** { ROT_0, ROT_90, ROT_180, ROT_270} |
| enum| **[VIEW_TYPE](Modules/group___enumerations.md#enum-view-type)** { VIEW_LEFT, VIEW_RIGHT, VIEW_TOP, VIEW_BOTTOM, VIEW_FRONT, VIEW_REAR, VIEW_NONE, VIEW_NUM_TYPES} |
| enum| **[VSPAERO_NOISE_TYPE](Modules/group___enumerations.md#enum-vspaero-noise-type)** { NOISE_FLYBY, NOISE_FOOTPRINT, NOISE_STEADY} |
| enum| **[VSPAERO_NOISE_UNIT](Modules/group___enumerations.md#enum-vspaero-noise-unit)** { NOISE_SI, NOISE_ENGLISH} |
| enum| **[VSPAERO_PROP_MODE](Modules/group___enumerations.md#enum-vspaero-prop-mode)** { VSPAERO_PROP_STATIC, VSPAERO_PROP_UNSTEADY, VSPAERO_PROP_PSEUDO_STEADY, VSPAERO_PROP_NUM_MODES} |
| enum| **[VSPAERO_STABILITY_TYPE](Modules/group___enumerations.md#enum-vspaero-stability-type)** { STABILITY_OFF, STABILITY_DEFAULT, STABILITY_P_ANALYSIS, STABILITY_Q_ANALYSIS, STABILITY_R_ANALYSIS, STABILITY_PITCH, STABILITY_ADJOINT, STABILITY_NUM_TYPES} |
| enum| **[VSPAERO_STALL_TYPE](Modules/group___enumerations.md#enum-vspaero-stall-type)** { STALL_OFF, STALL_ON} |
| enum| **[VSP_SURF_CFD_TYPE](Modules/group___enumerations.md#enum-vsp-surf-cfd-type)** { CFD_NORMAL, CFD_NEGATIVE, CFD_TRANSPARENT, CFD_STRUCTURE, CFD_STIFFENER, CFD_MEASURE_DUCT, CFD_NUM_TYPES} |
| enum| **[VSP_SURF_TYPE](Modules/group___enumerations.md#enum-vsp-surf-type)** { NORMAL_SURF, WING_SURF, DISK_SURF, NUM_SURF_TYPES} |
| enum| **[W_HINT](Modules/group___enumerations.md#enum-w-hint)** { W_RIGHT_0, W_BOTTOM, W_LEFT, W_TOP, W_RIGHT_1, W_FREE} |
| enum| **[WING_BLEND](Modules/group___enumerations.md#enum-wing-blend)** { BLEND_FREE, BLEND_ANGLES, BLEND_MATCH_IN_LE_TRAP, BLEND_MATCH_IN_TE_TRAP, BLEND_MATCH_OUT_LE_TRAP, BLEND_MATCH_OUT_TE_TRAP, BLEND_MATCH_IN_ANGLES, BLEND_MATCH_LE_ANGLES, BLEND_NUM_TYPES} |
| enum| **[WING_DRIVERS](Modules/group___enumerations.md#enum-wing-drivers)** { AR_WSECT_DRIVER, SPAN_WSECT_DRIVER, AREA_WSECT_DRIVER, TAPER_WSECT_DRIVER, AVEC_WSECT_DRIVER, ROOTC_WSECT_DRIVER, TIPC_WSECT_DRIVER, SECSWEEP_WSECT_DRIVER, NUM_WSECT_DRIVER, SWEEP_WSECT_DRIVER = SECSWEEP_WSECT_DRIVER + 1, SWEEPLOC_WSECT_DRIVER = SECSWEEP_WSECT_DRIVER + 2, SECSWEEPLOC_WSECT_DRIVER = SECSWEEP_WSECT_DRIVER + 3} |
| enum| **[XDDM_QUANTITY_TYPE](Modules/group___enumerations.md#enum-xddm-quantity-type)** { XDDM_VAR, XDDM_CONST} |
| enum| **[XSEC_CLOSE_TYPE](Modules/group___enumerations.md#enum-xsec-close-type)** { CLOSE_NONE, CLOSE_SKEWLOW, CLOSE_SKEWUP, CLOSE_SKEWBOTH, CLOSE_EXTRAP, CLOSE_NUM_TYPES} |
| enum| **[XSEC_CRV_TYPE](Modules/group___enumerations.md#enum-xsec-crv-type)** { XS_UNDEFINED = -1, XS_POINT, XS_CIRCLE, XS_ELLIPSE, XS_SUPER_ELLIPSE, XS_ROUNDED_RECTANGLE, XS_GENERAL_FUSE, XS_FILE_FUSE, XS_FOUR_SERIES, XS_SIX_SERIES, XS_BICONVEX, XS_WEDGE, XS_EDIT_CURVE, XS_FILE_AIRFOIL, XS_CST_AIRFOIL, XS_VKT_AIRFOIL, XS_FOUR_DIGIT_MOD, XS_FIVE_DIGIT, XS_FIVE_DIGIT_MOD, XS_ONE_SIX_SERIES, XS_AC25_773, XS_NUM_TYPES} |
| enum| **[XSEC_DRIVERS](Modules/group___enumerations.md#enum-xsec-drivers)** { WIDTH_XSEC_DRIVER, AREA_XSEC_DRIVER, HEIGHT_XSEC_DRIVER, HWRATIO_XSEC_DRIVER, NUM_XSEC_DRIVER, CIRCLE_NUM_XSEC_DRIVER = 2} |
| enum| **[XSEC_FLAP_TYPE](Modules/group___enumerations.md#enum-xsec-flap-type)** { FLAP_NONE, FLAP_PLAIN, FLAP_NUM_TYPES} |
| enum| **[XSEC_SIDES_TYPE](Modules/group___enumerations.md#enum-xsec-sides-type)** { XSEC_BOTH_SIDES, XSEC_LEFT_SIDE, XSEC_RIGHT_SIDE} |
| enum| **[XSEC_TRIM_TYPE](Modules/group___enumerations.md#enum-xsec-trim-type)** { TRIM_NONE, TRIM_X, TRIM_THICK, TRIM_NUM_TYPES} |
| enum| **[XSEC_TYPE](Modules/group___enumerations.md#enum-xsec-type)** { XSEC_FUSE, XSEC_STACK, XSEC_WING, XSEC_CUSTOM, XSEC_PROP, XSEC_NUM_TYPES} |
| enum| **[XSEC_WIDTH_SHIFT](Modules/group___enumerations.md#enum-xsec-width-shift)** { XS_SHIFT_LE = 0, XS_SHIFT_MID = 1, XS_SHIFT_TE = 2} |

## Types Documentation

### enum ABS_REL_FLAG

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ABS | |  Absolute position  |
| REL | |  Relative position  |




Enum that indicates if positions are relative or absolute. 


### enum AIRFOIL_EXPORT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SELIG_AF_EXPORT | |  Selig airfoil file format  |
| BEZIER_AF_EXPORT | |  Bezier airfoil file format  |




Enum used to identify the format of exported airfoil files. 


### enum ALIGN_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ALIGN_LEFT | |  Align to left  |
| ALIGN_CENTER | |  Align to center  |
| ALIGN_RIGHT | |  Align to right  |
| ALIGN_PIXEL | |  Align to specified pixel  |
| ALIGN_TOP | |  Align to top  |
| ALIGN_MIDDLE | |  Align to middle  |
| ALIGN_BOTTOM | |  Align to bottom  |
| NUM_ALIGN_TYPE | |  Number of alignment types  |




Enum for specifying alignment. 


### enum ANG_UNITS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ANG_RAD | |  Radians  |
| ANG_DEG | |  Degrees  |




Enum for specifying angular units. 


### enum ANGLE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ANG_0 | |  Zero deg  |
| ANG_90 | |  90 deg  |
| ANG_180 | |  180 deg  |
| ANG_270 | |  270 deg  |
| NUM_ANG | |  Number of angle choices  |




Enum for specifying image rotation angles (CW). 


### enum ATMOS_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ATMOS_TYPE_US_STANDARD_1976 | 0|  US Standard Atmosphere 1976 (default)  |
| ATMOS_TYPE_HERRINGTON_1966 | |  USAF 1966  |
| ATMOS_TYPE_MANUAL_P_R | |  Manual: pressure and density control  |
| ATMOS_TYPE_MANUAL_P_T | |  Manual: pressure and temperature control  |
| ATMOS_TYPE_MANUAL_R_T | |  Manual: density and temperature control  |
| ATMOS_TYPE_MANUAL_RE_L | |  Manual: Reynolds number and length control  |




Enum that identifies the atmospheric model used in the Parasite Drag tool. 


### enum ATTACH_TRANS_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ATTACH_TRANS_NONE | 0|  No parent attachment for translations  |
| ATTACH_TRANS_COMP | |  Translation relative to parent body axes  |
| ATTACH_TRANS_UV | |  Translation relative to parent surface coordinate frame  |
| ATTACH_TRANS_RST | |  Translation relative to parent per-section volume coordinate frame  |
| ATTACH_TRANS_LMN | |  Translation relative to parent uniform volume coordinate frame  |
| ATTACH_TRANS_EtaMN | |  Translation relative to wing parent uniform eta volume coordinate frame  |
| ATTACH_TRANS_NUM_TYPES | |  Number of translation attachment types  |




Enum that identifies the parent to child relative translation coordinate system. 


### enum ATTACH_ROT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ATTACH_ROT_NONE | 0|  No parent attachment for rotations  |
| ATTACH_ROT_COMP | |  Rotation relative to parent body axes  |
| ATTACH_ROT_UV | |  Rotation relative to parent surface coordinate frame  |
| ATTACH_ROT_RST | |  Rotation relative to parent per-section volume coordinate frame  |
| ATTACH_ROT_LMN | |  Rotation relative to parent uniform volume coordinate frame  |
| ATTACH_ROT_EtaMN | |  Rotation relative to wing parent eta volume coordinate frame  |
| ATTACH_ROT_NUM_TYPES | |  Number of rotation attachment types  |




Enum that determines parent to child relative rotation axes. 


### enum ATTRIBUTABLE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ATTROBJ_PARM | 0|  Parm  |
| ATTROBJ_GEOM | |  Geom  |
| ATTROBJ_VEH | |  Vehicle  |
| ATTROBJ_SUBSURF | |  SubSurf  |
| ATTROBJ_MEASURE | |  Measure  |
| ATTROBJ_LINK | |  Link  |
| ATTROBJ_ADVLINK | |  Adv Link  |
| ATTROBJ_ATTR | |  Attribute  |
| ATTROBJ_COLLECTION | |  Attribute Collection  |
| ATTROBJ_XSEC | |  Cross Section  |
| ATTROBJ_SEC | |  Wing Section  |
| ATTROBJ_MODE | |  Mode  |
| ATTROBJ_SET | |  Geom Set  |
| ATTROBJ_VARGROUP | |  Var Preset Group  |
| ATTROBJ_VARSETTING | |  Var Preset Setting  |
| ATTROBJ_FREE | |  Unattached attribute  |




Enum that entity type. 


### enum ATTRIBUTE_EVENT_GROUP

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ATTR_GROUP_NONE | -1|  No event (user attributes)  |
| ATTR_GROUP_WATERMARK | |  Watermark group  |
| NUM_ATTR_EVENT_GROUPS | |  Number attribute event groups  |




Enum for attribute event group. 


### enum AUX_GEOM_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| AUX_GEOM_ROTOR_TIP_PATH | |  Rotor tip path  |
| AUX_GEOM_ROTOR_BURST | |  Rotor burst zone  |
| AUX_GEOM_THREE_PT_GROUND | |  Three contact point ground plane  |
| AUX_GEOM_TWO_PT_GROUND | |  Two contact point ground plane  |
| AUX_GEOM_ONE_PT_GROUND | |  One contact point ground plane  |
| AUX_GEOM_THREE_PT_CCE | |  Three contact point composite clearance envelope  |
| AUX_GEOM_SUPER_CONE | |  Super cone (XSecCurve based profile)  |
| AUX_GEOM_SINGLE_GEAR | |  Single (potentially) off nominal gear  |
| NUM_AUX_GEOM_MODES | |  Number of auxiliary geom modes.  |




Enum for auxiliary geom modes. 


### enum BOGIE_SPACING_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| BOGIE_CENTER_DIST | |  Distance between centers  |
| BOGIE_CENTER_DIST_FRAC | |  Fractional distance between centers  |
| BOGIE_GAP | |  Gap  |
| BOGIE_GAP_FRAC | |  Fractional gap  |
| NUM_BOGIE_SPACING_TYPE | |  Number of bogie spacing control modes  |




Enum for bogie spacing control. 


### enum BOR_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| BOR_FLOWTHROUGH | |  Flowthrough mode (default)  |
| BOR_UPPER | |  Upper surface mode  |
| BOR_LOWER | |  Lower surface mode  |
| BOR_NUM_MODES | |  Number of Body of Revolution modes  |




Enum for Body of Revolution mode control. 


### enum CAMBER_INPUT_FLAG

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| MAX_CAMB | |  Input maximum camber, calculate ideal lift coefficient  |
| DESIGN_CL | |  Input ideal lift coefficient, calculate maximum camber  |




Enum used to select between maximum camber or ideal lift coefficient inputs. 


### enum CAMERA_VIEW

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CAM_TOP | |  Camera top view  |
| CAM_FRONT | |  Camera front view  |
| CAM_FRONT_YUP | |  Camera front Y-up view  |
| CAM_LEFT | |  Camera left view  |
| CAM_LEFT_ISO | |  Camera left isometric view  |
| CAM_BOTTOM | |  Camera bottom view  |
| CAM_REAR | |  Camera rear view  |
| CAM_RIGHT | |  Camera right view  |
| CAM_RIGHT_ISO | |  Camera right isometric view  |
| CAM_CENTER | |  Camera center view  |




Enum used to set camera view. 


### enum CAP_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NO_END_CAP | |  No end cap  |
| FLAT_END_CAP | |  Flat end cap  |
| ROUND_END_CAP | |  Round end cap  |
| EDGE_END_CAP | |  Edge end cap  |
| SHARP_END_CAP | |  Sharp end cap  |
| POINT_END_CAP | |  Point end cap  |
| ROUND_EXT_END_CAP_NONE | |  Extended round end cap, but not extended  |
| ROUND_EXT_END_CAP_LE | |  Extended round end cap, extend LE  |
| ROUND_EXT_END_CAP_TE | |  Extended round end cap, extend TE  |
| ROUND_EXT_END_CAP_BOTH | |  Extended round end cap, extend both  |
| NUM_END_CAP_OPTIONS | |  Number of end cap options  |




Enum that identifies the end cap types for a geometry (i.e. wing root and tip). 


### enum CFD_CONTROL_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CFD_MIN_EDGE_LEN | |  Minimum mesh edge length  |
| CFD_MAX_EDGE_LEN | |  Maximum mesh edge length  |
| CFD_MAX_GAP | |  Maximum mesh edge gap  |
| CFD_NUM_CIRCLE_SEGS | |  Number of edge segments to resolve circle  |
| CFD_GROWTH_RATIO | |  Maximum allowed edge growth ratio  |
| CFD_LIMIT_GROWTH_FLAG | |  Rigorous 3D growth limiting flag  |
| CFD_INTERSECT_SUBSURFACE_FLAG | |  Flag to intersect sub-surfaces  |
| CFD_HALF_MESH_FLAG | |  Flag to generate a half mesh  |
| CFD_FAR_FIELD_FLAG | |  Flag to generate a far field mesh  |
| CFD_FAR_MAX_EDGE_LEN | |  Maximum far field mesh edge length  |
| CFD_FAR_MAX_GAP | |  Maximum far field mesh edge gap  |
| CFD_FAR_NUM_CIRCLE_SEGS | |  Number of far field edge segments to resolve circle  |
| CFD_FAR_SIZE_ABS_FLAG | |  Relative or absolute size flag  |
| CFD_FAR_LENGTH | |  Far field length  |
| CFD_FAR_WIDTH | |  Far field width  |
| CFD_FAR_HEIGHT | |  Far field height  |
| CFD_FAR_X_SCALE | |  Far field X scale  |
| CFD_FAR_Y_SCALE | |  Far field Y scale  |
| CFD_FAR_Z_SCALE | |  Far field Z scale  |
| CFD_FAR_LOC_MAN_FLAG | |  Far field location flag: centered or manual  |
| CFD_FAR_LOC_X | |  Far field X location  |
| CFD_FAR_LOC_Y | |  Far field Y location  |
| CFD_FAR_LOC_Z | |  Far field Z location  |
| CFD_SRF_XYZ_FLAG | |  Flag to include X,Y,Z intersection curves in export files  |




Enum used to identify each CFD mesh control option (also applicable to FEA Mesh). \sa [SetCFDMeshVal()](Modules/group___c_f_d_mesh.md#function-setcfdmeshval), SetFEAMeshVal() 


### enum CFD_MESH_EXPORT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CFD_STL_FILE_NAME | |  STL export type  |
| CFD_POLY_FILE_NAME | |  POLY export type  |
| CFD_TRI_FILE_NAME | |  TRI export type  |
| CFD_OBJ_FILE_NAME | |  OBJ export type  |
| CFD_DAT_FILE_NAME | |  DAT export type  |
| CFD_KEY_FILE_NAME | |  KEY export type  |
| CFD_GMSH_FILE_NAME | |  GMSH export type  |
| CFD_TKEY_FILE_NAME | |  TKEY export type  |
| CFD_FACET_FILE_NAME | |  FACET export type  |
| CFD_VSPGEOM_FILE_NAME | |  VSPGEOM export type  |
| CFD_NUM_FILE_NAMES | |  Number of CFD Mesh export file types  |




Enum used to describe various CFD Mesh export file options. \sa [SetComputationFileName()](Modules/group___c_f_d_mesh.md#function-setcomputationfilename), [ComputeCFDMesh()](Modules/group___c_f_d_mesh.md#function-computecfdmesh)


### enum CFD_MESH_SOURCE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| POINT_SOURCE | |  Point source  |
| LINE_SOURCE | |  Line source  |
| BOX_SOURCE | |  Box source  |
| ULINE_SOURCE | |  Constant U Line source  |
| WLINE_SOURCE | |  Constant W Line source  |
| NUM_SOURCE_TYPES | |  Number of CFD Mesh source types  |




Enum that indicates the CFD Mesh source type. \sa [AddCFDSource()](Modules/group___c_f_d_mesh.md#function-addcfdsource)


### enum CFD_VIS_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TAG | |  Color mesh by tag value (component, subsurface, part, etc)  |
| REASON | |  Color mesh by local edge length reason  |




Enum that identifies how CFD and FEA meshes are colored. 


### enum CF_LAM_EQN

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CF_LAM_BLASIUS | 0|  Blasius laminar Cf equation  |
| CF_LAM_BLASIUS_W_HEAT | |  Blasius laminar Cf equation with heat (NOT IMPLEMENTED)  |




Enum that identifies the Parasite Drag Tool laminar friction coefficient equation choice. 


### enum CF_TURB_EQN

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CF_TURB_EXPLICIT_FIT_SPALDING | 0|  Explicit Fit of Spalding turbulent Cf equation  |
| CF_TURB_EXPLICIT_FIT_SPALDING_CHI | |  Explicit Fit of Spalding and Chi turbulent Cf equation  |
| CF_TURB_EXPLICIT_FIT_SCHOENHERR | |  Explicit Fit of Schoenherr turbulent Cf equation  |
| DO_NOT_USE_CF_TURB_IMPLICIT_KARMAN | |  Implicit Karman turbulent Cf equation (DO NOT USE)  |
| CF_TURB_IMPLICIT_SCHOENHERR | |  Implicit Schoenherr turbulent Cf equation  |
| CF_TURB_IMPLICIT_KARMAN_SCHOENHERR | |  Implicit Karman-Schoenherr turbulent Cf equation  |
| CF_TURB_POWER_LAW_BLASIUS | |  Power Law Blasius turbulent Cf equation  |
| CF_TURB_POWER_LAW_PRANDTL_LOW_RE | |  Power Law Prandtl Low Re turbulent Cf equation  |
| CF_TURB_POWER_LAW_PRANDTL_MEDIUM_RE | |  Power Law Prandtl Medium Re turbulent Cf equation  |
| CF_TURB_POWER_LAW_PRANDTL_HIGH_RE | |  Power Law Prandtl High Re turbulent Cf equation  |
| CF_TURB_SCHLICHTING_COMPRESSIBLE | |  Schlichting Compressible turbulent Cf equation  |
| DO_NOT_USE_CF_TURB_SCHLICHTING_INCOMPRESSIBLE | |  Schlichting Incompressible turbulent Cf equation (DO NOT USE)  |
| DO_NOT_USE_CF_TURB_SCHLICHTING_PRANDTL | |  Schlichting-Prandtl turbulent Cf equation (DO NOT USE)  |
| DO_NOT_USE_CF_TURB_SCHULTZ_GRUNOW_HIGH_RE | |  Schultz-Grunow High Re turbulent Cf equation (DO NOT USE)  |
| CF_TURB_SCHULTZ_GRUNOW_SCHOENHERR | |  Schultz-Grunow Estimate of Schoenherr turbulent Cf equation.  |
| DO_NOT_USE_CF_TURB_WHITE_CHRISTOPH_COMPRESSIBLE | |  White-Christoph Compressible turbulent Cf equation (DO NOT USE)  |
| CF_TURB_ROUGHNESS_SCHLICHTING_AVG | |  Roughness Schlichting Avg turbulent Cf equation.  |
| DO_NOT_USE_CF_TURB_ROUGHNESS_SCHLICHTING_LOCAL | |  Roughness Schlichting Local turbulent Cf equation (DO NOT USE)  |
| DO_NOT_USE_CF_TURB_ROUGHNESS_WHITE | |  Roughness White turbulent Cf equation (DO NOT USE)  |
| CF_TURB_ROUGHNESS_SCHLICHTING_AVG_FLOW_CORRECTION | |  Roughness Schlichting Avg Compressible turbulent Cf equation.  |
| CF_TURB_HEATTRANSFER_WHITE_CHRISTOPH | |  Heat Transfer White-Christoph turbulent Cf equation.  |




Enum that identifies the Parasite Drag Tool turbulent friction coefficient equation choice. 


### enum CHEVRON_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CHEVRON_NONE | |  No chevron.  |
| CHEVRON_PARTIAL | |  One or more chevrons of limited extent.  |
| CHEVRON_FULL | |  Full period of chevrons.  |
| CHEVRON_NUM_TYPES | |  Number of chevron types.  |




Enum for Chevron curve modification types. 


### enum CHEVRON_W01_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CHEVRON_W01_SE | |  Start and End  |
| CHEVRON_W01_CW | |  Center and Width  |
| CHEVRON_W01_NUM_MODES | |  Number of chevron W parameter mode types.  |




Enum for Chevron W parameter modes. 


### enum COLLISION_ERRORS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| COLLISION_OK | |  No Error.  |
| COLLISION_INTERSECT_NO_SOLUTION | |  Touching, no solution  |
| COLLISION_CLEAR_NO_SOLUTION | |  Not touching, no solution  |




Enum for Snap To collision error types. 


### enum COMPUTATION_FILE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NO_FILE_TYPE | 0|  No export file type  |
| COMP_GEOM_TXT_TYPE | 1|   |
| COMP_GEOM_CSV_TYPE | 1<<1|   |
| DRAG_BUILD_TSV_TYPE_DEPRECATED | 1<<2|   |
| SLICE_TXT_TYPE | 1<<3|   |
| MASS_PROP_TXT_TYPE | 1<<4|   |
| DEGEN_GEOM_CSV_TYPE | 1<<5|   |
| DEGEN_GEOM_M_TYPE | 1<<6|   |
| CFD_STL_TYPE | 1<<7|   |
| CFD_POLY_TYPE | 1<<8|   |
| CFD_TRI_TYPE | 1<<9|   |
| CFD_OBJ_TYPE | 1<<10|   |
| CFD_DAT_TYPE | 1<<11|   |
| CFD_KEY_TYPE | 1<<12|   |
| CFD_GMSH_TYPE | 1<<13|   |
| CFD_SRF_TYPE_DEPRECATED | 1<<14|   |
| CFD_TKEY_TYPE | 1<<15|   |
| PROJ_AREA_CSV_TYPE | 1<<16|   |
| WAVE_DRAG_TXT_TYPE | 1<<17|   |
| VSPAERO_PANEL_TRI_TYPE | 1<<18|   |
| DRAG_BUILD_CSV_TYPE | 1<<19|   |
| CFD_FACET_TYPE | 1<<20|   |
| CFD_CURV_TYPE_DEPRECATED | 1<<21|   |
| CFD_PLOT3D_TYPE_DEPRECATED | 1<<22|   |
| CFD_VSPGEOM_TYPE | 1<<23|   |
| VSPAERO_VSPGEOM_TYPE | 1<<24|   |




Enum used to identify various export file types. 


### enum CONFORMAL_TRIM_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| U_TRIM | |  Trim by U coordinate  |
| L_TRIM | |  Trim by L coordinate  |
| ETA_TRIM | |  Trim by Eta coordinate  |
| NUM_TRIM_TYPES | |  Number of conformal component trim types  |




Enum used to identify conformal component trim type. 


### enum DELIM_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DELIM_COMMA | |  Comma delimiter  |
| DELIM_USCORE | |  Underscore delimiter  |
| DELIM_SPACE | |  Space delimiter  |
| DELIM_NONE | |  No delimiter  |
| DELIM_NUM_TYPES | |  Number of delimiter types  |




Enum used to identify delimiter type. 


### enum DEPTH_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DEPTH_FRONT | |  Set 3D background before model  |
| DEPTH_REAR | |  Set 3D background behind model  |
| DEPTH_FREE | |  Set 3D background at specified location  |
| NUM_DEPTH_TYPE | |  Number of depth types  |




Enum for 3D background depth location settings. 


### enum DIMENSION_SET

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SET_3D | |  3D DXF export (default)  |
| SET_2D | |  2D DXF export  |




Enum for 2D or 3D DXF export options. 


### enum DIR_INDEX

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| X_DIR | 0|  X direction  |
| Y_DIR | 1|   |
| Z_DIR | 2|   |
| ALL_DIR | 3|   |




Enum used to identify axis of rotation or translation. 


### enum DISPLAY_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| DISPLAY_BEZIER | |  Display the normal Bezier surface (default)  |
| DISPLAY_DEGEN_SURF | |  Display as surface Degen Geom  |
| DISPLAY_DEGEN_PLATE | |  Display as plate Degen Geom  |
| DISPLAY_DEGEN_CAMBER | |  Display as camber Degen Geom  |




Enum for selecting the GUI display type for Geoms. 


### enum DRAW_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| GEOM_DRAW_WIRE | |  Draw the wireframe mesh (see through)  |
| GEOM_DRAW_HIDDEN | |  Draw the hidden mesh  |
| GEOM_DRAW_SHADE | |  Draw the shaded mesh  |
| GEOM_DRAW_TEXTURE | |  Draw the textured mesh  |
| GEOM_DRAW_NONE | |  Do not draw anything  |




Enum for selecting the GUI draw type for Geoms. 


### enum ENGINE_GEOM_IO_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ENGINE_GEOM_NONE | |  Component is not an integrated flowpath component.  |
| ENGINE_GEOM_INLET | |  Component represents integrated flowpath inlet.  |
| ENGINE_GEOM_INLET_OUTLET | |  Component represents integrated flowpath inlet and outlet.  |
| ENGINE_GEOM_OUTLET | |  Component represents integrated flowpath outlet.  |
| ENGINE_GEOM_IO_NUM_TYPES | |  Number of integrated flowpath component types.  |




Enum for identifying which kind of integrated flowpath modeling components is modeled. 


### enum ENGINE_GEOM_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ENGINE_GEOM_FLOWTHROUGH | |  Component is modeled as flowthrough engine.  |
| ENGINE_GEOM_TO_LIP | |  Component is modeled to the lip.  |
| ENGINE_GEOM_FLOWPATH | |  Component flowpath is modeled.  |
| ENGINE_GEOM_TO_FACE | |  Component is modeled to face.  |
| ENGINE_GEOM_NUM_TYPES | |  Number of integrated flowpath modeling types.  |




Enum for identifying how integrated flowpath modeling engine is represented. 


### enum ENGINE_LOC_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ENGINE_LOC_INDEX | |  Integrated flowpath key point identified by XSec index.  |
| ENGINE_LOC_U | |  Integrated flowpath key point identified by U parameter.  |




Enum for how integrated flowpath modeling key points are identified. 


### enum ENGINE_LOC_INDEX_TYPES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ENGINE_LOC_INLET_LIP | |  Integrated flowpath key point is inlet lip.  |
| ENGINE_LOC_INLET_FACE | |  Integrated flowpath key point is inlet face.  |
| ENGINE_LOC_OUTLET_LIP | |  Integrated flowpath key point is outlet lip.  |
| ENGINE_LOC_OUTLET_FACE | |  Integrated flowpath key point is outlet face.  |
| ENGINE_LOC_NUM | |  Number of integrated flowpath key point locations.  |




Enum for integrated flowpath modeling key points. 


### enum ENGINE_MODE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ENGINE_MODE_FLOWTHROUGH | |  Represent integrated flowpath as flowthrough engine.  |
| ENGINE_MODE_FLOWTHROUGH_NEG | |  Represent integrated flowpath as flowthrough engine with negative flowpath.  |
| ENGINE_MODE_FLOWTHROUGH_NEG_ONLY | |  Represent ONLY the integrated flowpath as flowthrough engine with negative flowpath.  |
| ENGINE_MODE_TO_LIP | |  Represent integrated flowpath to the lip.  |
| ENGINE_MODE_TO_FACE | |  Represent integrated flowpath to the face.  |
| ENGINE_MODE_TO_FACE_NEG | |  Represent integrated flowpath to the face with negative flowpath to the face.  |
| ENGINE_MODE_TO_FACE_NEG_ONLY | |  Represent ONLY the integrated flowpath to the face with negative flowpath to the face.  |
| ENGINE_MODE_EXTEND | |  Represent integrated flowpath with farfield extensions.  |
| ENGINE_MODE_NUM_TYPES | |  Number of integrated flowpath representations.  |




Enum for identifying how integrated flowpath modeling components are modeled. 


### enum ERROR_CODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| VSP_OK | |  No error  |
| VSP_INVALID_PTR | |  Invalid pointer error  |
| VSP_INVALID_TYPE | |  Invalid type error  |
| VSP_CANT_FIND_TYPE | |  Can't find type error  |
| VSP_CANT_FIND_PARM | |  Can't find parm error  |
| VSP_CANT_FIND_NAME | |  Can't find name error  |
| VSP_INVALID_GEOM_ID | |  Invalid Geom ID error  |
| VSP_FILE_DOES_NOT_EXIST | |  File does not exist error  |
| VSP_FILE_WRITE_FAILURE | |  File write failure error  |
| VSP_FILE_READ_FAILURE | |  File read failure error  |
| VSP_WRONG_GEOM_TYPE | |  Wrong Geom type error  |
| VSP_WRONG_XSEC_TYPE | |  Wrong XSec type error  |
| VSP_WRONG_FILE_TYPE | |  Wrong file type error  |
| VSP_INDEX_OUT_RANGE | |  Index out of range error  |
| VSP_INVALID_XSEC_ID | |  Invalid XSec ID error  |
| VSP_INVALID_ID | |  Invalid ID error  |
| VSP_CANT_SET_NOT_EQ_PARM | |  Can't set NotEqParm error  |
| VSP_AMBIGUOUS_SUBSURF | |  Ambiguous flow-through sub-surface error  |
| VSP_INVALID_VARPRESET_SETNAME | |  Invalid Variable Preset set name error  |
| VSP_INVALID_VARPRESET_GROUPNAME | |  Invalid Variable Preset group name error  |
| VSP_CONFORMAL_PARENT_UNSUPPORTED | |  Unsupported Conformal Geom parent error  |
| VSP_UNEXPECTED_RESET_REMAP_ID | |  Unexpected reset remap ID error  |
| VSP_INVALID_INPUT_VAL | |  Invalid input value error  |
| VSP_INVALID_CF_EQN | |  Invalid friction coefficient equation error  |
| VSP_INVALID_DRIVERS | |  Invalid drivers for driver group  |
| VSP_ADV_LINK_BUILD_FAIL | |  Advanced link build failure  |
| VSP_DEPRECATED | |  This capability has been deprecated and is not longer supported  |
| VSP_LINK_LOOP_DETECTED | |  A parameter link loop was detected and stopped  |
| VSP_LINK_OUTPUT_NOT_ASSIGNED | |  An output of a parameter link was not set  |
| VSP_DUPLICATE_NAME | |  A duplicate name has been provided  |
| VSP_GUI_DEVICE_DEACTIVATED | |  A deactivated GUI device was touched  |
| VSP_COULD_NOT_CREATE_BACKGROUND3D | |  Could not create and add Background3D  |
| VSP_NUM_ERROR_CODE | |  Total number of VSP error codes  |




Enum for OpenVSP API error codes. 


### enum EXCRES_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| EXCRESCENCE_COUNT | 0|  Drag counts excressence type  |
| EXCRESCENCE_CD | |  Drag coefficient excressence type  |
| EXCRESCENCE_PERCENT_GEOM | |  Percent of parent Geom drag coefficient excressence type  |
| EXCRESCENCE_MARGIN | |  Percent margin excressence type  |
| EXCRESCENCE_DRAGAREA | |  Drag area (D/q) excressence type  |




Enum used to indicate Parasite Drag Tool excressence type. 


### enum EXPORT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| EXPORT_FELISA | |  FELISA export type (NOT IMPLEMENTED)  |
| EXPORT_XSEC | |  XSec (*.hrm) export type  |
| EXPORT_STL | |  Stereolith (*.stl) export type  |
| EXPORT_AWAVE | |  AWAVE export type (NOT IMPLEMENTED)  |
| EXPORT_NASCART | |  NASCART (*.dat) export type  |
| EXPORT_POVRAY | |  POVRAY (*.pov) export type  |
| EXPORT_CART3D | |  Cart3D (*.tri) export type  |
| EXPORT_VSPGEOM | |  VSPGeom (*.vspgeom) export type  |
| EXPORT_VORXSEC | |  VORXSEC export type (NOT IMPLEMENTED)  |
| EXPORT_XSECGEOM | |  XSECGEOM export type (NOT IMPLEMENTED)  |
| EXPORT_GMSH | |  Gmsh (*.msh) export type  |
| EXPORT_X3D | |  X3D (*.x3d) export type  |
| EXPORT_STEP | |  STEP (*.stp) export type  |
| EXPORT_PLOT3D | |  PLOT3D (*.p3d) export type  |
| EXPORT_IGES | |  IGES (*.igs) export type  |
| EXPORT_BEM | |  Blade Element (*.bem) export type  |
| EXPORT_DXF | |  AutoCAD (*.dxf) export type  |
| EXPORT_FACET | |  Xpatch (*.facet) export type  |
| EXPORT_SVG | |  SVG (*.svg) export type  |
| EXPORT_PMARC | |  PMARC 12 (*.pmin) export type  |
| EXPORT_OBJ | |  OBJ (*.obj) export type  |
| EXPORT_SELIG_AIRFOIL | |  Airfoil points (*.dat) export type  |
| EXPORT_BEZIER_AIRFOIL | |  Airfoil curves (*.bz) export type  |
| EXPORT_IGES_STRUCTURE | |  IGES structure (*.igs) export type  |
| EXPORT_STEP_STRUCTURE | |  STEP structure (*.stp) export type  |




Enum for OpenVSP export types. 


### enum FEA_BC_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_BCM_USER | |  FEA boundary condition constraints user defined.  |
| FEA_BCM_ALL | |  FEA boundary condition constrains all DOF.  |
| FEA_BCM_PIN | |  FEA boundary condition pin constraints.  |
| FEA_BCM_SYMM | |  FEA boundary condition symmetrical constraints.  |
| FEA_BCM_ASYMM | |  FEA boundary condition antisymmetrical constraints.  |
| FEA_NUM_BCM_MODES | |  Number of FEA boundary condition constraint types.  |




Enum used to indicate FEA boundary condition constraint type. 


### enum FEA_BC_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_BC_STRUCTURE | |  FEA boundary condition assigned to structure.  |
| FEA_BC_PART | |  FEA boundary condition assigned to part.  |
| FEA_BC_SUBSURF | |  FEA boundary condition assigned to subsurface.  |
| FEA_NUM_BC_TYPES | |  Number of FEA boundary condition definition types.  |




Enum used to indicate FEA boundary condition definition type. 


### enum FEA_CROSS_SECT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_XSEC_GENERAL | 0|  General XSec type  |
| FEA_XSEC_CIRC | |  Circle XSec type  |
| FEA_XSEC_PIPE | |  Pipe XSec type  |
| FEA_XSEC_I | |  I XSec type  |
| FEA_XSEC_RECT | |  Rectangle XSec type  |
| FEA_XSEC_BOX | |  Box XSec type  |




Enum used to indicate FEA beam element cross-section type. 


### enum FEA_EXPORT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_MASS_FILE_NAME | |  FEA Mesh mass export type  |
| FEA_NASTRAN_FILE_NAME | |  FEA Mesh NASTRAN export type  |
| FEA_NKEY_FILE_NAME | |  FEA Mesh NKey export type  |
| FEA_CALCULIX_FILE_NAME | |  FEA Mesh Calculix export type  |
| FEA_STL_FILE_NAME | |  FEA Mesh STL export type  |
| FEA_GMSH_FILE_NAME | |  FEA Mesh GMSH export type  |
| FEA_SRF_FILE_NAME | |  FEA Mesh SRF export type  |
| FEA_CURV_FILE_NAME | |  FEA Mesh CURV export type  |
| FEA_PLOT3D_FILE_NAME | |  FEA Mesh PLOT3D export type  |
| FEA_IGES_FILE_NAME | |  FEA Mesh trimmed IGES export type  |
| FEA_STEP_FILE_NAME | |  FEA Mesh trimmed STEP export type  |
| FEA_NUM_FILE_NAMES | |  Number of FEA Mesh export type.  |




Enum for the various FEA Mesh export types. 


### enum FEA_FIX_PT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_FIX_PT_ON_BODY | |  On body fixed point type  |
| FEA_FIX_PT_GLOBAL_XYZ | |  Global XYZ off body fixed point type  |
| FEA_FIX_PT_DELTA_XYZ | |  Delta XYZ off body fixed point type  |
| FEA_FIX_PT_DELTA_UVN | |  Delta UVN off body fixed point type  |
| FEA_FIX_PT_GEOM_ORIGIN | |  Geom origin off body fixed point type  |
| FEA_FIX_PT_GEOM_CG | |  Geom CG off body fixed point type  |
| FEA_NUM_FIX_PT_TYPES | |  Number of off body fixed point types  |




Enum for FEA fixed point types. 


### enum FEA_MATERIAL_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_ISOTROPIC | |  Isotropic material  |
| FEA_ENG_ORTHO | |  Orthotropic material in engineering parameters  |
| FEA_ENG_ORTHO_TRANS_ISO | |  Orthotropic material with transverse isotropy assumed in engineering parameters  |
| FEA_LAMINATE | |  Laminate buildup material  |
| FEA_NUM_MAT_TYPES | |  Number of FEA material types  |




Enum for FEA material types. 


### enum FEA_ORIENTATION_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_ORIENT_GLOBAL_X | |  FEA Global X material orientation  |
| FEA_ORIENT_GLOBAL_Y | |  FEA Global Y material orientation  |
| FEA_ORIENT_GLOBAL_Z | |  FEA Global Z material orientation  |
| FEA_ORIENT_COMP_X | |  FEA Comp X material orientation  |
| FEA_ORIENT_COMP_Y | |  FEA Comp Y material orientation  |
| FEA_ORIENT_COMP_Z | |  FEA Comp Z material orientation  |
| FEA_ORIENT_PART_U | |  FEA Part U material orientation  |
| FEA_ORIENT_PART_V | |  FEA Part V material orientation  |
| FEA_ORIENT_OML_U | |  FEA OML U material orientation  |
| FEA_ORIENT_OML_V | |  FEA OML V material orientation  |
| FEA_ORIENT_OML_R | |  FEA OML R material orientation  |
| FEA_ORIENT_OML_S | |  FEA OML S material orientation  |
| FEA_ORIENT_OML_T | |  FEA OML T material orientation  |
| FEA_NUM_ORIENT_TYPES | |  Number of FEA material orientation types  |




Enum for FEA material orientation types. 


### enum FEA_PART_ELEMENT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_DEPRECATED | -1|  Flag for deprecated element type option  |
| FEA_SHELL | 0|  Shell (tris) FEA element type  |
| FEA_BEAM | |  Beam FEA element type  |
| FEA_SHELL_AND_BEAM | |  Both Shell and Beam FEA element types  |
| FEA_NO_ELEMENTS | |  FEA part with no elements  |
| FEA_NUM_ELEMENT_TYPES | |  Number of FEA element type choices  |




Enum for FEA Part element types. 


### enum FEA_PART_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_SLICE | 0|  Slice FEA Part type  |
| FEA_RIB | |  Rib FEA Part type  |
| FEA_SPAR | |  Spar FEA Part type  |
| FEA_FIX_POINT | |  Fixed Point FEA Part type  |
| FEA_DOME | |  Dome FEA Part type  |
| FEA_RIB_ARRAY | |  Rib array FEA Part type  |
| FEA_SLICE_ARRAY | |  Slice array FEA Part type  |
| FEA_SKIN | |  Skin FEA Part type  |
| FEA_TRIM | |  Trim FEA Part type  |
| FEA_POLY_SPAR | |  Poly Spar FEA Part type  |
| FEA_NUM_TYPES | |  Number of FEA Part types  |




Enum used to identify the available FEA Part types. 


### enum FEA_RIB_NORMAL

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NO_NORMAL | |  FEA Rib or Rib Array has no set perpendicular edge  |
| LE_NORMAL | |  FEA Rib or Rib Array is set perpendicular to the leading edge  |
| TE_NORMAL | |  FEA Rib or Rib Array is set perpendicular to the trailing edge  |
| SPAR_NORMAL | |  FEA Rib or Rib Array is set perpendicular to an FEA Spar  |




Enum that defines the type of edge to set the initial position of FEA Ribs and FEA Rib Arrays to. 


### enum FEA_SHELL_TREATMENT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FEA_KEEP | 0|  Keep shell elements  |
| FEA_DELETE | |  Delete shell elements  |
| FEA_NUM_SHELL_TREATMENT_TYPES | |  Number of FEA subsurface treatment choices  |




Enum for FEA Shell treatment types. 


### enum FEA_SLICE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| XY_BODY | 0|  Slice is parallel to parent Geom body XY plane  |
| YZ_BODY | |  Slice is parallel to parent Geom body YZ plane  |
| XZ_BODY | |  Slice is parallel to parent Geom body XZ plane  |
| XY_ABS | |  Slice is parallel to absolute XY plane  |
| YZ_ABS | |  Slice is parallel to absolute YZ plane  |
| XZ_ABS | |  Slice is parallel to absolute XZ plane  |
| SPINE_NORMAL | |  Slice is perpendicular to thespine of the parent Geom  |




Enum for FEA Slice orientation. 


### enum FEA_POLY_SPAR_POINT

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| POLY_SPAR_POINT_U01 | |  Spar points span specified in U01  |
| POLY_SPAR_POINT_U0N | |  Spar points span specified in U0N  |
| POLY_SPAR_POINT_ETA | |  Spar points span specified in eta  |
| NUM_POLY_SPAR_POINT_TYPES | |  Number of poly spar point types  |




Enum for FEA Poly spar point types. 


### enum FEA_UNIT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SI_UNIT | 0|  FEA Files output in (m, kg)  |
| CGS_UNIT | |  FEA Files output in (cm, g)  |
| MPA_UNIT | |  FEA Files output in (mm, tonne)  |
| BFT_UNIT | |  FEA Files output in (ft, slug)  |
| BIN_UNIT | |  FEA Files output in (in, lbf*sec^2/in)  |




Enum used to identify the FEA Mesh unit system (length, mass). 


### enum FF_B_EQN

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FF_B_MANUAL | 0|  Manual FF equation  |
| FF_B_SCHEMENSKY_FUSE | |  Schemensky Fuselage FF equation  |
| FF_B_SCHEMENSKY_NACELLE | |  Schemensky Nacelle FF equation  |
| FF_B_HOERNER_STREAMBODY | |  Hoerner Streamlined Body FF equation  |
| FF_B_TORENBEEK | |  Torenbeek FF equation  |
| FF_B_SHEVELL | |  Shevell FF equation  |
| FF_B_COVERT | |  Covert FF equation  |
| FF_B_JENKINSON_FUSE | |  Jenkinson Fuselage FF equation  |
| FF_B_JENKINSON_WING_NACELLE | |  Jenkinson Wing Nacelle FF equation  |
| FF_B_JENKINSON_AFT_FUSE_NACELLE | |  Jenkinson Aft Fuselage Nacelle FF equation  |




Enum for Parasite Drag Tool form factor equations for body-type components. 


### enum FF_W_EQN

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FF_W_MANUAL | 0|  Manual FF equation  |
| FF_W_EDET_CONV | |  EDET Conventional Airfoil FF equation  |
| FF_W_EDET_ADV | |  EDET Advanced Airfoil FF equation  |
| FF_W_HOERNER | |  Hoerner FF equation  |
| FF_W_COVERT | |  Covert FF equation  |
| FF_W_SHEVELL | |  Shevell FF equation  |
| FF_W_KROO | |  Kroo FF equation  |
| FF_W_TORENBEEK | |  Torenbeek FF equation  |
| FF_W_DATCOM | |  DATCOM FF equation  |
| FF_W_SCHEMENSKY_6_SERIES_AF | |  Schemensky 6 Series Airfoil FF equation  |
| FF_W_SCHEMENSKY_4_SERIES_AF | |  Schemensky 4 Series Airfoil FF equation  |
| FF_W_JENKINSON_WING | |  Jenkinson Wing FF equation  |
| FF_W_JENKINSON_TAIL | |  Jenkinson Tail FF equation  |
| FF_W_SCHEMENSKY_SUPERCRITICAL_AF | |  Schemensky Supercritical Airfoil FF equation  |




Enum for Parasite Drag Tool form factor equations for wing-type components. 


### enum FREESTREAM_PD_UNITS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| PD_UNITS_IMPERIAL | 0|  Imperial unit system  |
| PD_UNITS_METRIC | |  Metric unit system  |




Enum for Parasite Drag Tool freestream unit system. 


### enum FILE_CHOOSER_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| OPEN | |  Browse files that already exist  |
| SAVE | |  Browse file system and enter file name  |
| NUM_FILE_CHOOSER_MODES | |  Number of file chooser modes  |




Enum for setting the mode of the file chooser. 


### enum FILE_CHOOSER_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FC_OPENVSP | |  OpenVSP's own file chooser with directory preferences.  |
| FC_NATIVE | |  Operating system's native file chooser  |
| NUM_FILE_CHOOSER_TYPES | |  Number of file chooser types  |




Enum for file chooser type. 


### enum GDEV

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| GDEV_TAB | |  Custom GUI Tab  |
| GDEV_SCROLL_TAB | |  Custom GUI Fl_Scroll and Tab  |
| GDEV_GROUP | |  Custom GUI Group  |
| GDEV_PARM_BUTTON | |  Custom GUI ParmButton  |
| GDEV_INPUT | |  Custom GUI Input  |
| GDEV_OUTPUT | |  Custom GUI Output  |
| GDEV_SLIDER | |  Custom GUI Slider  |
| GDEV_SLIDER_ADJ_RANGE | |  Custom GUI SliderAdjRangeInput  |
| GDEV_CHECK_BUTTON | |  Custom GUI CheckButton  |
| GDEV_CHECK_BUTTON_BIT | |  Custom GUI CheckButtonBit  |
| GDEV_RADIO_BUTTON | |  Custom GUI RadioButton  |
| GDEV_TOGGLE_BUTTON | |  Custom GUI ToggleButton  |
| GDEV_TOGGLE_BUTTON_FREE | |  Custom GUI ToggleButton without Parm  |
| GDEV_TOGGLE_RADIO_GROUP | |  Custom GUI ToggleRadioGroup (NOT IMPLEMENTED)  |
| GDEV_TRIGGER_BUTTON | |  Custom GUI TriggerButton  |
| GDEV_COUNTER | |  Custom GUI Counter  |
| GDEV_CHOICE | |  Custom GUI Choice  |
| GDEV_ADD_CHOICE_ITEM | |  Add item to custom GUI Choice  |
| GDEV_SLIDER_INPUT | |  Custom GUI SliderInput  |
| GDEV_SLIDER_ADJ_RANGE_INPUT | |  Custom GUI SliderAdjRangeInput  |
| GDEV_SLIDER_ADJ_RANGE_TWO_INPUT | |  Custom GUI SliderAdjRangeInput with two inputs (NOT IMPLEMENTED)  |
| GDEV_FRACT_PARM_SLIDER | |  Custom GUI FractParmSlider  |
| GDEV_STRING_INPUT | |  Custom GUI StringInput  |
| GDEV_INDEX_SELECTOR | |  Custom GUI IndexSelector  |
| GDEV_COLOR_PICKER | |  Custom GUI ColorPicker  |
| GDEV_YGAP | |  Custom GUI Y gap  |
| GDEV_DIVIDER_BOX | |  Custom GUI divider box  |
| GDEV_BEGIN_SAME_LINE | |  Set begin same line flag for custom GUI  |
| GDEV_END_SAME_LINE | |  Set end same line flag for custom GUI  |
| GDEV_FORCE_WIDTH | |  Set forced width for custom GUI  |
| GDEV_SET_FORMAT | |  Set format label for custom GUI  |
| NUM_GDEV_TYPES | |  Number of [GDEV](Modules/group___enumerations.md#enum-gdev) types  |
| ALL_GDEV_TYPES | |  Flag for all [GDEV](Modules/group___enumerations.md#enum-gdev) types  |




Enum used for custom GUI development. 


### enum GEAR_CONFIGURATION_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| GEAR_CONFIGURATION_DOWN | |  Gear drawn down  |
| GEAR_CONFIGURATION_UP | |  Gear drawn up  |
| GEAR_CONFIGURATION_UP_AND_DOWN | |  Gear drawn both up and down  |
| GEAR_CONFIGURATION_INTERMEDIATE | |  Gear drawn somewhere beteween down and up  |
| GEAR_CONFIGURATION_ALL | |  Gear drawn in all configurations  |
| NUM_GEAR_CONFIGURATION_MODES | |  Number of gear configuration choices  |




Enum for gear configuration modes. 


### enum GEAR_RETRACT_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| GEAR_STOWED_POSITION | |  Specified by stowed position  |
| GEAR_MECHANISM | |  Specified by mechanism  |
| NUM_GEAR_RETRACT_MODES | |  Number of gear retract choices  |




Enum for gear retract modes. 


### enum GEAR_SUSPENSION_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| GEAR_SUSPENSION_NOMINAL | |  Gear suspension at nominal extension  |
| GEAR_SUSPENSION_COMPRESSED | |  Gear suspension is compressed  |
| GEAR_SUSPENSION_EXTENDED | |  Gear suspension is extended  |
| NUM_GEAR_SUSPENSION_MODES | |  Number of gear suspension choices  |




Enum for tire dimension modes. 


### enum GENDER

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| MALE | |  Male Human component  |
| FEMALE | |  Female Human component  |




Enum for OpenVSP Human component gender types. 


### enum GEOMETRY_ANALYSIS_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| EXTERNAL_INTERFERENCE | |  Interference between mutually external bodies  |
| PACKAGING_INTERFERENCE | |  Interference when one body is internal to another  |
| EXTERNAL_SELF_INTERFERENCE | |  Interference between multiple surfaces of one Geom / Set  |
| PLANE_STATIC_DISTANCE_INTERFERENCE | |  Interference between surfaces and a plane  |
| PLANE_2PT_ANGLE_INTERFERENCE | |  Interference angle between surfaces and a plane  |
| GEAR_CG_TIPBACK_ANALYSIS | |  Calculate tipback angle  |
| PLANE_1PT_ANGLE_INTERFERENCE | |  Interference roll angle between surfaces and a plane  |
| GEAR_WEIGHT_DISTRIBUTION_ANALYSIS | |  Calculate distribution of weight across landing gear  |
| GEAR_TIPOVER_ANALYSIS | |  Calculate tipover angle  |
| GEAR_TURN_ANALYSIS | |  Calculate ground manueveribility  |
| VISIBLE_FROM_POINT_ANALYSIS | |  Calculate az,el domain visible from a point  |
| CCE_INTERFERENCE | |  Interference with composite clearance envelope  |
| LINEAR_SWEPT_VOLUME_ANALYSIS | |  Interference with linear swept volume  |
| VISIBLE_AT_SURF_ANALYSIS | |  Calculate visibility of a surface from a direction  |
| NUM_INTERFERENCE_TYPES | |  Number of interference check types  |




Geometry analysis types.. 


### enum GUI_GEOM_SCREEN

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| POD_GEOM_SCREEN | |  Pod geom screen  |
| FUSELAGE_GEOM_SCREEN | |  Fuselage geom screen  |
| MS_WING_GEOM_SCREEN | |  Wing geom screen  |
| BLANK_GEOM_SCREEN | |  Blank geom screen  |
| MESH_GEOM_SCREEN | |  Mesh geom screen  |
| NGON_MESH_GEOM_SCREEN | |  NGon Mesh geom screen  |
| STACK_GEOM_SCREEN | |  Stack geom screen  |
| CUSTOM_GEOM_SCREEN | |  Custom geom screen  |
| PT_CLOUD_GEOM_SCREEN | |  Point cloud geom screen  |
| PROP_GEOM_SCREEN | |  Propeller geom screen  |
| HINGE_GEOM_SCREEN | |  Hinge geom screen  |
| MULT_GEOM_SCREEN | |  Multiple geom screen  |
| CONFORMAL_SCREEN | |  Conformal geom screen  |
| ELLIPSOID_GEOM_SCREEN | |  Ellipsoid geom screen  |
| BOR_GEOM_SCREEN | |  Body of revolution geom screen  |
| WIRE_FRAME_GEOM_SCREEN | |  Wireframe geom screen  |
| HUMAN_GEOM_SCREEN | |  Human geom screen  |
| ROUTING_GEOM_SCREEN | |  Routing geom screen  |
| AUXILIARY_GEOM_SCREEN | |  Auxiliary geom screen  |
| GEAR_GEOM_SCREEN | |  Gear geom screen  |
| COBRA_GEOM_SCREEN | |  Cobra body geom screen  |
| NUM_GEOM_SCREENS | |  Number of geom screens  |
| ALL_GEOM_SCREENS | |  All geom screens  |




Enum for geom screen types. 


### enum GUI_VSP_SCREEN

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| VSP_ADV_LINK_SCREEN | |  Advanced linking screen  |
| VSP_ADV_LINK_VAR_RENAME_SCREEN | |  Advanced link variable rename screen  |
| VSP_AERO_STRUCT_SCREEN | |  Aero / structural analysis screen  |
| VSP_AIRFOIL_CURVES_EXPORT_SCREEN | |  Airfoil curves export screen  |
| VSP_AIRFOIL_POINTS_EXPORT_SCREEN | |  Airfoil points screen  |
| VSP_ATTRIBUTE_EXPLORER_SCREEN | |  Attribute details screen  |
| VSP_BACKGROUND_SCREEN | |  Background control screen  |
| VSP_BACKGROUND3D_SCREEN | |  Background3D control screen  |
| VSP_BACKGROUND3D_PREVIEW_SCREEN | |  Background3D preview screen  |
| VSP_BEM_OPTIONS_SCREEN | |  Blade element method options screen  |
| VSP_CFD_MESH_SCREEN | |  CFD Mesh screen  |
| VSP_CLIPPING_SCREEN | |  Clipping screen  |
| VSP_COMP_GEOM_SCREEN | |  CompGeom screen  |
| VSP_COR_SCREEN | |  Center of rotation screen  |
| VSP_CURVE_EDIT_SCREEN | |  Curve edit screen  |
| VSP_DEGEN_GEOM_SCREEN | |  Degen geom screen  |
| VSP_DESIGN_VAR_SCREEN | |  Design variables screen  |
| VSP_DXF_OPTIONS_SCREEN | |  DXF options screen  |
| VSP_EXPORT_SCREEN | |  Export screen  |
| VSP_FEA_PART_EDIT_SCREEN | |  FEA Part edit screen  |
| VSP_FEA_XSEC_SCREEN | |  FEA XSec screen  |
| VSP_FIT_MODEL_SCREEN | |  Fit model screen  |
| VSP_IGES_OPTIONS_SCREEN | |  IGES options screen  |
| VSP_IGES_STRUCTURE_OPTIONS_SCREEN | |  IGES structure options screen  |
| VSP_EXPORT_CUSTOM_SCRIPT | |  Custom geom export screen  |
| VSP_GEOMETRY_ANALYSIS_SCREEN | |  Geometry analysis screen  |
| VSP_IMPORT_SCREEN | |  Import screen  |
| VSP_LIGHTING_SCREEN | |  Lighting screen  |
| VSP_MANAGE_GEOM_SCREEN | |  Manage geom screen  |
| VSP_MANAGE_TEXTURE_SCREEN | |  Texture mapping screen  |
| VSP_MASS_PROP_SCREEN | |  Mass properties screen  |
| VSP_MATERIAL_EDIT_SCREEN | |  Material edit screen  |
| VSP_MEASURE_SCREEN | |  Measure screen  |
| VSP_MODE_EDITOR_SCREEN | |  Mode editor screen  |
| VSP_NERF_MANAGE_GEOM_SCREEN | |  NERF'ed (limited to make safe) Manage geom screen  |
| VSP_SNAP_TO_SCREEN | |  Snap to screen  |
| VSP_PARASITE_DRAG_SCREEN | |  Parasite drg screen  |
| VSP_PARM_DEBUG_SCREEN | |  Parameter debug screen  |
| VSP_PARM_LINK_SCREEN | |  Parameter linking screen  |
| VSP_PARM_SCREEN | |  Parameter screen  |
| VSP_PICK_SET_SCREEN | |  Pick set screen  |
| VSP_PREFERENCES_SCREEN | |  Preferences screen  |
| VSP_PROJECTION_SCREEN | |  Projected area screen  |
| VSP_PSLICE_SCREEN | |  Planar slicing screen  |
| VSP_RESULTS_VIEWER_SCREEN | |  Results viewing screen  |
| VSP_SCREENSHOT_SCREEN | |  Screenshot screen  |
| VSP_SELECT_FILE_SCREEN | |  Select file screen  |
| VSP_SET_EDITOR_SCREEN | |  Set editor screen  |
| VSP_STEP_OPTIONS_SCREEN | |  STEP options screen  |
| VSP_STEP_STRUCTURE_OPTIONS_SCREEN | |  STEP structure options screen  |
| VSP_STL_OPTIONS_SCREEN | |  STL options screen  |
| VSP_STRUCT_SCREEN | |  Structure definition screen  |
| VSP_STRUCT_ASSEMBLY_SCREEN | |  Structure assembly screen  |
| VSP_SURFACE_INTERSECTION_SCREEN | |  Surface intersection screen  |
| VSP_SVG_OPTIONS_SCREEN | |  SVG options screen  |
| VSP_USER_PARM_SCREEN | |  User parameter screen  |
| VSP_VAR_PRESET_SCREEN | |  Variable presets editor screen  |
| VSP_VEH_NOTES_SCREEN | |  Vehicle notes screen  |
| VSP_VEH_SCREEN | |  Veh geom screen  |
| VSP_VIEW_SCREEN | |  Adjust viewpoint screen  |
| VSP_VSPAERO_PLOT_SCREEN | |  VSPAERO results manager screen  |
| VSP_VSPAERO_SCREEN | |  VSPAERO screen  |
| VSP_XSEC_SCREEN | |  XSec screen  |
| VSP_WAVEDRAG_SCREEN | |  Wave drag screen  |
| VSP_MAIN_SCREEN | |  Main screen  |
| VSP_NUM_SCREENS | |  Number of screens  |
| VSP_ALL_SCREENS | |  Flag for all screens  |




Enum for OpenVSP screen types. 


### enum INIT_EDIT_XSEC_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| EDIT_XSEC_CIRCLE | |  Circle initialized as cubic Bezier type  |
| EDIT_XSEC_ELLIPSE | |  Ellipse initialized as PCHIP type  |
| EDIT_XSEC_RECTANGLE | |  Rectangle initialized as linear type  |
| NUM_INIT_EDIT_XSEC_TYPES | |  Number of initializable edit curve types  |




Initial shape enums for XS_EDIT_CURVE type XSecs. 


### enum IMPORT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| IMPORT_STL | |  Stereolith (*.stl) import  |
| IMPORT_NASCART | |  NASCART (*.dat) import  |
| IMPORT_CART3D_TRI | |  Cart3D (*.try) import  |
| IMPORT_XSEC_MESH | |  XSec as Tri Mesh (*.hrm) import  |
| IMPORT_PTS | |  Point Cloud (*.pts) import  |
| IMPORT_V2 | |  OpenVSP v2 (*.vsp) import  |
| IMPORT_BEM | |  Blade Element (*.bem) import  |
| IMPORT_XSEC_WIRE | |  XSec as Wireframe (*.hrm) import  |
| IMPORT_P3D_WIRE | |  Plot3D as Wireframe (*.p3d) import  |




Enum for OpenVSP import types. 


### enum INTERSECT_EXPORT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| INTERSECT_SRF_FILE_NAME | |  SRF intersection file type  |
| INTERSECT_CURV_FILE_NAME | |  CURV intersection file type  |
| INTERSECT_PLOT3D_FILE_NAME | |  PLOT3D intersection file type  |
| INTERSECT_IGES_FILE_NAME | |  IGES intersection file type  |
| INTERSECT_STEP_FILE_NAME | |  STEP intersection file type  |
| INTERSECT_NUM_FILE_NAMES | |  Number of surface intersection file types  |




Enum for Surface Intersection export file types. 


### enum LEN_UNITS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| LEN_MM | |  Millimeter  |
| LEN_CM | |  Centimeter  |
| LEN_M | |  Meter  |
| LEN_IN | |  Inch  |
| LEN_FT | |  Feet  |
| LEN_YD | |  Yard  |
| LEN_UNITLESS | |  Unitless  |
| NUM_LEN_UNIT | |  Number of length unit types  |




Enum that describes units for length. 


### enum MASS_UNIT

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| MASS_UNIT_G | 0|  Gram  |
| MASS_UNIT_KG | |  Kilogram  |
| MASS_UNIT_TONNE | |  Tonne  |
| MASS_UNIT_LBM | |  Pound-mass  |
| MASS_UNIT_SLUG | |  Slug  |
| MASS_LBFSEC2IN | |  lbf*sec^2/in  |
| NUM_MASS_UNIT | |  Number of mass unit types  |




Enum that describes units for mass. 


### enum MESH_REASON

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NO_REASON | |  No reason determined.  |
| MAX_LEN_CONSTRAINT | |  Maximum edge length.  |
| CURV_GAP | |  Maximum gap curvature based criteria.  |
| CURV_NCIRCSEG | |  Minimum number of segments to define a circle curvature based criteria.  |
| SOURCES | |  Mesh sources.  |
| MIN_LEN_CONSTRAINT | |  Minimum edge length.  |
| MIN_LEN_CONSTRAINT_CURV_GAP | |  Maximum gap constrained by minimum length.  |
| MIN_LEN_CONSTRAINT_CURV_NCIRCSEG | |  Number of segments to define a circle constrained by minimum length.  |
| MIN_LEN_CONSTRAINT_SOURCES | |  Mesh sources constrained by minimum length (not applied).  |
| GROW_LIMIT_MAX_LEN_CONSTRAINT | |  Maximum growth limit from maximum edge length (not used, growth limited small to large).  |
| GROW_LIMIT_CURV_GAP | |  Maximum growth limit from maximum gap.  |
| GROW_LIMIT_CURV_NCIRCSEG | |  Maximum growth limit from number of segments to define a circle.  |
| GROW_LIMIT_SOURCES | |  Maximum growth limit from mesh sources.  |
| GROW_LIMIT_MIN_LEN_CONSTRAINT | |  Maximum growth limit from minimum length constraint.  |
| GROW_LIMIT_MIN_LEN_CONSTRAINT_CURV_GAP | |  Maximum growth limit from maximum gap constrained by minimum length.  |
| GROW_LIMIT_MIN_LEN_CONSTRAINT_CURV_NCIRCSEG | |  Maximum growth limit from number of segments to define a circle constrained by minimum length.  |
| GROW_LIMIT_MIN_LEN_CONSTRAINT_SOURCES | |  Maximum growth limit from sources constrained by minimum length.  |
| NUM_MESH_REASON | |  Number of reasons that can set the mesh local minimum edge length.  |
| MIN_LEN_INCREMENT | MIN_LEN_CONSTRAINT - MAX_LEN_CONSTRAINT|  Reason increment when adding minimum length constraint.  |
| GROW_LIMIT_INCREMENT | GROW_LIMIT_CURV_GAP - CURV_GAP|  Reason increment when adding growth limit constraint.  |
| MIN_GROW_LIMIT | GROW_LIMIT_CURV_GAP|  Reason marker for minimum reason to apply growth limit.  |




Enum that describes the criteria that set the local minimum edge length. 


### enum MESH_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TRI_MESH_TYPE | |  Triangle mesh  |
| QUAD_MESH_TYPE | |  Quadrilateral mesh  |
| NGON_MESH_TYPE | |  N-gon mesh  |
| NUM_MESH_TYPE | |  Number of mesh types  |




Enum for different mesh types. 


### enum MOTION_EXTENT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| EXTENT_FORWARD_INF | |  Forward beyond extent of model.  |
| EXTENT_REVERSE_INF | |  Reverse beyond extent of model.  |
| EXTENT_FORWARD_FINITE | |  Forward displacement.  |
| EXTENT_REVERSE_FINITE | |  Reverse displacement.  |
| EXTENT_SLIDER_FULL | |  Full range of slider motion.  |
| EXTENT_SLIDER_BEFORE | |  Slider motion from start to current position.  |
| EXTENT_SLIDER_AFTER | |  Slider motion from current position to end.  |
| MOTION_NUM_EXTENT_TYPES | |  Number of swept volume extent types.  |




Enum used to describe swept volume motion extent types. 


### enum OBJ_ID_LENGTH

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ID_LENGTH_PRESET_GROUP | 5|  ID for Var Preset Groups are length 5  |
| ID_LENGTH_PRESET_SETTING | 6|  ID for Var Preset Settings are length 6  |
| ID_LENGTH_ATTR | 8|  ID for Attributes are length 8  |
| ID_LENGTH_ATTRCOLL | 9|  ID for Attribute Collections are length 9  |
| ID_LENGTH_PARMCONTAINER | 10|  ID for Parm Containers are length 10  |
| ID_LENGTH_PARM | 11|  ID for Parms are length 11  |




Enum for ID length by vsp object type. 


### enum PARM_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| PARM_DOUBLE_TYPE | |  Double Parm type (Parm)  |
| PARM_INT_TYPE | |  Integer Parm type (IntParm)  |
| PARM_BOOL_TYPE | |  Bool Parm type (BoolParm)  |
| PARM_FRACTION_TYPE | |  Fraction Parm type (FractionParm)  |
| PARM_LIMITED_INT_TYPE | |  Limited integer Parm type (LimIntParm)  |
| PARM_NOTEQ_TYPE | |  Not equal Parm type (NotEqParm)  |
| PARM_POWER_INT_TYPE | |  Power integer Parm type (PowIntParm)  |




Enum for OpenVSP's various Parm class types. 


### enum PATCH_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| PATCH_NONE | |  No patch  |
| PATCH_POINT | |  Point patch type  |
| PATCH_LINE | |  Line patch type  |
| PATCH_COPY | |  Copy patch type  |
| PATCH_HALFWAY | |  Halfway patch type  |
| PATCH_NUM_TYPES | |  Number of patch types  |




Enum used to identify patch types for WireGeoms. 


### enum PCURV_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| LINEAR | |  Linear curve type  |
| PCHIP | |  Piecewise Cubic Hermite Interpolating Polynomial curve type  |
| CEDIT | |  Cubic Bezier curve type  |
| APPROX_CEDIT | |  Approximate curve as Cubic Bezier  |
| NUM_PCURV_TYPE | |  Number of curve types  |




Enum for parametric curve types. 


### enum PRES_UNITS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| PRES_UNIT_PSF | 0|  Pounds per square foot  |
| PRES_UNIT_PSI | |  Pounds per square inch  |
| PRES_UNIT_BA | |  Barye  |
| PRES_UNIT_PA | |  Pascal  |
| PRES_UNIT_KPA | |  Kilopascal  |
| PRES_UNIT_MPA | |  Megapascal  |
| PRES_UNIT_INCHHG | |  Inch of mercury  |
| PRES_UNIT_MMHG | |  Millimeter of mercury  |
| PRES_UNIT_MMH20 | |  Millimeter of water  |
| PRES_UNIT_MB | |  Millibar  |
| PRES_UNIT_ATM | |  Atmosphere  |
| NUM_PRES_UNIT | |  Number of pressure unit choices  |




Enum that describes units for pressure. 


### enum PROJ_BNDY_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NO_BOUNDARY | |  No boundary  |
| SET_BOUNDARY | |  Set boundary  |
| GEOM_BOUNDARY | |  Geom boundary  |
| NUM_PROJ_BNDY_OPTIONS | |  Number of projected area boundary options  |




Enum for Projected Area boundary option type. 


### enum PROJ_DIR_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| X_PROJ | |  Project in X axis direction  |
| Y_PROJ | |  Project in Y axis direction  |
| Z_PROJ | |  Project in Z axis direction  |
| GEOM_PROJ | |  Project toward a Geom  |
| VEC_PROJ | |  Project along a 3D vector  |
| NUM_PROJ_DIR_OPTIONS | |  Number of Projected Area direction types  |




Enum for Projected Area direction type. 


### enum PROJ_TGT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SET_TARGET | |  Set target type  |
| GEOM_TARGET | |  Geom target type  |
| MODE_TARGET | |  Mode target type  |
| Z_TARGET | |  Z plane target type  |
| XYZ_TARGET | |  XYZ point target type  |
| NUM_PROJ_TGT_OPTIONS | |  Number of Projected Area target types  |




Enum for Projected Area target type. 


### enum PROP_AZIMUTH_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| PROP_AZI_UNIFORM | |  Propeller blades are uniformly spaced  |
| PROP_AZI_FREE | |  Propeller blades are free to spaced arbitrarially  |
| PROP_AZI_BALANCED | |  Propeller blade balance is enforced  |
| NUM_PROP_AZI | |  Number of propeller blade azimuth modes  |




Enum used to specify the mode of a propeller blade azimuth control. 


### enum PROP_DRIVERS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| RPM_PROP_DRIVER | |  RPM driver  |
| CT_PROP_DRIVER | |  Thrust coefficient driver  |
| CP_PROP_DRIVER | |  Power coefficient driver  |
| T_PROP_DRIVER | |  Thrust driver  |
| ETA_PROP_DRIVER | |  Prop efficiency driver  |
| J_PROP_DRIVER | |  Advance ratio driver  |
| P_PROP_DRIVER | |  Power driver  |
| CQ_PROP_DRIVER | |  Torque coefficient driver  |
| Q_PROP_DRIVER | |  Torque driver  |
| NUM_PROP_DRIVER | |  Number of actuator disk drivers  |




Enum for actuator disk driver parameters. 


### enum PROP_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| PROP_BLADES | |  Propeller Geom is defined by individual propeller blades  |
| PROP_BOTH | |  Propeller Geom is defined by blades and a disk together  |
| PROP_DISK | |  Propeller Geom is defined by a flat circular disk  |




Enum used to specify the mode of a propeller Geom. 


### enum PROP_PCURVE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| PROP_CHORD | |  Chord parameterization  |
| PROP_TWIST | |  Twist parameterization  |
| PROP_RAKE | |  Rake parameterization  |
| PROP_SKEW | |  Skew parameterization  |
| PROP_SWEEP | |  Sweep parameterization  |
| PROP_THICK | |  Thickness parameterization  |
| PROP_CLI | |  Induced lift coefficient parameterization  |
| PROP_AXIAL | |  Axial parameterization  |
| PROP_TANGENTIAL | |  Tangential parameterization  |
| NUM_PROP_PCURVE | |  Number of propeller blade curve parameterization options  |




Enum for the various propeller blade curve parameterization options. 


### enum REORDER_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| REORDER_MOVE_UP | |  Move up one position  |
| REORDER_MOVE_DOWN | |  Move down one position  |
| REORDER_MOVE_TOP | |  Move to top  |
| REORDER_MOVE_BOTTOM | |  Move to bottom  |
| NUM_REORDER_TYPES | |  Number reordering instructions  |




Enum used to identify array reordering instructions. 


### enum REF_WING_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| MANUAL_REF | 0|  Manually specify the reference areas and lengths  |
| COMPONENT_REF | |  Use a particular wing to calculate the reference area and lengths  |
| NUM_REF_TYPES | |  Number of wing reference types  |




Enum used to indicate manual or component reference type. 


### enum RES_DATA_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| INVALID_TYPE | -1|  Invalid data type  |
| BOOL_DATA | 0|  Bool data type  |
| INT_DATA | 1|  Integer data type  |
| DOUBLE_DATA | 2|  Double data type  |
| STRING_DATA | 3|  String data type  |
| VEC3D_DATA | 4|  Vec3d data type  |
| INT_MATRIX_DATA | 5|  Int matrix data type  |
| DOUBLE_MATRIX_DATA | 6|  Double matrix data type  |
| ATTR_COLLECTION_DATA | 8|  Attribute collection data type  |
| PARM_REFERENCE_DATA | 9|  Parm reference data type  |




Enum representing the possible data types returned from the ResultsMgr. Datatypes are shared with Attribute Definitions 


### enum RES_GEOM_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| MESH_INDEXED_TRI | |  Indexed triangulated mesh Geom type  |
| MESH_SLICE_TRI | |  Sliced Triangulated mesh Geom type  |
| GEOM_XSECS | |  GeomXSec Geom type  |
| MESH_INDEX_AND_SLICE_TRI | |  Both indexed and sliced triangulated mesh Geom type  |




Enum representing the possible Geom types returned from the ResultsMgr. 


### enum RHO_UNITS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| RHO_UNIT_SLUG_FT3 | 0|  Slug per cubic foot  |
| RHO_UNIT_G_CM3 | |  Gram per cubic centimeter  |
| RHO_UNIT_KG_M3 | |  Kilogram per cubic meter  |
| RHO_UNIT_TONNE_MM3 | |  Tonne per cubic millimeter  |
| RHO_UNIT_LBM_FT3 | |  Pound-mass per cubic foot  |
| RHO_UNIT_LBFSEC2_IN4 | |  Pound-force-second squared per inch to the fourth  |
| RHO_UNIT_LBM_IN3 | |  Pound-mass per cubic inch  |
| NUM_RHO_UNIT | |  Number of density unit options  |




Enum that describes units for density. 


### enum ROUTE_PT_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ROUTE_PT_COMP | |  Routing point relative to parent body axes  |
| ROUTE_PT_UV | |  Routing point relative to parent surface coordinate frame  |
| ROUTE_PT_RST | |  Routing point relative to parent per-section volume coordinate frame  |
| ROUTE_PT_LMN | |  Routing point relative to parent uniform volume coordinate frame  |
| ROUTE_PT_EtaMN | |  Routing point relative to wing parent uniform eta volume coordinate frame  |
| ROUTE_PT_NUM_TYPES | |  Number of routing point coordinate types  |




Enum that identifies the coordinate type used for a routing point. 


### enum ROUTE_PT_DELTA_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ROUTE_PT_DELTA_XYZ | |  Routing point ofset in global axes  |
| ROUTE_PT_DELTA_COMP | |  Routing point offset in parent body frame  |
| ROUTE_PT_DELTA_UVN | |  Routing point offset in parent surface coordinate frame  |
| ROUTE_PT_DELTA_NUM_TYPES | |  Number of routing point offset coordinate types  |




Enum that identifies the coordinate offset type used for a routing point. 


### enum SCALE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SCALE_WIDTH | |  Scale image to match desired width  |
| SCALE_HEIGHT | |  Scale image to match desired height  |
| SCALE_WIDTH_HEIGHT | |  Scale image to match desired width and height  |
| SCALE_RESOLUTION | |  Scale image to specified resolution  |
| NUM_SCALE_TYPES | |  Number of ways to scale 3D background image.  |




Enum representing the possible ways to scale a 3D background image. 


### enum SET_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SET_NONE | -1|  None set  |
| SET_ALL | 0|  All set  |
| SET_SHOWN | 1|  Shown set  |
| SET_NOT_SHOWN | 2|  Not shown set  |
| SET_FIRST_USER | 3|  First user-defined set  |
| MIN_NUM_USER | 20|  Minimum number of user sets  |
| MAX_NUM_SETS | 1000|  Maximum possible number of sets  |




Enum for specifying named set types. 


### enum STEP_REPRESENTATION

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| STEP_SHELL | |  Manifold shell surface STEP file representation  |
| STEP_BREP | |  Manifold solid BREP STEP file representation  |




Enum that identifies the trimmed STEP export representation type. 


### enum SUBSURF_INCLUDE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SS_INC_TREAT_AS_PARENT | |  Treat the sub-surface the same as the parent  |
| SS_INC_SEPARATE_TREATMENT | |  Treat the sub-surface separately from the parent  |
| SS_INC_ZERO_DRAG | |  No drag contribution for the sub-surface  |




Enum used to identify Parasite Drag Tool sub-surface treatment. 


### enum SUBSURF_INOUT

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| INSIDE | |  The interior of the sub-surface is its surface  |
| OUTSIDE | |  The exterior of the sub-surface is its surface  |
| NONE | |  No part of the parent surface belongs to the sub-surface  |




Enum for indicating which part of the parent surface a sub-surfacce is dedfine. 


### enum SUBSURF_LINE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CONST_U | |  Constant U sub-surface  |
| CONST_W | |  Constant W sub-surface  |




Enum that identifies which surface coordinate is constant for a line sub-surface. 


### enum SUBSURF_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SS_LINE | |  Line sub-surface type  |
| SS_RECTANGLE | |  Rectangle sub-surface type  |
| SS_ELLIPSE | |  Ellipse sub-surface type  |
| SS_CONTROL | |  Control sub-surface type  |
| SS_LINE_ARRAY | |  Line array sub-surface type  |
| SS_FINITE_LINE | |  Finite line sub-surface type  |
| SS_XSEC_CURVE | |  XSecCurve based sub-surface type  |
| SS_INTERSECT | |  Intersection derived sub-surface type  |
| SS_NUM_TYPES | |  Number of sub-surface types  |




Enum for the various sub-surface types. 


### enum SYM_FLAG

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SYM_XY | ( 1 << 0 )|  XY planar symmetry.  |
| SYM_XZ | ( 1 << 1 )|  XZ planar symmetry.  |
| SYM_YZ | ( 1 << 2 )|  YZ planar symmetry.  |
| SYM_ROT_X | ( 1 << 3 )|  X rotational symmetry.  |
| SYM_ROT_Y | ( 1 << 4 )|  Y rotational symmetry.  |
| SYM_ROT_Z | ( 1 << 5 )|  Z rotational symmetry.  |
| SYM_PLANAR_TYPES | 3|  Number of planar symmetry types.  |
| SYM_NUM_TYPES | 6|  Number of symmetry types.  |




Enum that represents various symmetry types. 


### enum SYM_XSEC_TYP

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| SYM_NONE | |  No cross section symmetry.  |
| SYM_RL | |  Right/left cross section symmetry.  |
| SYM_TB | |  Top/bottom cross section symmetry.  |
| SYM_ALL | |  All cross section symmetry.  |




Enum that represents various cross section symmetry types. 


### enum TEMP_UNITS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TEMP_UNIT_K | 0|  Kelvin  |
| TEMP_UNIT_C | |  Celsius  |
| TEMP_UNIT_F | |  Fahrenheit  |
| TEMP_UNIT_R | |  Rankine  |
| NUM_TEMP_UNIT | |  Number of temperature unit choices  |




Enum that describes units for temperature. 


### enum TIRE_CLEARANCE_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TIRE_NOMINAL_CLEARANCE | |  Tire nominal shape  |
| TIRE_GROWTH_CLEARANCE | |  Tire growth (spinning) clearance  |
| TIRE_CLEARANCE | |  TRA clearance envelope  |
| NUM_TIRE_CLEARANCE_MODES | |  Number of tire clearance modes  |




Enum for tire clearance modes. 


### enum TIRE_CONTACT_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TIRE_STATIC_LODED_CONTACT | |  Tire static loaded radius  |
| TIRE_NOMINAL_CONTACT | |  Tire nominal radius  |
| TIRE_GROWTH_CONTACT | |  Tire growth (spinning) radius  |
| TIRE_FLAT_CONTACT | |  Tire flat tire radius  |
| NUM_TIRE_CONTACT_MODES | |  Number of tire radius modes  |




Enum for tire contact radius modes. 


### enum TIRE_DIM_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TIRE_DIM_IN | |  Tire dimensions in inches  |
| TIRE_DIM_MODEL | |  Tire dimensions in model units  |
| TIRE_DIM_FRAC | |  Tire dimensions as fractions  |
| NUM_TIRE_DIM_MODES | |  Number of tire dimension choices  |




Enum for tire dimension modes. 


### enum TIRE_MODES

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TIRE_TRA | |  Full TRA model  |
| TIRE_FAIR_FLANGE | |  TRA with faired flange / flank  |
| TIRE_FAIR_WHEEL | |  TRA with faired wheel  |
| TIRE_BALLOON | |  Balloon tire  |
| TIRE_BALLOON_WHEEL | |  Balloon tire with wheel  |
| TIRE_BALLOON_FAIR_WHEEL | |  Balloon tire with faired wheel  |
| NUM_TIRE_MODES | |  Number of tire choices  |




Enum for tire modes. 


### enum VEL_UNITS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| V_UNIT_FT_S | 0|  Feet per second  |
| V_UNIT_M_S | |  Meter per second  |
| V_UNIT_MPH | |  Mile per hour  |
| V_UNIT_KM_HR | |  Kilometer per hour  |
| V_UNIT_KEAS | |  Knots equivalent airspeed  |
| V_UNIT_KTAS | |  Knots true airspeed  |
| V_UNIT_MACH | |  Mach  |




Enum that describes units for velocity. 


### enum VIEW_NUM

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| VIEW_1 | |  One 2D view  |
| VIEW_2HOR | |  Two horizontal 2D views  |
| VIEW_2VER | |  Two vertical 2D views  |
| VIEW_4 | |  Four 2D views  |




Enum for 2D drawing types (DXF & SVG). 


### enum VIEW_ROT

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| ROT_0 | |  No rotation  |
| ROT_90 | |  90 degree rotation  |
| ROT_180 | |  180 degree rotation  |
| ROT_270 | |  270 degree rotation  |




Enum for describing 2D view rotations (DXF & SVG). 


### enum VIEW_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| VIEW_LEFT | |  Left 2D view type  |
| VIEW_RIGHT | |  Right 2D view type  |
| VIEW_TOP | |  Top 2D view type  |
| VIEW_BOTTOM | |  Bottom 2D view type  |
| VIEW_FRONT | |  Front 2D view type  |
| VIEW_REAR | |  Rear 2D view type  |
| VIEW_NONE | |  No 2D view type  |
| VIEW_NUM_TYPES | |  Number of 2D view types  |




Enum for describing 2D view types (DXF & SVG). 


### enum VSPAERO_NOISE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NOISE_FLYBY | |  Set up fly by noise analysis in VSPAERO for PSU-WOPWOP  |
| NOISE_FOOTPRINT | |  Set up footprint noise analysis in VSPAERO for PSU-WOPWOP  |
| NOISE_STEADY | |  Set up steady state noise analysis in VSPAERO for PSU-WOPWOP  |




Enums for VSPAERO unsteady noise calculation types. 


### enum VSPAERO_NOISE_UNIT

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NOISE_SI | |  Assume geometry and VSPAERO inputs in SI (m N kg s) for PSU-WOPWOP  |
| NOISE_ENGLISH | |  Assume geometry and VSPAERO inputs in english (ft lbf slug s) units, will convert to SI (m N kg s) for PSU-WOPWOP  |




Enums for VSPAERO unsteady noise units. 


### enum VSPAERO_PROP_MODE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| VSPAERO_PROP_STATIC | |  Model propellers as static, non-rotating blades &ndash; i.e. used as a wing.  |
| VSPAERO_PROP_UNSTEADY | |  Model propellers as unsteady rotating blades  |
| VSPAERO_PROP_PSEUDO_STEADY | |  Model propellers with pseudo steady model  |
| VSPAERO_PROP_NUM_MODES | |  Number of ways to model propeller blades in VSPAERO  |




Enum for the ways VSPAERO can treat propeller blades. 


### enum VSPAERO_STABILITY_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| STABILITY_OFF | |  No stability analysis (off)  |
| STABILITY_DEFAULT | |  Steady 6DOF stability analysis  |
| STABILITY_P_ANALYSIS | |  Unsteady roll stability analysis  |
| STABILITY_Q_ANALYSIS | |  Unsteady pitch stability analysis  |
| STABILITY_R_ANALYSIS | |  Unsteady yaw stability analysis  |
| STABILITY_PITCH | |  Simplified pitch stability analysis  |
| STABILITY_ADJOINT | |  Steady 6DOF stability analysis using adjoint  |
| STABILITY_NUM_TYPES | |  Number of stability analysis types  |




Enum for the types of VSPAERO stability analyses. 


### enum VSPAERO_STALL_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| STALL_OFF | |  Stall modeling off  |
| STALL_ON | |  Stall modeling on  |




Enum for the VSPAERO stall modeling options. 


### enum VSP_SURF_CFD_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CFD_NORMAL | |  Normal CFD Mesh surface  |
| CFD_NEGATIVE | |  Negative volume CFD Mesh surface  |
| CFD_TRANSPARENT | |  Transparent CFD Mesh surface  |
| CFD_STRUCTURE | |  FEA structure CFD Mesh surface  |
| CFD_STIFFENER | |  FEA stiffener CFD Mesh surface  |
| CFD_MEASURE_DUCT | |  Measure duct cross sectional area surface  |
| CFD_NUM_TYPES | |  Number of CFD Mesh surface types  |




Enum that is used to describe surfaces in CFD Mesh. 


### enum VSP_SURF_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| NORMAL_SURF | |  Normal VSP surface  |
| WING_SURF | |  Wing VSP surface  |
| DISK_SURF | |  Disk VSP surface  |
| NUM_SURF_TYPES | |  Number of VSP surface types  |




Enum for the different surface types in OpenVSP. 


### enum W_HINT

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| W_RIGHT_0 | |  Chevron start/ends at right (W = 0) of cross section  |
| W_BOTTOM | |  Chevron start/ends at bottom of cross section  |
| W_LEFT | |  Chevron start/ends at left of cross section  |
| W_TOP | |  Chevron start/ends at top of cross section  |
| W_RIGHT_1 | |  Chevron start/ends at right (W = 1) of cross section  |
| W_FREE | |  Chevron start/ends at user specified point on cross section  |




Enum for chevron W parameter start/end hints. 


### enum WING_BLEND

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| BLEND_FREE | |  Free blending  |
| BLEND_ANGLES | |  Blend based on angles (sweep & dihedral)  |
| BLEND_MATCH_IN_LE_TRAP | |  Match inboard leading edge trapezoid  |
| BLEND_MATCH_IN_TE_TRAP | |  Match inboard trailing edge trapezoid  |
| BLEND_MATCH_OUT_LE_TRAP | |  Match outboard leading edge trapezoid  |
| BLEND_MATCH_OUT_TE_TRAP | |  Match outboard trailing edge trapezoid  |
| BLEND_MATCH_IN_ANGLES | |  Match inboard angles  |
| BLEND_MATCH_LE_ANGLES | |  Match leading edge angles  |
| BLEND_NUM_TYPES | |  Number of blending types  |




Enum used to identify the type of wing blending between XSecs. 


### enum WING_DRIVERS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| AR_WSECT_DRIVER | |  Aspect ratio driver  |
| SPAN_WSECT_DRIVER | |  Span driver  |
| AREA_WSECT_DRIVER | |  Area driver  |
| TAPER_WSECT_DRIVER | |  Taper driver  |
| AVEC_WSECT_DRIVER | |  Average chord driver  |
| ROOTC_WSECT_DRIVER | |  Root chord driver  |
| TIPC_WSECT_DRIVER | |  Tip chord driver  |
| SECSWEEP_WSECT_DRIVER | |  Section sweep driver  |
| NUM_WSECT_DRIVER | |  Number of wing section drivers  |
| SWEEP_WSECT_DRIVER | SECSWEEP_WSECT_DRIVER + 1|   |
| SWEEPLOC_WSECT_DRIVER | SECSWEEP_WSECT_DRIVER + 2|   |
| SECSWEEPLOC_WSECT_DRIVER | SECSWEEP_WSECT_DRIVER + 3|   |




Enum for controlling wing section planform parameter control and linking. 


### enum XDDM_QUANTITY_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| XDDM_VAR | |  Variable XDDM type  |
| XDDM_CONST | |  Constant XDDM type  |




Enum that identifies the working XDDM type. 


### enum XSEC_CLOSE_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| CLOSE_NONE | |  No closure  |
| CLOSE_SKEWLOW | |  Skew lower closure  |
| CLOSE_SKEWUP | |  Skew upper closure  |
| CLOSE_SKEWBOTH | |  Skew both closure  |
| CLOSE_EXTRAP | |  Extrapolate closure  |
| CLOSE_NUM_TYPES | |  Number of XSec closure types  |




Enum for modifying XSec through closure types. 


### enum XSEC_CRV_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| XS_UNDEFINED | -1|   |
| XS_POINT | |  Point XSec  |
| XS_CIRCLE | |  Circle XSec  |
| XS_ELLIPSE | |  Ellipse XSec  |
| XS_SUPER_ELLIPSE | |  Super ellipse XSec  |
| XS_ROUNDED_RECTANGLE | |  Rounded rectangle XSec  |
| XS_GENERAL_FUSE | |  General fuselage XSec  |
| XS_FILE_FUSE | |  Fuselage file XSec  |
| XS_FOUR_SERIES | |  Four series XSec  |
| XS_SIX_SERIES | |  Six series XSec  |
| XS_BICONVEX | |  Biconvex XSec  |
| XS_WEDGE | |  Wedge XSec  |
| XS_EDIT_CURVE | |  Generic Edit Curve XSec  |
| XS_FILE_AIRFOIL | |  Airfoil file XSec  |
| XS_CST_AIRFOIL | |  CST airfoil XSec  |
| XS_VKT_AIRFOIL | |  VKT airfoil XSec  |
| XS_FOUR_DIGIT_MOD | |  Four digit modified XSec  |
| XS_FIVE_DIGIT | |  Five digit XSec  |
| XS_FIVE_DIGIT_MOD | |  Five digit modified XSec  |
| XS_ONE_SIX_SERIES | |  One six series XSec  |
| XS_AC25_773 | |  FAA AC 25.773 pilot view requirement  |
| XS_NUM_TYPES | |  Number of XSec types  |




Enum that identifies the various OpenVSP XSecCurve types. 


### enum XSEC_DRIVERS

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| WIDTH_XSEC_DRIVER | |  Width driver  |
| AREA_XSEC_DRIVER | |  Area driver  |
| HEIGHT_XSEC_DRIVER | |  Height driver  |
| HWRATIO_XSEC_DRIVER | |  Height/width ratio driver  |
| NUM_XSEC_DRIVER | |  Number of XSec drivers  |
| CIRCLE_NUM_XSEC_DRIVER | 2|   |




Enum for XSec drivers. 


### enum XSEC_FLAP_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| FLAP_NONE | |  No flap  |
| FLAP_PLAIN | |  Plain flap  |
| FLAP_NUM_TYPES | |  Number of flap types  |




Enum used to identify XSec flap type. 


### enum XSEC_SIDES_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| XSEC_BOTH_SIDES | |  Both sides  |
| XSEC_LEFT_SIDE | |  Left side  |
| XSEC_RIGHT_SIDE | |  Right side  |




Enum for XSec side types. 


### enum XSEC_TRIM_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| TRIM_NONE | |  No trimming  |
| TRIM_X | |  Trim XSec by X  |
| TRIM_THICK | |  Trim XSec by thickness  |
| TRIM_NUM_TYPES | |  Number of trimming types  |




Enum used to identify XSec trim type. 


### enum XSEC_TYPE

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| XSEC_FUSE | |  Fuselage XSec Geom  |
| XSEC_STACK | |  Stack XSec Geom  |
| XSEC_WING | |  Wing XSec Geom  |
| XSEC_CUSTOM | |  Custom XSec Geom  |
| XSEC_PROP | |  Propeller XSec Geom  |
| XSEC_NUM_TYPES | |  Number of XSec types  |




Enum for the various XSec types in OpenVSP. 


### enum XSEC_WIDTH_SHIFT

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| XS_SHIFT_LE | 0|  Shift leading edge  |
| XS_SHIFT_MID | 1|   |
| XS_SHIFT_TE | 2|   |




Enum for XSec width shift. 







-------------------------------

Updated on 2026-04-23 at 15:22:23 +0800