---
title: Background3D Functions
summary: This group of functions is used to work with 3D background images. Click here to return to the main page. 

---

# Background3D Functions

This group of functions is used to work with 3D background images. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| string | **[AddBackground3D](Modules/group___background3_d.md#function-addbackground3d)**() |
| int | **[GetNumBackground3Ds](Modules/group___background3_d.md#function-getnumbackground3ds)**() |
| vector< string > | **[GetAllBackground3Ds](Modules/group___background3_d.md#function-getallbackground3ds)**() |
| void | **[ShowAllBackground3Ds](Modules/group___background3_d.md#function-showallbackground3ds)**() |
| void | **[HideAllBackground3Ds](Modules/group___background3_d.md#function-hideallbackground3ds)**() |
| void | **[DelAllBackground3Ds](Modules/group___background3_d.md#function-delallbackground3ds)**() |
| void | **[DelBackground3D](Modules/group___background3_d.md#function-delbackground3d)**(const string & id) |
| vector< string > | **[GetAllBackground3DRelativePaths](Modules/group___background3_d.md#function-getallbackground3drelativepaths)**() |
| vector< string > | **[GetAllBackground3DAbsolutePaths](Modules/group___background3_d.md#function-getallbackground3dabsolutepaths)**() |
| string | **[GetBackground3DRelativePath](Modules/group___background3_d.md#function-getbackground3drelativepath)**(const string & id) |
| string | **[GetBackground3DAbsolutePath](Modules/group___background3_d.md#function-getbackground3dabsolutepath)**(const string & id) |
| void | **[SetBackground3DRelativePath](Modules/group___background3_d.md#function-setbackground3drelativepath)**(const string & id, const string & fname) |
| void | **[SetBackground3DAbsolutePath](Modules/group___background3_d.md#function-setbackground3dabsolutepath)**(const string & id, const string & fname) |


## Functions Documentation

### function AddBackground3D

```
string AddBackground3D()
```


**Return**: string ID for added Background3D 

Add a Background3D to model 

int nbg = GetNumBackground3Ds();

// Add Background3D
string bg_id = AddBackground3D();

if ( GetNumBackground3Ds() != nbg + 1 )
{
    Print( "ERROR: AddBackground3D" );
}

DelBackground3D( bg_id );
```

 \endforcpponly \beginPythonOnly ```py

nbg = GetNumBackground3Ds()

# Add Background3D
bg_id = AddBackground3D()

if GetNumBackground3Ds() != nbg + 1 :
    print( "ERROR: AddBackground3D" )

DelBackground3D( bg_id )
```

  


### function GetNumBackground3Ds

```
int GetNumBackground3Ds()
```


**Return**: int Number of Background3D's in model 

Get Number of Background3D's in a model 

int nbg = GetNumBackground3Ds();

// Add Background3D
string bg_id = AddBackground3D();

if ( GetNumBackground3Ds() != nbg + 1 )
{
    Print( "ERROR: AddBackground3D" );
}

DelBackground3D( bg_id );
```

 \endforcpponly \beginPythonOnly ```py

nbg = GetNumBackground3Ds()

# Add Background3D
bg_id = AddBackground3D()

if GetNumBackground3Ds() != nbg + 1 :
    print( "ERROR: AddBackground3D" )

DelBackground3D( bg_id )
```

  


### function GetAllBackground3Ds

```
vector< string > GetAllBackground3Ds()
```


**Return**: vector<string> Vector of Background3D IDs 

Get id's of all Background3Ds in model 

int nbg = GetNumBackground3Ds();

// Add Background3D
AddBackground3D();
AddBackground3D();
AddBackground3D();

if ( GetNumBackground3Ds() != nbg + 3 )
{
    Print( "ERROR: AddBackground3D" );
}

array< string > @bg_array = GetAllBackground3Ds();

for( int n = 0; n < int( bg_array.length() ); n++ )
{
    Print( bg_array[n] );
}

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

nbg = GetNumBackground3Ds()

# Add Background3D
AddBackground3D()
AddBackground3D()
AddBackground3D()

if GetNumBackground3Ds() != nbg + 3 :
    print( "ERROR: AddBackground3D" )

bg_array = GetAllBackground3Ds()

for n in range( len( bg_array ) ):
    print( bg_array[n] )

DelAllBackground3Ds()
```

  


### function ShowAllBackground3Ds

```
void ShowAllBackground3Ds()
```


Show all Background3Ds in model 

// Add Background3D
AddBackground3D();
AddBackground3D();
AddBackground3D();

ShowAllBackground3Ds();

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
AddBackground3D()
AddBackground3D()
AddBackground3D()

ShowAllBackground3Ds()

DelAllBackground3Ds()
```

  


### function HideAllBackground3Ds

```
void HideAllBackground3Ds()
```


Hide all Background3Ds in model 

// Add Background3D
AddBackground3D();
AddBackground3D();
AddBackground3D();

HideAllBackground3Ds();

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
AddBackground3D()
AddBackground3D()
AddBackground3D()

HideAllBackground3Ds()

DelAllBackground3Ds()
```

  


### function DelAllBackground3Ds

```
void DelAllBackground3Ds()
```


Delete all Background3Ds in model 

// Add Background3D
AddBackground3D();
AddBackground3D();
AddBackground3D();

DelAllBackground3Ds();

int nbg = GetNumBackground3Ds();

if ( nbg != 0 )
{
    Print( "ERROR: DelAllBackground3Ds" );
}
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
AddBackground3D()
AddBackground3D()
AddBackground3D()

DelAllBackground3Ds()

nbg = GetNumBackground3Ds()

if nbg != 0 :
    print( "ERROR: DelAllBackground3Ds" )
```

  


### function DelBackground3D

```
void DelBackground3D(
    const string & id
)
```


**Parameters**: 

  * **id** string Background3D ID to delete 


Delete specific Background3D frommodel 

// Add Background3D
AddBackground3D();
string bg_id = AddBackground3D();
AddBackground3D();

int nbg = GetNumBackground3Ds();

DelBackground3D( bg_id );

if ( GetNumBackground3Ds() != nbg - 1 )
{
    Print( "ERROR: DelBackground3D" );
}
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
AddBackground3D()
bg_id = AddBackground3D()
AddBackground3D()

nbg = GetNumBackground3Ds()

DelBackground3D( bg_id )

if GetNumBackground3Ds() != nbg -1 :
    print( "ERROR: DelBackground3D" )
```

  


### function GetAllBackground3DRelativePaths

```
vector< string > GetAllBackground3DRelativePaths()
```


**Return**: vector<string> Vector of relative paths to Background3D image files 

Get relative paths to all Background3D images in model. Note that path is relative to the model's *.vsp3 file. Consequently, if a file has not yet been saved or assigned a file name, the relative path is meaningless. 

// Add Background3D
AddBackground3D();
AddBackground3D();
AddBackground3D();

array< string > @bg_file_array = GetAllBackground3DRelativePaths();

for( int n = 0; n < int( bg_file_array.length() ); n++ )
{
    Print( bg_file_array[n] );
}

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
AddBackground3D()
AddBackground3D()
AddBackground3D()

bg_file_array = GetAllBackground3DRelativePaths()

for n in range( len( bg_file_array ) ):
    print( bg_file_array[n] )

DelAllBackground3Ds()
```

  


### function GetAllBackground3DAbsolutePaths

```
vector< string > GetAllBackground3DAbsolutePaths()
```


**Return**: vector<string> Vector of absolute paths to Background3D image files 

Get absolute paths to all Background3D images in model. 

// Add Background3D
AddBackground3D();
AddBackground3D();
AddBackground3D();

array< string > @bg_file_array = GetAllBackground3DAbsolutePaths();

for( int n = 0; n < int( bg_file_array.length() ); n++ )
{
    Print( bg_file_array[n] );
}

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
AddBackground3D()
AddBackground3D()
AddBackground3D()

bg_file_array = GetAllBackground3DAbsolutePaths()

for n in range( len( bg_file_array ) ):
    print( bg_file_array[n] )

DelAllBackground3Ds()
```

  


### function GetBackground3DRelativePath

```
string GetBackground3DRelativePath(
    const string & id
)
```


**Parameters**: 

  * **id** string Background3D ID 


**Return**: string Relative path to Background3D image file 

Get relative path to specified Background3D's image. Note that path is relative to the model's *.vsp3 file. Consequently, if a file has not yet been saved or assigned a file name, the relative path is meaningless. 

// Add Background3D
string bg_id = AddBackground3D();

SetBackground3DRelativePath( bg_id, "front.png" );
string bg_file = GetBackground3DRelativePath( bg_id );

Print( bg_file );

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
bg_id = AddBackground3D()

SetBackground3DRelativePath( bg_id, "front.png" )
bg_file = GetBackground3DRelativePath( bg_id )

print( bg_file )

DelAllBackground3Ds()
```

  


### function GetBackground3DAbsolutePath

```
string GetBackground3DAbsolutePath(
    const string & id
)
```


**Parameters**: 

  * **id** string Background3D ID 


**Return**: string Absolute path to Background3D image file 

Get absolute path to specified Background3D's image. 

// Add Background3D
string bg_id = AddBackground3D();

SetBackground3DAbsolutePath( bg_id, "/user/me/vsp_work/front.png" );
string bg_file = GetBackground3DAbsolutePath( bg_id );

Print( bg_file );

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
bg_id = AddBackground3D()

SetBackground3DAbsolutePath( bg_id, "/user/me/vsp_work/front.png" )
bg_file = GetBackground3DAbsolutePath( bg_id )

print( bg_file )

DelAllBackground3Ds()
```

  


### function SetBackground3DRelativePath

```
void SetBackground3DRelativePath(
    const string & id,
    const string & fname
)
```


**Parameters**: 

  * **id** string Background3D ID 
  * **fname** string Relative path to Background3D image file 


Set relative path to specified Background3D's image. Note that path is relative to the model's *.vsp3 file. Consequently, if a file has not yet been saved or assigned a file name, the relative path is meaningless. 

// Add Background3D
string bg_id = AddBackground3D();

SetBackground3DRelativePath( bg_id, "front.png" );
string bg_file = GetBackground3DRelativePath( bg_id );

Print( bg_file );

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
bg_id = AddBackground3D()

SetBackground3DRelativePath( bg_id, "front.png" )
bg_file = GetBackground3DRelativePath( bg_id )

print( bg_file )

DelAllBackground3Ds()
```

  


### function SetBackground3DAbsolutePath

```
void SetBackground3DAbsolutePath(
    const string & id,
    const string & fname
)
```


**Parameters**: 

  * **id** string Background3D ID 
  * **fname** string Absolute path to Background3D image file 


Set absolute path to specified Background3D's image. 

// Add Background3D
string bg_id = AddBackground3D();

SetBackground3DAbsolutePath( bg_id, "front.png" );
string bg_file = GetBackground3DAbsolutePath( bg_id );

Print( bg_file );

DelAllBackground3Ds();
```

 \endforcpponly \beginPythonOnly ```py

# Add Background3D
bg_id = AddBackground3D()

SetBackground3DAbsolutePath( bg_id, "front.png" )
bg_file = GetBackground3DAbsolutePath( bg_id )

print( bg_file )

DelAllBackground3Ds()
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800