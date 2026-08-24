# MAP ROOM

3D deep basemap room. Pure HTML / CSS / JS.

**Live:** https://artsrun.github.io/map-room/

## Stack

| Layer | API |
|---|---|
| Room | CSS `perspective` + `preserve-3d` |
| Faces + well | Carto raster XYZ |
| Fly-to | HTML `<map>` / `<area>` + city chips + minimap click |
| Camera | pointer / pinch / wheel / WASD |
| Frame | `requestAnimationFrame` (update-the-rendering) |
| Optional | WICG `layoutsubtree` + `drawElementImage` + `onpaint` |

Tiles: `https://{a-d}.basemaps.cartocdn.com/{style}/{z}/{x}/{y}@2x.png`  
© OpenStreetMap · © CARTO

## Controls

- drag — orbit
- wheel — dolly (`shift`/`ctrl`+wheel = zoom)
- pinch — zoom
- `WASD` orbit · `Q`/`E` push · `+`/`-` zoom
- minimap click — fly to that mercator point
- chips — Yerevan / Ararat / Tbilisi / Istanbul / Ankara

Chip `tests: n/n` is an in-page mercator + URL self-check.

## html-in-canvas

`chrome://flags/#canvas-draw-element` → Enabled → relaunch.

Without the flag the room still runs (CSS HUD).

Explainer: https://github.com/WICG/html-in-canvas

## Pages

Settings → Pages → Deploy from branch **prod** `/`  
or the `pages` workflow on push to `prod`.
