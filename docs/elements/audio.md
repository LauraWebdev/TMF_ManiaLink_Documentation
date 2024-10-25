---
tags:
- Elements
---

# &lt;audio&gt;
This element creates an audio player. Unlike [&lt;music&gt;](./music.md), the audio player is visible and can be interacted with by the player. Valid formats are `.ogg` and `.mux`

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

### `data="audio.ogg"`
The path to the audio file. You can also wrap the path in the element instead. (Example: `<audio>audio.ogg</audio>`)

### `play="1"`
This audio automatically starts playing when set to `1`

### `looping="0"`
The audioplayer stops after the audio played once when set to `0`. The default value is `1` (looping)

## Examples
```xml
<audio
    pos="0 0 0"
    data="alpine_race.ogg"
/>
```