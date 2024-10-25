---
tags:
- Elements
---

# &lt;music&gt;
This element creates an invisible audio player. Unlike [&lt;audio&gt;](./audio.md), the audio player is not visible. It is generally used for background music. Valid formats are `.ogg` and `.mux`. If you change the ManiaLink (for example through a link) and the other ManiaLink also includes the same music tag, it will continue playing during and after navigation.

!!! warning
    This element only works when placed as a direct child of [&lt;manialink&gt;](./manialink.md), it cannot be placed in a [&lt;frame&gt;](./frame.md)

!!! note
    Although not required, it is best practice to place your music element as the last element for clarity.

## Attributes
### `data="music.ogg"`
The path to the audio file.

## Examples
```xml
<music data="alpine_race.ogg" />
```