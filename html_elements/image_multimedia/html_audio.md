
# audio Create an HTML 5 audio tag 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| src | any | true | [Not Defined] | The source URL or array or list of URL's to create audio tags for |
| autoplay | boolean | false | false | Whether or not to start playing the audio as soon as it can |
| controls | boolean | false | true | Whether or not to show controls on the audio player |
| loop | boolean | false | false | Whether or not to loop the audio over and over again |
| preLoad | boolean | false | false | If true, the audio will be loaded at page load, and ready to run. Ignored if 'autoplay' is present |
| noBaseURL | boolean | false | false | Defaults to false. If you want to NOT append a request's ses or html base url then set this argument to true |
| name | string | false |  | The name tag |
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control |

