
# selectState Render out a select tag populated with US state options. Uses the same arguments as the basic <select> function. 

1. **Access**: public
2. **Location**: HTMLHelper Extended 
3. Custom Function


| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| name | string | false |  | The name of the field 
| verbose | boolean | false | true | Show the long name of a state (default) or the two character abbreviation. 
| allOption | boolean | false | false | Add an empty (no value) option before the others. If there is only one value, this will be skipped. 
| selectedValue | string | false |  | selected value if any 
| excludedValues | string | false |  | A CSV list of option values to exclude from the 'values' column. 
