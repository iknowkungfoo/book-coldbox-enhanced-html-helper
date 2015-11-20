# Data Attributes

> HTML5 is designed with extensibility in mind for data that should be associated with a particular element but need not have any defined meaning. data-* attributes allow us to store extra information on standard, semantic HTML elements without other hacks such as classList, non-standard attributes, extra properties on DOM, or setUserData.

- [Using Data Attributes @ MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_data_attributes)

Instead of creating arbitrary attributes on an HTML element, prefix them with `data-`. This will put them into the element's data collection. In the HTML source you will see the `data-` values that were defined on render. Anything added to the data collection via JavaScript will not be visible in the HTML.

***No Personally identifiable information (PII) should ever go into data attributes.***

Here is a simple text input using data attributes to specify a related field ID. Notice that the data attributes are defined as a struct, using the key `data` at the root.

```html
// CFML
#html.textField(
    name = "firstName"
    , data = { relatedID = "lastName"})#
 
// HTML
<input class="cbhtml" name="firstName" id="firstName" data-relatedid="lastName" type="text"/>
```

If your data key needs to contain a hyphen, then make sure to surround the key with double-quotes.

```html
// CFML
#html.textField(
    name = "firstName"
    , data = { "related-ID" = "lastName"})#
 
// HTML
<input class="cbhtml" name="firstName" id="firstName" data-related-id="lastName" type="text"/>
```

### Notes

1. Regardless of how defined, ***data keys in HTML are output in lowercase***. 
2. jQuery does not always reference them in that format.

## jQuery

> **.data()**
> 
> Store arbitrary data associated with the matched elements or return the value at the named data store for the first element in the set of matched elements.

- [jQuery API Documentation](http://atlas.altidev.net/confluence/pages/editpage.action?pageId=69697538)

Here is that simple text input with the data key specifying a related field ID. They data key `data-relatedid` is defined.

```html
// CFML
#html.textField(
    name = "firstName"
    , data = { relatedID = "lastName"})#
 
// HTML
<input class="cbhtml" name="firstName" id="firstName" data-relatedid="lastName" type="text"/>
```
Referencing the data collection via jQuery:
```javascript
// jQuery
var data = jQuery('#firstName').data();
 
// jQuery defines data as a JSON Object containing
{ "relatedid" : "lastName" }
```
 If your data key has a hyphen in it, then jQuery returns the key as lower camel case.

```html
// CFML
#html.textField(
    name = "firstName"
    , data = { "related-ID" = "lastName"})#
 
// HTML
<input class="cbhtml" name="firstName" id="firstName" data-related-id="lastName" type="text"/>
```

```javascript
// jQuery
var data = jQuery('#firstName').data();
 
// jQuery defines data as a JSON Object containing
{ "relatedId" : "lastName" }
// Notice the capital "I" in relatedId.
```

## Why Use Data Attributes?

I might write a some conditional logic using JavaScript to do the following:

1. If the field "firstName" is filled out, then ensure the field defined in `data-related-id` is also populated.
2. If I select a value from a `<select>` field, then use that value in a query to populate a related `<select>` using the value in `data-related-id`.

These also come in handy when using the [jQuery Validate](http://jqueryvalidation.org/) plugin for form validation.

```html
// CFML
#html.textField(
    name = "firstName"
    , class = "required"
    , data = { "msg-required" = "Please enter a First Name."})#
 
// HTML
<input class="cbhtml" name="firstName" id="firstName" class="required" type="text"
    data-msg-required="Please enter a First Name" />
```

This and other `data-` attributes can be used to set or override validation configuration without writing additional JavaScript.