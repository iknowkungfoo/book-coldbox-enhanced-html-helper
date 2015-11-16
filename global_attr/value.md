# Value

The `value` attribute is only used by form fields. All values are properly XSS encoded using the proper contextual [OWASP ESAPI encoder functions](https://owasp-esapi-java.googlecode.com/svn/trunk_doc/latest/org/owasp/esapi/Encoder.html).

|Name   |Type   |Required   |Default |Hint  |
|-------|-------|-----------|--------|------|
|value   |string |false | |The value of the field.|

## Form Fields with Value as an Attribute

Most HTML form fields use `value` as an attribute. Notice that the space between "John" and "Smith" has been properly XSS encoded using `encodeForHTMLAttribute()`.

```html
// In the handler
<cfset rc.firstName = "John Smith" />

// In a viewlet
#html.textField(name = "firstName", value = rc.firstName)#

// The rendered HTML
<input class="cbhtml" name="firstName" value="John&#x20;Smith" id="firstName" type="text"/>
```
## Form Fields with Value as Content

A `<textarea>` is a form-associated element whose `value` is output as content between HTML tags. For this reason, the `value` has been encoded using `encodeForHTML()`. This is why the space between "John" and "Smith" displays as a simple space.

```html
// In the handler
<cfset rc.firstName = "John Smith" />

// In a viewlet
#html.textarea(name = "firstName", value = rc.firstName)#

// The rendered HTML
<textarea class="cbhtml" name="firstName" id="firstName">John Smith</textarea>
```