# Structure
ManiaLinks are `utf-8` encoded XML files. Since there are no ways to create a scrollable area, all pages must be made to fit and use pagination instead. All ManiaLink pages use an absolute [positioning](./positioning.md), so a ManiaLink created for a 1280x1024 monitor will scale proportionally on a 640x480 monitor.

Each ManiaLink starts with the XML-Doctype, this line describes what content and encoding is to be expected.
```xml
<?xml version="1.0" encoding="utf-8"?>
```

After the doctype, you can use all sorts of elements within a [<manialink\>](../elements/manialink.md) tag.
```xml
<?xml version="1.0" encoding="utf-8"?>
<manialink>
    <timeout>0</timeout>

    <label posn="-20 0 1" text="example" />
</manialink>
```

## Project Structure
It is a best practice to organize your project properly. This is an example of a bigger ManiaLink project.

```
|- partials
|  |- header.xml
|  |- footer.xml
|  |- navigation.xml
|- media
|  |- audio
|  |  |- background.ogg
|  |  |- horn01.ogg
|  |  |- horn02.ogg
|  |  |- horn03.ogg
|  |  |- horn04.ogg
|  |- images
|  |  |- logo.tga
|  |  |- profile.tga
|  |  |- header_banner.tga
|  |  |- background.tga
|- index.xml
|- about.xml
|- horns.xml
```