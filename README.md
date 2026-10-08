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

Both are derived from OpenStreetMap and are offered under the Open Database Licence 1.0
(https://opendatacommons.org/licenses/odbl/1-0/). Credit: © OpenStreetMap contributors.

The postcodes in Great Britain's place files: Contains OS data © Crown copyright and database right 2026.
Contains Royal Mail data © Royal Mail copyright and database right 2026. Contains National Statistics data
© Crown copyright and database right 2026. Offered under the Open Government Licence v3.0
(https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
