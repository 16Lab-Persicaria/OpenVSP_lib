---
title: Advanced Link Functions
summary: The following functions are available for the Advanced Link tool. Click here to return to the main page. 

---

# Advanced Link Functions

The following functions are available for the Advanced Link tool. Click here to return to the main page. 

## Functions

|                | Name           |
| -------------- | -------------- |
| std::vector< std::string > | **[GetAdvLinkNames](Modules/group___advanced_link.md#function-getadvlinknames)**() |
| int | **[GetLinkIndex](Modules/group___advanced_link.md#function-getlinkindex)**(const string & name) |
| void | **[DelAdvLink](Modules/group___advanced_link.md#function-deladvlink)**(int index) |
| void | **[DelAllAdvLinks](Modules/group___advanced_link.md#function-delalladvlinks)**() |
| void | **[AddAdvLink](Modules/group___advanced_link.md#function-addadvlink)**(const string & name) |
| void | **[AddAdvLinkInput](Modules/group___advanced_link.md#function-addadvlinkinput)**(int index, const string & parm_id, const string & var_name) |
| void | **[AddAdvLinkOutput](Modules/group___advanced_link.md#function-addadvlinkoutput)**(int index, const string & parm_id, const string & var_name) |
| void | **[DelAdvLinkInput](Modules/group___advanced_link.md#function-deladvlinkinput)**(int index, const string & var_name) |
| void | **[DelAdvLinkOutput](Modules/group___advanced_link.md#function-deladvlinkoutput)**(int index, const string & var_name) |
| std::vector< std::string > | **[GetAdvLinkInputNames](Modules/group___advanced_link.md#function-getadvlinkinputnames)**(int index) |
| std::vector< std::string > | **[GetAdvLinkInputParms](Modules/group___advanced_link.md#function-getadvlinkinputparms)**(int index) |
| std::vector< std::string > | **[GetAdvLinkOutputNames](Modules/group___advanced_link.md#function-getadvlinkoutputnames)**(int index) |
| std::vector< std::string > | **[GetAdvLinkOutputParms](Modules/group___advanced_link.md#function-getadvlinkoutputparms)**(int index) |
| bool | **[ValidateAdvLinkParms](Modules/group___advanced_link.md#function-validateadvlinkparms)**(int index) |
| void | **[SetAdvLinkCode](Modules/group___advanced_link.md#function-setadvlinkcode)**(int index, const string & code) |
| std::string | **[GetAdvLinkCode](Modules/group___advanced_link.md#function-getadvlinkcode)**(int index) |
| void | **[SearchReplaceAdvLinkCode](Modules/group___advanced_link.md#function-searchreplaceadvlinkcode)**(int index, const string & from, const string & to) |
| bool | **[BuildAdvLinkScript](Modules/group___advanced_link.md#function-buildadvlinkscript)**(int index) |


## Functions Documentation

### function GetAdvLinkNames

```
std::vector< std::string > GetAdvLinkNames()
```


**Return**: Array of advanced link names 

Get an array of all advanced link names 

array< string > @link_array = GetAdvLinkNames();

for( int n = 0 ; n < int( link_array.length() ) ; n++ )
{
    Print( link_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

link_array = GetAdvLinkNames()

for n in range(len(link_array) ):

    print( link_array[n] )
```

  


### function GetLinkIndex

```
int GetLinkIndex(
    const string & name
)
```


**Parameters**: 

  * **name** string Name for advanced link 


**Return**: index for advanced link 

Find the index of a specific advanced link. 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )
```

  


### function DelAdvLink

```
void DelAdvLink(
    int index
)
```


**Parameters**: 

  * **index** Index for advanced link 


Delete an advanced link specified by index 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

DelAdvLink( indx );

array< string > @link_array = GetAdvLinkNames();

// Should print nothing.
for( int n = 0 ; n < int( link_array.length() ) ; n++ )
{
    Print( link_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

DelAdvLink( indx )

link_array = GetAdvLinkNames()

# Should print nothing.
for n in range(len(link_array) ):

    print( link_array[n] )
```

  


### function DelAllAdvLinks

```
void DelAllAdvLinks()
```


Delete all advanced links 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

DelAllAdvLinks();

array< string > @link_array = GetAdvLinkNames();

// Should print nothing.
for( int n = 0 ; n < int( link_array.length() ) ; n++ )
{
    Print( link_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

DelAllAdvLinks()

link_array = GetAdvLinkNames()

# Should print nothing.
for n in range( len(link_array) ):

    print( link_array[n] )
```

  


### function AddAdvLink

```
void AddAdvLink(
    const string & name
)
```


**Parameters**: 

  * **name** string Name for advanced link 


Add an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )
```

  


### function AddAdvLinkInput

```
void AddAdvLinkInput(
    int index,
    const string & parm_id,
    const string & var_name
)
```


**Parameters**: 

  * **index** int Advanced link index 
  * **parm_id** string Parameter ID for advanced link input variable 
  * **var_name** string Name for advanced link input variable 


Add an input variable to an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )
```

  


### function AddAdvLinkOutput

```
void AddAdvLinkOutput(
    int index,
    const string & parm_id,
    const string & var_name
)
```


**Parameters**: 

  * **index** int Advanced link index 
  * **parm_id** string Parameter ID for advanced link output variable 
  * **var_name** string Name for advanced link output variable 


Add an output variable to an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )
```

  


### function DelAdvLinkInput

```
void DelAdvLinkInput(
    int index,
    const string & var_name
)
```


**Parameters**: 

  * **index** int Advanced link index 
  * **var_name** string Name for advanced link input variable to delete 


Delete an input variable from an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );
string y_pos = GetParm( pod, "Y_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );
AddAdvLinkInput( indx, y_pos, "y" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

DelAdvLinkInput( indx, "y" );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )
y_pos = GetParm( pod, "Y_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )
AddAdvLinkInput( indx, y_pos, "y" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

DelAdvLinkInput( indx, "y" )

BuildAdvLinkScript( indx )
```

  


### function DelAdvLinkOutput

```
void DelAdvLinkOutput(
    int index,
    const string & var_name
)
```


**Parameters**: 

  * **index** int Advanced link index 
  * **var_name** string Name for advanced link output variable to delete 


Delete an output variable from an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );
string y_pos = GetParm( pod, "Y_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );
AddAdvLinkOutput( indx, y_pos, "y" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

DelAdvLinkOutput( indx, "y" );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )
y_pos = GetParm( pod, "Y_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )
AddAdvLinkOutput( indx, y_pos, "y" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

DelAdvLinkOutput( indx, "y" )

BuildAdvLinkScript( indx )
```

  


### function GetAdvLinkInputNames

```
std::vector< std::string > GetAdvLinkInputNames(
    int index
)
```


**Parameters**: 

  * **index** int Advanced link index 


**Return**: Array of advanced link input names 

Get the name of all the inputs to a specified advanced link index 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

array< string > @name_array = GetAdvLinkInputNames( indx );

for( int n = 0 ; n < int( name_array.length() ) ; n++ )
{
    Print( name_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

name_array = GetAdvLinkInputNames( indx )

for n in range(len(name_array) ):

    print( name_array[n] )
```

  


### function GetAdvLinkInputParms

```
std::vector< std::string > GetAdvLinkInputParms(
    int index
)
```


**Parameters**: 

  * **index** int Advanced link index 


**Return**: Array of advanced link input Parm IDs 

Get the Parm IDs of all the inputs to a specified advanced link index 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

array< string > @parm_array = GetAdvLinkInputParms( indx );

for( int n = 0 ; n < int( parm_array.length() ) ; n++ )
{
    Print( parm_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

parm_array = GetAdvLinkInputParms( indx )

for n in range( len(parm_array) ):

    print( parm_array[n] )
```

  


### function GetAdvLinkOutputNames

```
std::vector< std::string > GetAdvLinkOutputNames(
    int index
)
```


**Parameters**: 

  * **index** int Advanced link index 


**Return**: Array of advanced link output names 

Get the Parm IDs of all the outputs to a specified advanced link index 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

array< string > @name_array = GetAdvLinkOutputNames( indx );

for( int n = 0 ; n < int( name_array.length() ) ; n++ )
{
    Print( name_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

name_array = GetAdvLinkOutputNames( indx )

for n in range( len(name_array) ):

    print( name_array[n] )
```

  


### function GetAdvLinkOutputParms

```
std::vector< std::string > GetAdvLinkOutputParms(
    int index
)
```


**Parameters**: 

  * **index** int Advanced link index 


**Return**: Array of advanced link output Parm IDs 

Get the Parm IDs of all the outputs to a specified advanced link index 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

array< string > @parm_array = GetAdvLinkOutputParms( indx );

for( int n = 0 ; n < int( parm_array.length() ) ; n++ )
{
    Print( parm_array[n] );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

parm_array = GetAdvLinkOutputParms( indx )

for n in range( len(parm_array) ):

    print( parm_array[n] )
```

  


### function ValidateAdvLinkParms

```
bool ValidateAdvLinkParms(
    int index
)
```


**Parameters**: 

  * **index** int Index for advanced link 


**Return**: Flag indicating whether parms are valid 

Validate the input and output parameters for an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

bool valid = ValidateAdvLinkParms( indx );

if ( valid )
{
    Print( "Advanced link Parms are valid." );
}
else
{
    Print( "Advanced link Parms are not valid." );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

valid = ValidateAdvLinkParms( indx )

if  valid :
    print( "Advanced link Parms are valid." )
else:
    print( "Advanced link Parms are not valid." )
```

  


### function SetAdvLinkCode

```
void SetAdvLinkCode(
    int index,
    const string & code
)
```


**Parameters**: 

  * **index** int Index for advanced link 
  * **code** string Code for advanced link 


Get the code from an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )
```

  


### function GetAdvLinkCode

```
std::string GetAdvLinkCode(
    int index
)
```


**Parameters**: 

  * **index** int Index for advanced link 


**Return**: String containing advanced link code 

Get the code from an advanced link 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

BuildAdvLinkScript( indx );

string code = GetAdvLinkCode( indx );

Print( code );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

BuildAdvLinkScript( indx )

code = GetAdvLinkCode( indx )

print( code )
```

  


### function SearchReplaceAdvLinkCode

```
void SearchReplaceAdvLinkCode(
    int index,
    const string & from,
    const string & to
)
```


**Parameters**: 

  * **index** int Index for advanced link 
  * **from** string Search token 
  * **to** string Replace token 


Search and replace strings in the advanced link code 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );
SearchReplaceAdvLinkCode( indx, "10.0", "12.3" );

string code = GetAdvLinkCode( indx );

Print( code );

BuildAdvLinkScript( indx );
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )
SearchReplaceAdvLinkCode( indx, "10.0", "12.3" )

code = GetAdvLinkCode( indx )

print( code )

BuildAdvLinkScript( indx )
```

  


### function BuildAdvLinkScript

```
bool BuildAdvLinkScript(
    int index
)
```


**Parameters**: 

  * **index** int Index for advanced link 


**Return**: Flag indicating whether advanced link build was successful 

Build (ready for execution and perform syntax check) an advanced link. 

string pod = AddGeom( "POD", "" );
string length = FindParm( pod, "Length", "Design" );
string x_pos = GetParm( pod, "X_Rel_Location", "XForm" );

AddAdvLink( "ExampleLink" );
int indx = GetLinkIndex( "ExampleLink" );
AddAdvLinkInput( indx, length, "len" );
AddAdvLinkOutput( indx, x_pos, "x" );

SetAdvLinkCode( indx, "x = 10.0 - len;" );

bool success = BuildAdvLinkScript( indx );

if ( success )
{
    Print( "Advanced link build successful." );
}
else
{
    Print( "Advanced link build not successful." );
}
```

 \endforcpponly \beginPythonOnly ```py

pod = AddGeom( "POD", "" )
length = FindParm( pod, "Length", "Design" )
x_pos = GetParm( pod, "X_Rel_Location", "XForm" )

AddAdvLink( "ExampleLink" )
indx = GetLinkIndex( "ExampleLink" )
AddAdvLinkInput( indx, length, "len" )
AddAdvLinkOutput( indx, x_pos, "x" )

SetAdvLinkCode( indx, "x = 10.0 - len;" )

success = BuildAdvLinkScript( indx )

if  success :
    print( "Advanced link build successful." )
else:
    print( "Advanced link build not successful." )
```

  






-------------------------------

Updated on 2026-04-23 at 11:25:06 +0800