---
tags:
- Elements
---

# &lt;video&gt;
This element creates a video player. Only BINK (.bik) videos are supported.

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

### `data="video.bik"`
The path to the videofile. You can also wrap the path in the element instead. (Example: `<video>video.bik</video>`)

### `play="1"`
This video automatically starts playing when set to `1`

### `looping="0"`
The videoplayer stops after the video played once when set to `0`. The default value is `1` (looping)

## Examples
```xml
<video
    pos="0 0 0"
    size="0.512 0.256"
    data="sign_warning.bik"
    play="1"
/>
```