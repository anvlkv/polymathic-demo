+++
title="field"
description="Bulma form field component"
+++

```md
    {{/* field(type="email",name="email",label="Email with autocomplete off", autocomplete="off") */}}
```

{{ field(type="email",name="email",label="Email with autocomplete off", autocomplete="off") }}

```md
    {{/* field(type="file",name="file",label="File input") */}}
```

{{ field(type="file",name="file",label="File input") }}

```md
    {{/* field(type="textarea",name="textarea",label="Textarea") */}}
```

{{ field(type="textarea",name="textarea",label="Textarea") }}

```md
    {{/* field(name="text",label="Text") */}}
```

{{ field(name="text",label="Text") }}



```md
    {%/* field(type="select",label="Select", name="select") */%}

    <optgroup label="Group 1">
        <option>
            Option 1
        </option>
        <option>
            Option 2
        </option>
    </optgroup>
    <optgroup label="Group 2">
        <option>
            Option 3
        </option>
        <option>
            Option 4
        </option>
    </optgroup>

    {%/* end */%}
```

{% field(type="select",label="Select", name="select") %}

<optgroup label="Group 1">
    <option>
        Option 1
    </option>
    <option>
        Option 2
    </option>
</optgroup>
<optgroup label="Group 2">
    <option>
        Option 3
    </option>
    <option>
        Option 4
    </option>
</optgroup>

{% end %}

```md
    {%/* field(type="checkbox", name="check", label="Checkbox") */%}

    Some value [with a link](/some-where)

    {%/* end */%}
```

{% field(type="checkbox", name="check", label="Checkbox") %}

Some value [with a link](/some-where)

{% end %}

```md
    {{/* field(type="radio", name="radio", label="Radio buttons", options=["Variant A","Variant B","Variant C"]) */}}
```

{{ field(type="radio", name="radio", label="Radio buttons", options=["Variant A","Variant B","Variant C"])}}

```md
    {%/* field(type="submit") */%}
        Submit button text
    {%/* end */%}
```

{% field(type="submit") %}
Submit button text
{% end %}

```md
    {%/* field(type="reset") */%}
        Reset button text
    {%/* end */%}
```

{% field(type="reset") %}
Reset button text
{% end %}

## Horizontal layout

```md
    {{/* field(horizontal=true, type="email",name="email",label="Email with autocomplete off", autocomplete="off") */}}
```

{{ field(horizontal=true, type="email",name="email",label="Email with autocomplete off", autocomplete="off") }}

```md
    {{/* field(horizontal=true, type="file",name="file",label="File input") */}}
```

{{ field(horizontal=true, type="file",name="file",label="File input") }}

```md
    {{/* field(horizontal=true, type="textarea",name="textarea",label="Textarea") */}}
```

{{ field(horizontal=true, type="textarea",name="textarea",label="Textarea") }}

```md
    {{/* field(horizontal=true, name="text",label="Text") */}}
```

{{ field(horizontal=true, name="text",label="Text") }}



```md
    {%/* field(horizontal=true, type="select",label="Select", name="select") */%}

    <optgroup label="Group 1">
        <option>
            Option 1
        </option>
        <option>
            Option 2
        </option>
    </optgroup>
    <optgroup label="Group 2">
        <option>
            Option 3
        </option>
        <option>
            Option 4
        </option>
    </optgroup>

    {%/* end */%}
```

{% field(horizontal=true, type="select",label="Select", name="select") %}

<optgroup label="Group 1">
    <option>
        Option 1
    </option>
    <option>
        Option 2
    </option>
</optgroup>
<optgroup label="Group 2">
    <option>
        Option 3
    </option>
    <option>
        Option 4
    </option>
</optgroup>

{% end %}

```md
    {%/* field(horizontal=true, type="checkbox", name="check", label="Checkbox") */%}

    Some value [with a link](/some-where)

    {%/* end */%}
```

{% field(horizontal=true, type="checkbox", name="check", label="Checkbox") %}

Some value [with a link](/some-where)

{% end %}

```md
    {{/* field(horizontal=true, type="radio", name="radio", label="Radio buttons", options=["Variant A","Variant B","Variant C"]) */}}
```

{{ field(horizontal=true, type="radio", name="radio", label="Radio buttons", options=["Variant A","Variant B","Variant C"])}}

```md
    {%/* field(horizontal=true, type="submit") */%}
        Submit button text
    {%/* end */%}
```

{% field(horizontal=true, type="submit") %}
Submit button text
{% end %}

```md
    {%/* field(horizontal=true, type="reset") */%}
        Reset button text
    {%/* end */%}
```

{% field(horizontal=true, type="reset") %}
Reset button text
{% end %}