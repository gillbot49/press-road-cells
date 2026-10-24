# press-road-cells
OpenStreetMap road network cells for Press. Data (c) OpenStreetMap contributors, ODbL 1.0.

- **Road cells** are the assets of the `road-cells-v1` release (`cells.json` lists them), made by
  `tools/build-road-graph.mjs` in the Press repository.
- **Place files** are in `places/` (`places.json` lists them), one per road cell on the same key:
  townlands with their outlines and counties, towns and villages, named streets and house numbers,
  for finding an address and naming a pin on the phone. Made by `tools/build-place-cells.py` in the
  Press repository from download.openstreetmap.fr's Ireland extract of 7 Oct 2026 (TASK-1643).
  No postcodes or Eircodes are included.

- **The United Kingdom's road cells** are files in `roads/` (`roads/cells.json` lists them), 130 cells
  for Great Britain and Northern Ireland, cut from download.openstreetmap.fr's united_kingdom extract
  of 8 Oct 2026 by `tools/cut-road-regions.py` (with the Ireland extract for the cells across the North
  Channel). Cities whose whole-degree cell would outweigh any map a phone has been offered are cut
  into half-degree cells (`51.5_-0.5`). Press reads this list beside the release's, and a key in both
  is this one.
- **Great Britain's place files** are in `places/` beside Ireland's, with every Great Britain postcode
  at the point Ordnance Survey's Code-Point Open gives it. Northern Ireland's names are Ireland's files.

- **Map layers** are in `layers/` (`layers/layers.json` lists them), one per Irish road cell on the same
  key: the sea (from OpenStreetMap's land polygons), lakes, rivers, county lines and the names of
  counties, bays and big lakes, and every building, houses kept apart from other buildings. They are
  what Press's Roads map draws besides the roads (TASK-1720). Made by `tools/build-map-layers.py` in
  the Press repository from download.openstreetmap.fr's Ireland and Northern Ireland extracts of
  7-8 Oct 2026 and osmdata.openstreetmap.de's land polygons.
  **Great Britain's** are beside them (TASK-1723): one per cell in `roads/cells.json`, 122 files and 681 MB, cut
  from download.openstreetmap.fr's united_kingdom extract of 11 Oct 2026 with the land polygons. The five coastal
  cells Ireland and Great Britain share (52_-6, 53_-6, 54_-6, 55_-6, 55_-7) are cut over both countries, on Great
  Britain's larger boxes, and replace Ireland's; `layers/layers.json` lists all 145.

- **Building tiles** are in `buildings/` (`buildings/tiles.json` lists them with their sizes), for the map on a
  trader's website enquiry form, where a customer puts a pin on her house (TASK-3025). They are the map layers'
  buildings, unchanged, regrouped into tiles of 5 by 5 of the layers' 0.02° squares (0.1° a side), so her browser
  fetches about 20 KB to see one house rather than a whole cell. Named `<ti>_<tj>.json.gz`, where `ti` and `tj` are
  the square numbers divided by 5, rounded down. Made by `tools/cut-building-tiles.py` in the Press repository from
  `layers/` as of 24 Oct 2026: 5,089 tiles, 284 MB.

All of them are derived from OpenStreetMap and are offered under the Open Database Licence 1.0
(https://opendatacommons.org/licenses/odbl/1-0/). Credit: © OpenStreetMap contributors.

The postcodes in Great Britain's place files: Contains OS data © Crown copyright and database right 2026.
Contains Royal Mail data © Royal Mail copyright and database right 2026. Contains National Statistics data
© Crown copyright and database right 2026. Offered under the Open Government Licence v3.0
(https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
