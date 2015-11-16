# ID and Name

As of HTML 5, the `name` attribute has been deprecated. ColdFusion still requires it for form fields whose values will are to be processed. The `id` attribute must be a unique value across the entire document. By default, there is no need to specify an id attribute, the HTML Helper will set the `id` attribute equal to its `name` attribute.

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
