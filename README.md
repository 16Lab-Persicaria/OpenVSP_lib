## OpenVSP Lib

Original repo: https://github.com/OpenVSP/OpenVSP

Rebuild OpenVSP 3.49.0 for using as an external cpp lib

### Build variables:
- VSP_NO_GRAPHICS
- VSP_NO_VSPAERO
- VSP_NO_API_WRAPPERS
- VSP_NO_HELP
- VSP_NO_DOC
- VSP_NO_PYDOC

### Dependencies:
Denpendencies categories 1&2 are included in this repo.
```
    # ---1. OpenVSP core lib ---
    'geom_api',
    'geom_core',
    'cfd_mesh',
    'xmlvsp',
    'robust',
    'sixseries',
    'util',
    'util_api',
    'tritri',
    'wavedragEL',
    'stb_image',

    # ---2. External lib ---
    'angelscript',
    'cpptest',
    'libxml2',
    'cminpack_s',
    'libexpress',
    'libexppp',
    'libsdai_ap203',
    'libstepeditor',
    'libstepcore',
    'libstepdai',
    'libsteputils',
    'libbase',
    'iges_static',
    'triangle-api',
    'triangle',
    'delabella',
    'pinocchio',
    'Clipper2',

    # ---3. System lib ---
    'shlwapi',
    'wsock32',
    'ws2_32',
    'kernel32',
    'user32',
    'gdi32',
    'winspool',
    'shell32',
    'ole32',
    'oleaut32',
    'uuid',
    'comdlg32',
    'advapi32',
```

### License

NOSA 1.3