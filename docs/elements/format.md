---
tags:
- Elements
---

# &lt;format&gt;
This element applies textstylings to the parent and it's child elements which it was placed it. Only [&lt;label&gt;](./label.md), [&lt;entry&gt;](./entry.md), [&lt;fileentry&gt;](./fileentry.md) and [&lt;quad&gt;](./quad.md) elements are affected.

## Attributes
### `textsize="Number"`
The size of the text.

### `textcolor="RGBA"`
A [color](../general/colors.md) used for the text color.

### `bgcolor="RGBA"`
A [color](../general/colors.md) to fill a `<quad>` with a solid color.

### `style="StyleName"`
A [predefined style](../general/predefined-styles.md). Only text styles can be used.

## Examples
```xml
<format style="TextValueSmall" />
```

```xml
<quad posn="10 10 0" sizen="10 10">
    <format bgcolor="F00F" />
</quad>
```