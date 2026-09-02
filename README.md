One subfolder per approved phone model — `motorola/`, `samsung/`, `tecno/` (matching the phone rows in `catalog/catalog.csv`). Each phone folder now holds three files:

- `housing.stl` — phone clip housing
- `lens.stl` — lens barrel
- `diffuser.stl` — light diffuser

A new phone model added to the catalog gets its own folder here with the same three filenames.

**Universal parts** — the same physical part regardless of phone model, so each one only needs to exist once, in a shared `universal/` folder (not inside any phone folder):

- `universal/tray.stl` — specimen tray
- `universal/eppendorf-tray.stl` — Eppendorf tray

If you have old per-phone `tray.stl` files from an earlier version of this repo, they're no longer used and can be deleted — the site now always links to `universal/tray.stl` instead.
