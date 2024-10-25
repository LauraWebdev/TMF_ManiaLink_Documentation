# Text formatting
All standard text formatting from TrackMania is available for MediaLinks as part of the $-syntax. If you actually need to display a `$`, you can escape it with another $ (Example: `$$` becomes $).

## Examples
- `$i$bLorem&zIpsum` becomes ***Lorem***Ipsum
- `$l[http://www.google.com]` becomes [http://www.google.com](http://www.google.com)

## Options
| Syntax | Description | Example |   |
| ------ | ----------- | ------- | - |
| $[0-9a-z] | Text Color | `$FFFWhite $F00Red` | <span style="color: white">White</span> <span style="color: red">Red</span> |
| $t | Capitals | `$tHello` | HELLO |
| $i | Italic | `$iHello` | *Hello* |
| $s | Shadowed | `$sHello` | <span style="text-shadow: 1px 1px 0px grey">Hello</span> |
| $w | Wide Spacing | `$wHello` | <span style="letter-spacing: 0.3rem">Hello</span> |
| $n | Narrow Spacing | `$nHello` | <span style="letter-spacing: -0.05rem">Hello</span> |
| $m | Reset Spacing | `$wHello$mWorld` | <span style="letter-spacing: 0.3rem">Hello</span>World |
| $g | Reset Color | `$i$f00Hello$gWorld` | *<span style="color: #f00">Hello</span>World* |
| $z | Reset All | `$i$f00Hello$zWorld` | *<span style="color: #f00">Hello</span>*World |
| $o | Bold with semi-wide spacing | `$oHello` | **<span style="letter-spacing: 0.15rem">Hello</span>** |
| $h | ManiaLink | `$h[example:home]Home$h` | [Home](#) |
| $l | External Link | `$l[http://google.com]Google$l` | [Google](https://google.com) |
| $p | ManiaLink with Player Parameters | `$p[example:profile]Profile$p` | *The link includes `playerlogin`, `lang`, `nickname` and `path` query parameters* |