
# emailField Render out an email field. Remember that any extra arguments are passed as tag attributes 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| name | string | false |  | The name of the field 
| value | string | false |  | The value of the field 
| disabled | boolean | false | false | Disabled 
| readonly | boolean | false | false | Readonly 
| wrapper | string | false |  | The wrapper tag to use around the tag. Empty by default 
| groupWrapper | string | false |  | The wrapper tag to use around the tag and label. Empty by default 
| label | string | false |  | If Passed we will prepend a label tag 
| labelwrapper | string | false |  | The wrapper tag to use around the label. Empty by default 
| labelClass | string | false |  | The class to be applied to the label 
| bind | any | false |  | The entity binded to this control 
| bindProperty | any | false |  | The property to use for the value, by convention we use the name attribute 
