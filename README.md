# Black Ops (2010) PS3 zombies — map viewer

Live: **https://justinbulbasaur.github.io/blackops-zombies-viewer/**

The three zombie maps of Call of Duty: Black Ops (Kino der Toten, "Five", Dead Ops Arcade),
extracted from the PS3 disc's fast files and texture paks into glTF, plus weapon models,
the maps' lights / entities / weapon definitions, and the loading videos.

* `index.html` — three.js map viewer (WASD fly, drag to look). Loads `maps/*.opt.glb`.
* `model.html?glb=models/<name>.glb` — orbit viewer for single models (Thundergun, Ray Gun).
* `maps/` — meshopt-compressed GLBs with WebP textures (files over 24 MiB are split into
  `.partN` pieces the viewer re-joins), `manifest.json`, per-map stats.
* `data/` — primary lights and collision counts (`*_world.json`), entity strings
  (`*_mapents.txt`), full weapon definitions (`weapons_*.json`), texture tables.
* `screenshots/` — spawn-room renders and weapon renders.
* `videos/` — loading / outro videos.

Everything was produced by the Python tools in the private extraction project (zone walker,
DXT decoder, glTF writer); this repo only holds the published output. Coordinates are
Y-up metres (CoD inches × 0.0254). Lighting in the viewer is a plain hemisphere light, not
the game's baked lightmaps.
