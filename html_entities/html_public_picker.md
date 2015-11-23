
# picker Render out two related select tags, where options can be moved from one to the other. 

1. **Access**: public
2. **Location**: HTMLHelper Extended 
3. Custom Function


| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| name | string | true | [Not Defined] | The (unique) name of the picker. 
| leftHand | struct | false | [Not Defined] | Configuration for left-hand Select (See function 'select'). 
| rightHand | struct | false | StructNew() | Configuration for right-hand Select (See function 'select'). 
| label | string | false | [Not Defined] | Label for the picker. 
| labelWrapper | string | false | h3 | Tag to wrap about the label. 
| size | numeric | false | 10 | The number of rows in the <select>s that should be visible. 
| showHelp | boolean | false | true | Show the instructions under the picker. 
