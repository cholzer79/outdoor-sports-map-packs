# outdoor-sports-map-packs

Offline map packs of the outdoor details hikers and climbers need: via ferratas and their grades, material ropeways,
peaks, huts, saddles, graded mountain paths and forest roads. A desktop app downloads them instead of asking the
Overpass API for every area its activities cross.

**Map data © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright), available under the
[Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/).** The packs are built from the extracts of
[Geofabrik](https://download.geofabrik.de). They are a derived database of OpenStreetMap and are shared under the same
licence: you may use them freely if you credit OpenStreetMap and share changes to them under the ODbL.

## What is here

```
regions.json     the regions the packs cover, each a whole Geofabrik extract by its id (with a German name)
manifest.json    every published part: area, regions, release, file, size, sha256, data date, build date, pieces held;
                 "checked" says when the tool last looked (the app ignores packs not checked for more than two months)
```

The part files themselves are in the [releases](../../releases), one release per data month (e.g. `2026-10`), one
file per area of about 100 km (`x-y.pack`: zoom-8 tile x/y, gzipped JSON). A part that did not change keeps its older
release, so a new release holds only what changed.

First regions: Switzerland, Liechtenstein, Austria, Bavaria and Italy's Nord-Est (South Tyrol, Trentino).

## Making and uploading the packs

The packs are made by the map pack tool on a PC or a server, never by GitHub Actions. Its README has the GitHub setup
(signing in with the GitHub CLI on a PC, a fine-grained token limited to this repository on a server), the first
upload and how to run it on a schedule.
