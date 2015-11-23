
# meta Helps you generate meta tags 

1. **Access**: public
2. **Location**: HTMLHelper Extended 

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| name | any | true | [Not Defined] | A name for the meta tag or an array of struct data to convert to meta tags.Keys [name,content,type] |


| content | any | false |  | The content attribute |


| type | string | false | name | Either ''name'' or ''equiv'' which produces http-equiv instead of the name |


| sendToHeader | boolean | false | false | Send to the header via htmlhead by default, else it returns the content |


