# Class

By default, any HTML Helper generated element gets the class `cbhtml`.

```html
// CFML
#html.textField(name = "firstName")#

// HTML rendered.
<input class="eqhtml" name="firstName" id="firstName" type="text">
```
Any `class` you define on the element will have that default class appended to it.

```html
// CFML
#html.textField(name = "firstName", class="required")#

// HTML rendered.
<input class="required&#x20;cbhtml" name="firstName" id="firstName" type="text"/>
```
1. The class "required" was defined for this text field.
2. The class "eqhtml" was appended to the class definition.
3. The final value for the class attribute was properly XSS encoded for an HTML Attribute.

## CSS Overrides

One reason for adding the class of `cbhtml` to HTML Helper elements is to override existing CSS definitions without affecting legacy code.

For example, this defines a default for these three HTML elements with the class of `cbhtml`.

```css
input.cbhtml, select.cbhtml, textarea.cbhtml {
    background: none; 
    padding-right: 0px; 
    background-color: white;
}
```

Here is a legacy definition, along with an additional definition for elements that have both the class required and the class `cbhtml` defined.

```css
# Legacy definition
label.required {float:right;}

# HTML Helper Override
label.required.cbhtml {float:none;}
```
