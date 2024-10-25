---
tags:
- Elements
---

# &lt;entry&gt;
The `<entry>` element is the ManiaLink equivalent of an `<input>` in HTML. It allows arbitrary user input. Any data will be appended to the next navigation as a query parameter, static ManiaLink's therefore are not able to respond to player input.

!!! warn
    `<entry>` elements always hold data as a `string`. Any syntax checking must be done server-side.

<!-- TODO: Check if this actually works as a key:value and not an url replacement -->

## Attributes
### `pos="X Y Z"`
[Classic positioning](../general/positioning.md#classical-united--nations), available for backwards compatibility

### `posn="X Y Z"`
[Modern positioning](../general/positioning.md#modern-united-forever--nations-forever)

### `size="width height"`
[Classic sizing](../general/positioning.md#classical-united--nations), available for backwards compatibility

### `sizen="width height"`
[Modern sizing](../general/positioning.md#modern-united-forever--nations-forever)

### `scale="factor"`
Element scale, a scale of `2` doubles the size.

### `halign="left|center|right"`
[Horizontal Aligment](../general/positioning.md#alignment)

### `valign="top|center|bottom"`
[Vertical Aligment](../general/positioning.md#alignment)

### `name="EntryName"`
The name for this entry. While not technically unique, subsequent `<entry>` elements with the same `name` will overwrite any data. This name will be the query parameters key.

### `default="value"`
The default value of this entry. It will be the query parameters value if unchanged.

### `autonewline="1"`
This attribute enables automatic word-wrap if text overflows. If set to `0`, overflowing text will be cut off instead.

### `textsize="Number"`
The size of the text.

### `textcolor="RGBA"`
A [color](../general/colors.md) used for the text color.

### `size="StyleName"`
A [predefined style](../general/predefined-styles.md). Only text styles can be used.

## Examples
```xml
<frame>
    <entry posn="15 -8 5" sizen="5 2" style="TextValueSmall" name="inputvalue" default="42" />
    <label posn="15 -1 -12 5" style="CardButtonMedium" text="Link with value" url="http://site.php?value=inputvalue" />
</frame>
```