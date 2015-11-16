# Label and Content Wrappers

These attributes wrap the core HTML element with other HTML tags.

|Name   |Type   |Required   |Default |Hint  |
|-|-|-|-|-|
|wrapper        |string     |false  |   |The wrapper to use around the tag. Empty by default.
|groupWrapper   |string     |false  |   |The wrapper tag to use around the tag and label. Empty by default.
|label          |string     |false  |   |If a value is passed in, a `<label>` tag will be wrapped around the HTML element.
|labelWrapper   |string     |false  |   |The wrapper tag to use around the label. Empty by default.
|labelClass     |string     |false  |   |The class to be applied to the `<label>`.

Start with a basic text input field.

```html
// CFML
#html.textField(name = "firstName")#

// HTML
<input class="cbhtml" name="firstName" id="firstName" type="text">
```

Now add a `<label>`. Notice that the `<label>` was automatically given a `for` attribute, populated with the input's id value.

```html
// CFML
#html.textField(name = "firstName", label = "First Name")#

// HTML
<label for="firstName" class="cbhtml">First Name</label>
<input class="cbhtml" name="firstName" id="firstName" type="text"/>
```

Next, wrap both the `<label>` and `<input>` with table cells.

```html
// CFML
#html.textField(name = "firstName", wrapper = "td", label = "First Name", labelWrapper = "td")#

// HTML
<td><label for="firstName" class="cbhtml">First Name</label></td>
<td><input class="cbhtml" name="firstName" id="firstName" type="text"/></td>
```

Last, wrap both table cells with a table row using `groupWrapper` and give the `<label>` a class of `required`.

```html
// CFML
#html.textField(
    name = "firstName"
    , wrapper = "td"
    , groupWrapper = "tr"
    , label = "First Name"
    , labelWrapper = "td"
    , labelClass = "required")#

// HTML
<tr>
    <td><label for="firstName" class="required&#x20;cbhtml">First Name</label></td>
    <td><input class="cbhtml" name="firstName" id="firstName" type="text"/></td>
</tr>
```

Notice that the value of the `class` attribute contains the string `&#x20:`. This is the properly XSS encoded value of a space (" ") in an HTML attribute.

## Attributes on Wrappers

Any `wrapper` or `labelWrapper` can have attributes passed to them directly in the value. Here is an example of adding the class `myclass` to the `<td>` that is wrapping the `<label>`. In this case, the default class `cbhtml` is not added to those elements.

```html
// CFML
#html.textField(
    name = 'firstName'
    , wrapper = 'td'
    , groupWrapper = 'tr'
    , label = 'First Name'
    , labelWrapper = 'td class="myclass"'
    , labelClass = 'required')#

// HTML rendered.
<tr>
    <td class="myclass"><label for="firstName" class="required&#x20;cbhtml">First Name</label></td>
    <td><input class="cbhtml" name="firstName" id="firstName" type="text"/></td>
</tr>
```
