
# &lt;docType&gt;

Render a doctype by type name. The doctype specifies which version of (X)HTML that page is using.

1. **Access**: public
2. **Location**: HTMLHelper Core

## Arguments

| name 	| type 	| required 	| default 	| hint 	|
|:--- 	|:--- 	|:--- 		|:--- 		|:--- 	|
| type | string | false | html5 | The doctype to generate, we default to HTML 5 |


## Available Doc types

* xhtml11
* xhtml1-strict
* xhtml-trans
* xthml-frame
* html5 (default)
* html4-strict
* html4-trans
* html4-frame

## Usage

This should only exist at the top of a layout, above the `<html>` tag.

```html
// CFML
<cfoutput>
#html.doctype()#
<html>
<head>
</cfoutput>

// HTML
<!DOCTYPE html>
<html>
<head>
```