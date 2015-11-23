
# autoDiscoveryLink Creates auto discovery links for RSS and ATOM feeds. 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| type | string | false | RSS | Type of feed: RSS or ATOM or Custom Type 
| href | any | false | [Not Defined] | The href link to discover 
| rel | any | false | alternate | The rel attribute 
| title | any | false |  | The title attribute 
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control 
