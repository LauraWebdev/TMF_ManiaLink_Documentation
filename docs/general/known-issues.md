# Known issues
This is a list of known issues and commonly asked questions.

## Why are my images blurry?
The quality of images depends on the players texture settings. This unfortunately means that only players with a texture quality of "high" will see your ManiaLink in high quality. Lower quality settings may lead to an odd rendering of your images.

## `addplayerid` is not secure
With various elements, you can include information about the player such as the id, nickname and selected zone. Since this information is displayed as a query parameter in the URL, it can be easily manipulated and should not be used to verify a player.

## The game crashes, if `folder` is not set for [&lt;fileentry&gt;](../elements/fileentry.md)
If you leave out the attribute `folder` for [&lt;fileentry&gt;](../elements/fileentry.md), the game will immediately crash. To avoid this bug, set the folder to an empty string (`folder=""`).

## Differences between United Forever and Nations Forever
While both TrackMania United Forever and TrackMania Nations Forever support ManiaLinks, there are still some small differences. Nations Forever are not allowed to register [named ManiaLinks](../setup/link-setup.md) or access them. Since the menu style is also slightly different (with a higher focus on green UI elements), visuals will not always be the same between the two versions.