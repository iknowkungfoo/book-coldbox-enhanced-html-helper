# &lt;select&gt;

Render out a `<select>` tag.

1. **Access**: public
2. **Location**: HTMLHelper Extended

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| name | string | false |  | The name of the field |
| options | any | false |  | The value for the options, usually by calling our options() method |
| column | string | false |  | If using a query or array of objects the column to display as value and name |
| nameColumn | string | false |  | If using a query or array of objects, the name column to display, if not passed defaults to the value column |
| selectedIndex | numeric | false | 0 | selected index |
| selectedValue | string | false |  | selected value if any |
| excludedValues | string | false |  | A CSV list of option values to exclude from the 'values' column. |
| bind | any | false |  | The entity binded to this control |
| bindProperty | any | false |  | The property to use for the value, by convention we use the name attribute |
| disabled | boolean | false | false | Disabled button or not? |
| multiple | boolean | false | false | multiple button or not? |
| wrapper | string | false |  | The wrapper tag to use around the tag. Empty by default |
| groupWrapper | string | false |  | The wrapper tag to use around the tag and label. Empty by default |
| label | string | false |  | If Passed we will prepend a label tag |
| labelwrapper | string | false |  | The wrapper tag to use around the label. Empty by default |
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control |
| labelClass | string | false |  | The class to be applied to the label |
| size | numeric | false | 5 | If multiple = true, how many rows to display. |

