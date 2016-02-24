
# button Render out a button. Remember that any extra arguments are passed as tag attributes 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| name | string | false |  | The name of the field |
| value | string | false |  | The value of the field |
| disabled | boolean | false | false | Disabled button or not? |
| type | string | false | button | The type of button to create: button, reset or submit |
| wrapper | string | false |  | The wrapper tag to use around the tag. Empty by default |
| groupWrapper | string | false |  | The wrapper tag to use around the tag and label. Empty by default |
| label | string | false |  | If Passed we will prepend a label tag |
| labelwrapper | string | false |  | The wrapper tag to use around the label. Empty by default |
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control |
| labelClass | string | false |  | The class to be applied to the label |


