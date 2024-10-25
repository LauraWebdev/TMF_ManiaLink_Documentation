---
tags:
- Elements
---

# &lt;include&gt;
With this element, you can export elements of your ManiaLink in a seperate file. This can be helpful for elements that you want to reuse, such as a sidebar or navigation bar.

The content of the linked file will be directly imported at the place of the include element. It therefore does not require an XML doctype or a [&lt;manialink&gt;](./manialink.md) as a root element.

!!! note
    The linked file may only have one root element. If you want to include multiple elements, group them in an empty [&lt;frame&gt;](./frame.md) element.

!!! warn
    Since the [&lt;music&gt;](./music.md) may not be placed within a [&lt;frame&gt;](./frame.md), it can only be exported as the sole element in the linked file.

## Attributes
### `url="./header.xml"`
The path to the linked file.

## Examples
**index.xml**
```xml
<?xml version="1.0" encoding="utf-8" ?>
<manialink>
    <include url="./header.xml" />
</manialink>
```

**header.xml**
```xml
<frame>
    <quad posn="-20 -20 0" sizen="20 20" style="Bgs1InRace" substyle="BgWindow2" />
    <quad posn="20 20 1" sizen="20 20" style="Bgs1InRace" substyle="BgWindow1" />
</frame>
```