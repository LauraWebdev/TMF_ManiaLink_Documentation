---
tags:
- Elements
---

# &lt;fileentry&gt;
Similar to [&lt;entry&gt;](./entry.md) elements, this element is used to receive player input, used in dynamic ManiaLinks. While `<entry>` elements hold `string` data, a `<fileentry>` element sends a selected file to the server through HTTP POST. When clicked by the player, a file browser opens and lets the user select a file.

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
The name for this `<fileentry>`. While not technically unique, subsequent `<fileentry>` elements with the same `name` will overwrite any data. This name will be the key.

### `folder="./"`
A path relative to the players `Documents/TrackMania` folder. It will be the entrypoint of the opened filebrowser and the upmost folder a player can jump to.

!!! warning
    This attribute is required, not setting it will crash the game. Since the default path is the `Documents/TrackMania` folder, you can prevent a game crash by just setting folder to an empty string (Example: `folder=""`)

### `default="value"`
The default value of this `<fileentry>`.

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
    <fileentry sizen="39 2" posn="16 -28 0" halign="left" style="TextValueSmall" name="avatarfilename" folder="skins\avatars" default="??"/>
    <label posn="1 -32 0" halign="left" style="CardButtonMediumWide" manialink="POST(http://localhost/ManialinkSamples/UploadAvatar.php?file=avatarfilename,avatarfilename)" addplayerid="1" text="Post with playerid, target=manialink"/>
</frame>
```