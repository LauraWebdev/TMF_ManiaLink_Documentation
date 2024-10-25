---
tags:
- Elements
---

# &lt;frame&gt;
A frame is a group of other elements with it's own position. Think of it as a `<div>` in HTML. With it, you can group areas (such as a sidebar or header). The frames position is added to the child elements position.

## Attributes
### `pos="X Y Z"`
[Classic positioning](../general/positioning.md#classical-united--nations), available for backwards compatibility

### `posn="X Y Z"`
[Modern positioning](../general/positioning.md#modern-united-forever--nations-forever)

## Example
```xml
<frame posn="20 20 0">
    <quad posn="10 -10 0" />
</frame>
```
Since the frame is at position `20 20 0`, the child `<quad>` element with the position `10 -10 0` will be at position `30 10 0`.