
# label Render a label tag. Remember that any extra arguments are passed as tag attributes 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| field | string | true | [Not Defined] | The for who attribute 
| content | string | false |  | The label content. If not passed the field is used 
| wrapper | string | false |  | The wrapper tag to use around the tag. Empty by default 
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control 
| class | string | false |  | The class to be applied to the label 
