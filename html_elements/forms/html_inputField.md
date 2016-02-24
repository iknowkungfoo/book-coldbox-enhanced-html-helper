# inputField 

Create an input field using some cool tags and features.	Any extra arguments are passed to the tag 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| type | string | false | text | The type of input field to create |
| name | string | false |  | The name of the field |
| value | string | false |  | The value of the field |
| disabled | boolean | false | false | Disabled |
| checked | boolean | false | false | Checked |
| readonly | boolean | false | false | Readonly |
| wrapper | string | false |  | The wrapper tag to use around the tag. Empty by default |
| groupWrapper | string | false |  | The wrapper tag to use around the tag and label. Empty by default |
| label | string | false |  | If Passed we will prepend a label tag |
| labelwrapper | string | false |  | The wrapper tag to use around the label. Empty by default |
| labelClass | string | false |  | The class to be applied to the label |
| bind | any | false |  | The entity binded to this control |
| bindProperty | any | false |  | The property to use for the value, by convention we use the name attribute |
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control |
