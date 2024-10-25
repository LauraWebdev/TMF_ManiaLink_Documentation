# ManiaCodes
ManiaCodes are small XML files containing links to ressources such as Tracks, Replays or Skins. They are generally used to give players the option to download Avatars, Horns or Skins through a [ManiaLink](../index.md#what-is-a-manialink).

!!! warning
    To create and access ManiaCodes, you must own a Trackmania United Forever account. Trackmania Nations Forever accounts have no access to ManiaCodes.

## Registering a ManiaCode
As with ManiaLinks, ManiaCodes must be created through the Trackmania player page. Please visit the [Link Setup](../setup/link-setup.md) guide for more information.

## Syntax
A ManiaCode, much like a ManiaLink, is an XML file. Unline ManiaLinks, the root element is not [&lt;manialink&gt;](../elements/manialink.md) but `<maniacode>`. There are special ManiaCodes elements that can be combined as children of the root element.

### Example
```xml
<?xml version='1.0' encoding='utf-8' ?>
<maniacode>
    <!-- Content -->
</maniacode>
```

## Elements
### ``show_message``
This message will be displayed as a dialog after the ManiaCode finished running. If not specified, the game will display `Maniacode completed` instead.

```xml
<show_message>
    <message>Thank you!</message>
</show_message>
```

### ``install_track``
This element, lets a player permanently install a track. The `name` element is used to define a filename after download. It will always be suffixed by `.Challenge.Gbx`.

```xml
<install_track>
    <name>TrackDavid</name>
    <url>http://data.trackmaniaunited.com/tracks/TrackDavid.Challenge.Gbx</url>
</install_track>
```

### ``play_track``
This element lets a player play a track. The syntax is similar to ``install_track`` but it does not permanently download the track. After leaving the track, the game will remove it.

```xml
<play_track>
    <name>TrackDavid</name>
    <url>http://data.trackmaniaunited.com/tracks/TrackDavid.Challenge.Gbx</url>
</play_track>
```

### ``install_replay``
This element lets a player permanently download ghost data from a replay. As with tracks, the `name` attribute is used to rename the downloaded file and suffixed by `.Replay.Gbx`.

```xml
<install_replay>
    <name>ReplayDavid</name>
    <url>http://data.trackmaniaunited.com/replays/ReplayDavid.Replay.Gbx</url>
</install_replay>
```

### ``view_replay``
This element lets a player see a replay. As with ``play_track``, the downloaded data is immediately loaded and not permanently stored. After leaving the replay viewer, the replay will be removed.

```xml
<view_replay>
    <name>ReplayDavid</name>
    <url>http://data.trackmaniaunited.com/replays/ReplayDavid.Replay.Gbx</url>
</view_replay>
```

### ``play_replay``
This element lets a player play against the ghost of a replay. As with ``play_replay``, the downloaded data is immediately loaded and not permanently stored. Afterwards, the replay will be removed.

```xml
<play_replay>
    <name>ReplayDavid</name>
    <url>http://data.trackmaniaunited.com/replays/ReplayDavid.Replay.Gbx</url>
</play_replay>
```

### ``join_server``
This element lets a player join a server. The destination can either be the direct IP or a registered login name.

```xml
<join_server>
    <ip>213.186.41.190:30000</ip>
</join_server>
```

```xml
<join_server>
    <login>my_server</login>
</join_server>
```

### ``install_skin``
This element lets a player download a car skin. After the download finishes, the player is asked if they want to apply the skin. The `name` element is used for the download modal, while `file` defines the file destination and `url` defines the file origin. The `file` element defines the type of skin (Example: ``Skins/Vehicles/SportCar`` is a skin for the car used in the `Island` environment)

#### Skin types
| Path | Type |
| ---- | ---- |
| `Skins/Vehicles/` | Cars |
| `Skins/Horns/` | Horns |
| `Skins/Avatars/` | Avatars |
| `ChallengeMusics/` | Music (`.ogg` or `.mux`) |
| `Skins/CarEngines` | Engine Sounds |

#### Car skin types
| Path | Environment |
| ---- | ---- |
| CarCommon | Any |
| AmericanCar | Desert |
| RallyCar | Rally |
| SnowCar | Snow |
| SportsCar | Island |
| CoastCar | Coast |
| BayCar | Bay |
| StadiumCar | Stadium |

!!! note
    Locators for skins are generated automatically. You should not add them to your ManiaCode.

```xml
<install_skin>
    <name>TestDavid</name>
    <file>Skins/Vehicles/SportCar/TestDavid.zip</file>
    <url>http://data.trackmaniaunited.com/vehicles/TestDavid.zip</url>
</install_skin>
```

### ``get_skin``
This element is used to load a replays custom car into the cache of the game so it can be displayed in a replay.
```xml
<get_skin>
    <name>TestDavid</name>
    <file>Skins/Vehicles/CarCommon/TestDavid.zip</file>
    <url>http://data.trackmaniaunited.com/vehicles/TestDavid.zip</url>
</get_skin>
```

### ``add_buddy``
This element lets a player add another player as a friend (through the Buddy List system).

```xml
<add_buddy>
    <login>tmuffan</login>
</add_buddy>
```

### ``add_favourite``
This element lets a player add a server as their favorite. You can either specify the direct IP or a registered login name.

```xml
<add_favourite>
    <ip>213.186.41.190:30000</ip>
</add_favourite>
```

```xml
<add_favourite>
    <login>my_server</login>
</add_favourite>
```

### ``goto``
This element is used to redirect the player to a ManiaLink. It is frequently used to add "donation" features to a ManiaLink.

```xml
<goto>
    <link>MyManiaLink</link>
</goto>
```

### ``install_track_pack``
This element lets the player install a group of tracks as a combined folder. The downloaded pack will be available under ``/Tracks/Challenges/Downloaded/ManiaLink/``.

```xml
<install_track_pack>
    <name>Testfolder</name>
    <track>
        <name>Trackname1</name>
        <url>http://www.yourdomain.com/Tracks/Test.Challenge.Gbx</url>
    </track>
    <track>
        <name>Trackname2</name>
        <url>http://www.yourdomain.com/Tracks/Test2.Challenge.Gbx</url>
    </track>
</install_track_pack>
```