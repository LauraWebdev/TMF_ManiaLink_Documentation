---
tags:
- Elements
---

# &lt;label&gt;
A label can be used to display text. It can have a link and be [localized](../general/multi-language.md).

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

### `text="Hello"`
The text to display, it supports all [text formatting options](../general/text-formatting.md). Word-wraps are preserved.

### `autonewline="1"`
This attribute enables automatic word-wrap if text overflows. If set to `0`, overflowing text will be cut off instead.

### `maxline="Number"` <!-- TODO: IS IT maxlines OR maxline -->
Controls how many lines this `<label>` can occupy.

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
### `textsize="Number"`
The size of the text.

### `textcolor="RGBA"`
A [color](../general/colors.md) used for the text color.

### `size="StyleName"`
A [predefined style](../general/predefined-styles.md). Only text styles can be used.

## Examples
```xml
<label
    posn="-30 -20 5"
    halign="center"
    style="CardButtonMedium"
    text="$o$008White Button with darkblue Font"
/>
```