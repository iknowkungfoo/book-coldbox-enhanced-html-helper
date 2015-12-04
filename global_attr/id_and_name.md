# ID and Name

The `name` attribute [was deprecated](http://www.w3.org/TR/html5/obsolete.html) with the emergence of HTML 5. ColdFusion still requires it to know which form field values will be available to the server. 

The `id` attribute must be a unique value across the entire document. This is a function of the Document Object Model, by which JavaScript and CSS can identify specific elements.

By default, there is no need to specify an `id` attribute, the HTML Helper will set the `id` attribute equal to its `name` attribute.

|Name   |Type   |Required   |Default |Hint  |
|-------|-------|-----------|--------|------|
|name   |string |false | |The name of the field.|
|id     |string |false |Any value passed into name. |The unique ID of the field.|

Start with a basic text input field.

```html
// CFML
#html.textField(name = "firstName")#

// HTML rendered.
<input class="cbhtml" name="firstName" id="firstName" type="text">
```

Now, specify a unique `id` for the field.

```html
// CFML
#html.textField(name = "firstName", id = "id_firstName")#

// HTML rendered.
<input class="cbhtml" name="firstName" id="id_firstName" type="text">
```
