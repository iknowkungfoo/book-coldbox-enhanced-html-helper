
# video Create an HTML 5 video tag 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

| name 	| type 	| required 	| default 	| hint
|:--- 	|:--- 	|:--- 		|:--- 		|:---


| src | any | true | [Not Defined] | The source URL or array or list of URL's to create video tags for 
| width | string | false |  | The width tag 
| height | string | false |  | The height tag 
| poster | string | false |  | The URL of the image when video is unavailable 
| autoplay | boolean | false | false | Whether or not to start playing the video as soon as it can 
| controls | boolean | false | true | Whether or not to show controls on the video player 
| loop | boolean | false | false | Whether or not to loop the video over and over again 
| preload | boolean | false | false | If true, the video will be loaded at page load, and ready to run. Ignored if 'autoplay' is present 
| noBaseURL | boolean | false | false | Defaults to false. If you want to NOT append a request's ses or html base url then set this argument to true 
| name | string | false |  | The name tag 
| data | struct | false | StructNew() | A structure that will add data-{key} elements to the HTML control 
