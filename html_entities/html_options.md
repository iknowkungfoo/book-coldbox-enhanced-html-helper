
# options Render out options. Remember that any extra arguments are passed as tag attributes. Updated from CB 4.0. 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| values | any | false | [Not Defined] | The values array, list, or query to build options for |


| column | any | false |  | If using a query or array of objects the column to display as value and name |


| nameColumn | any | false |  | If using a query or array of objects, the name column to display, if not passed defaults to the value column |


| selectedIndex | any | false | 0 | selected index(s) if any. So either one or a list of indexes |


| selectedValue | any | false |  | selected value(s) if any. So either one or a list of values |


| excludedValues | string | false |  | A CSV list of option values to exclude from the 'values' source (column). |


| emptyOption | boolean | false | false | Add an empty (no value) option before the others. If there is only one value, this will be skipped. |


| emptyOptionLabel | string | false | Select One | Label text for the empty option. |


| emptyOptionLabelNoData | string | false | { No options found. } | Label text for the empty option. |


