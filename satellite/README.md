# satellite

Satellite background tiles for the ATY map panels, cut on the **same grid as `styleAtlas`**:
`{z}/{x}/{y}.jpg`, 256 px tiles, zoom 0-5 (z5 = 8192 x 8192 px). Zones and players keep
their world coordinates, so switching between `styleAtlas` and `satellite` never moves them.

```
https://raw.githubusercontent.com/atiysuu/mapStyles/main/satellite/{z}/{x}/{y}.jpg
```

## Source and attribution

Derived from the satellite layer of **[CreepPork/GTAV-Maps](https://github.com/CreepPork/GTAV-Maps)**,
MIT License, Copyright (c) 2019 Ralfs Garkaklis. The original license text is kept in
[`LICENSE-CreepPork-GTAV-Maps.txt`](LICENSE-CreepPork-GTAV-Maps.txt).

Changes made: the z7 tiles were assembled into one image, re-projected onto the `styleAtlas`
pixel grid (scale 0.7447, plus a small affine correction fitted against `styleAtlas`), resampled
and re-cut into the z0-5 pyramid, then saved as JPEG (quality 85).

## Rockstar Games material

The imagery is a rendering of the GTA V map. Grand Theft Auto V and its artwork are the property
of Rockstar Games / Take-Two Interactive. The MIT license above covers CreepPork's work, **not**
Rockstar's rights. This set is an unofficial fan-made derivative, not affiliated with or endorsed
by Rockstar Games or Take-Two, and it will be removed on request of the rights holder.

## Alignment

Measured against `styleAtlas` (the two layers are different drawings of the same map, so a few
pixels of disagreement are inherent to the sources): median 1.1 px over 645 interior patches,
about 70% within 2 px; larger local differences of up to roughly 6 px at z5 exist in places
(for example around LSIA). 1 px at z5 is about 1.5 world units.
