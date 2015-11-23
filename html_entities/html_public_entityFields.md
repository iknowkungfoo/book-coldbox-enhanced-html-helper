
# entityFields Create fields based on entity properties 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| entity | any | true | [Not Defined] | The entity binded to this control 
| groupWrapper | string | false |  | The wrapper tag to use around the tag and label. Empty by default 
| fieldwrapper | any | false |  | The wrapper tag to use around the field items. Empty by default 
| labelwrapper | any | false |  | The wrapper tag to use around the label items. Empty by default 
| labelClass | string | false |  | The class to be applied to the label 
| textareas | any | false |  | A list of property names that you want as textareas 
| booleanSelect | boolean | false | true | If a boolean is detected a dropdown is generated, if false, then radio buttons 
| showRelations | boolean | false | true | If true it will show relation tables for one to one and one to many 
| manytoone | struct | false | StructNew() | A structure of data to help with many to one relationships on how they are presented. Possible key values for each key are [valuecolumn='',namecolumn='',criteria={},sortorder=string]. Example: {criteria={productid=1},sortorder='Department desc'} 
| manytomany | struct | false | StructNew() | A structure of data to help with many to one relationships on how they are presented. Possible key values for each key are [valuecolumn='',namecolumn='',criteria={},sortorder=string,selectColumn='']. Example: {criteria={productid=1},sortorder='Department desc'} 
