# press-road-cells
OpenStreetMap road network cells for Press. Data (c) OpenStreetMap contributors, ODbL 1.0.

- **Road cells** are the assets of the `road-cells-v1` release (`cells.json` lists them), made by
  `tools/build-road-graph.mjs` in the Press repository.
- **Place files** are in `places/` (`places.json` lists them), one per road cell on the same key:
  townlands with their outlines and counties, towns and villages, named streets and house numbers,
  for finding an address and naming a pin on the phone. Made by `tools/build-place-cells.py` in the
  Press repository from download.openstreetmap.fr's Ireland extract of 7 Oct 2026 (TASK-1643).
  No postcodes or Eircodes are included.

Both are derived from OpenStreetMap and are offered under the Open Database Licence 1.0
(https://opendatacommons.org/licenses/odbl/1-0/). Credit: © OpenStreetMap contributors.
