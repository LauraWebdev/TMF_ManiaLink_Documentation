---
tags:
- Elements
---

# &lt;timeout&gt;
This element controls the time Trackmania Forever will cache your ManiaLink. If your ManiaLink is serving dynamic content that changes frequently, it might make sense to set this value lower. For local development, you should use a value of `0` to turn off caching entirely.

## Examples
```xml
 <!-- Caching turned off -->
<timeout>0</timeout>
```

```xml
 <!-- Caching for 1 hour -->
<timeout>3600</timeout>
```