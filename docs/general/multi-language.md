# Multi-Language
Many different elements of a ManiaLink can be served in the players language. By utilizing a localization file, you can easily organize and adjust text and images for different languages. To localize an attribute, you simply add `id` to the end of the attribute and enter a localization id. (Example: `text` becomes `textid`). In your localization file, you use the localization id to provide different values for the attribute per language.

Localizations are grouped in the [&lt;dico&gt;](../elements/dico.md) element. Within it, you must provide a language through the [&lt;language&gt;](../elements/language.md) element. In that element, you use the localization id as the elements tag to provide values for the attribute.

!!! note
    If a certain localization id or language does not exist, the game will default to the **English** localization.

## Restrictions
A localization id must be a valid tag name. It must start with a letter and only include letters and numbers. The only special characters you can use are dashes and underscores. Furthermore, only some attributes of a few elements can be localized.

- [<quad\>](../elements/quad.md)
    - `image`
    - `imagefocus`
    - `url`
    - `manialink`
- [<label\>](../elements/label.md)
    - `text`
    - `url`
    - `manialink`
- [<audio\>](../elements/audio.md)
    - `data`
- [<video\>](../elements/video.md)
    - `data`

!!! warning
    This list might not be complete

## Localization Files
While you can also provide localizations within your ManiaLink's XML, it is best practice to create a seperate file for them and include them in your ManiaLink. This way, you can focus on all localized attributes and reuse them on multiple pages.

**localization.xml**
```xml
<dico>
    <language id="en">
        <example>Example</example>
        <greeting>Welcome!</greeting>
    </language>
    <language id="de">
        <example>Beispiel</example>
        <greeting>Wilkommen!</greeting>
    </language>
</dico>
```

**index.xml**
```xml
<?xml version="1.0" encoding="utf-8" ?>
<manialink>
    <include url="./localization.xml" />

    <label posn="-20 0 1" textid="example" />
    <label posn="-20 -10 1" textid="greeting" />
</manialink>
```

## Language Codes
| Code | Language   |
|------|------------|
| cz   | Czech      |
| de   | German     |
| en   | English    |
| es   | Espanol    |
| fr   | French     |
| hu   | Hungarian  |
| it   | Italian    |
| jp   | Japanese   |
| kr   | Croatian   |
| nl   | Dutch      |
| pl   | Polish     |
| pt   | Portuguese |
| ru   | Russian    |
| sk   | Slovak     |
| zh   | Chinese    |