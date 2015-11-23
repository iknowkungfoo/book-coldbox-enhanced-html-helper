
# link Create link tags, using the SES base URL or not 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| href | any | true | [Not Defined] | The href link to link to 
| rel | any | false | stylesheet | The rel attribute 
| type | any | false | text/css | The type attribute 
| title | any | false |  | The title attribute 
| media | any | false |  | The media attribute 
| noBaseURL | boolean | false | false | Defaults to false. If you want to NOT append a request's ses or html base url then set this argument to true 
| charset | any | false | UTF-8 | The charset to add, defaults to utf-8 
| sendToHeader | boolean | false | false | Send to the header via htmlhead by default, else it returns the content 
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control 
