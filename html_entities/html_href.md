
# href Create href tags, using the SES base URL or not 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| href | any | false |  | Where to link to, this can be an action, absolute, etc |


| text | any | false |  | The text of the link |


| queryString | any | false |  | The query string to append, if needed. |


| title | any | false |  | The title attribute |


| target | any | false |  | The target of the href link |


| ssl | boolean | false | false | If true, it will change http to https if found in the ses base url ONLY |


| noBaseURL | boolean | false | false | Defaults to false. If you want to NOT append a request's ses or html base url then set this argument to true |


| img | struct | false | StructNew() | Defines an img for the content of the href instead of text. Supercedes text argument. |


| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control |


