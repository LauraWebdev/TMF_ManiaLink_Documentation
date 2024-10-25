---
tags:
- Elements
---

# &lt;quad&gt;
A quad is a rectangular shape that can display an image or a background color. It can link to ressources and have a special image for the `onMouseOver` event. It is a self-closing tag with no content.

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

### `image="./some-image.jpg"`
The image is scaled to fit the `<quad>`'s dimensions. Supported file formats are `.jpg`, `.tga`, `.dds` as well as `.gif` (256 colors with transparency) and `.png` (24bit with/without transparency).

### `imagefocus="./some-image-focus.jpg"`
Same as [image](#imagesome-imagejpg), replaces the set image when the mouse hovers over the `<quad>`.
!!! note
    A hover event is only fired if either `url`, `manialink` or `maniazones` is set.

### `style="CategoryName"`
The category name of a [predefined style](../general/predefined-styles.md). Both `style` and `substyle` are required, `image` and `imagefocus` will not be available if used.

### `style="StyleName"`
The style name of a [predefined style](../general/predefined-styles.md). Both `style` and `substyle` are required, `image` and `imagefocus` will not be available if used.

### `bgcolor="RGBA"`
A [color](../general/colors.md) to fill this `<quad>` with a solid color. Can also be set in a [&lt;format&gt;](./format.md) element but only affects other `<quad>` elements.

### `url="https://google.com"`
Links to an external page. Clicking minimizes the game and opens the default browser. 
!!! note
    You can only use either `url`, `manialink` or `maniazones`

### `manialink="ManiaLink"`
Links to a ManiaLink, either [linked](../setup/link-setup.md) or by URL.
!!! note
    You can only use either `url`, `manialink` or `maniazones`

### `maniazones="ManiaZone"`
Links to a ManiaZone
!!! note
    You can only use either `url`, `manialink` or `maniazones`

### `addplayerid="1"`
Adds additional playerdata to the URL as a query parameter.

| Parameter | Example | Description |
| --------- | ------- | ----------- |
| `playerlogin` | `nadeo` | The players login name |
| `lang` | `en` | The players language |
| `nickname` | `$f00Nadeo` | The players nickname (with styling) |
| `path` | `World/Germany/Bavaria/Nuremberg` | The players leaderboard location |

!!! warning
    This data can be manipulated by the player. [More information](../general/known-issues.md#addplayerid-is-not-secure)

## Example
```xml
<quad
    pos="-0.5 0.25 -0.5"
    size="1.2 0.2"
    valign="center"
    image="./header.png"
    imagefocus="./header-hover.png"
    manialink="./index.xml"
/>
```

```xml
<quad
    posn="0 0 0"
    sizen="32 32"
    halign="left"
    valign="top"
    style="Bgs1InRace"
    substyle="BgWindow1"
/>
```