
# startForm Create cool form tags. Any extra argument will be passed as attributes to the form tag 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| action | string | false |  | The event or route action to submit to.	This will be inflated using the request's base URL if not a full http URL. If empty, then it is a self-submitting form |


| name | string | false |  | The name of the form tag |


| method | string | false | POST | The HTTP method of the form: POST or GET |


| multipart | boolean | false | false | Set the multipart encoding type on the form |


| ssl | boolean | false | false | If true, it will change http to https if found in the ses base url ONLY |


| noBaseURL | boolean | false | false | Defaults to false. If you want to NOT append a request's ses or html base url then set this argument to true |


| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control |


