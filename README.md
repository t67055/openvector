# OpenVector

Community build guide and bill-of-materials for a VectorCam devices.

The live build guide lives at a Claude Artifact page. This repo is the data source behind it: the parts catalog, reference PDFs, and STL files. The page fetches directly from this repo, so pushing a file here is how you update the live site.

## Structure

```
catalog/
  catalog.csv          bill-of-materials — one row per part (see schema below)
docs/
  tool-specifications.pdf
  assembly-instructions.pdf
  printing-specifications.pdf
stl/
  motorola/             one folder per approved phone model
    housing.stl
    lens.stl
    tray.stl
    diffuser.stl
  samsung/
    ...
  tecno/
    ...
```

## catalog.csv schema

`id, category, item, spec, unit, cost, href, qtyPerUnit`

- `id` — stable slug, don't change once set (the site may reference it)
- `category` — one of `phone`, `hardware`, `filament`, `lab`
- `item` — display name
- `spec` — short spec string (many rows are still `placeholder` — fill in as real specs are confirmed)
- `unit` — the purchasable unit ("pack of 5", "1kg spool", "device", ...)
- `cost` — price of one `unit`, in USD, as a plain number
- `href` — product link. Amazon links are the only marketplace populated so far; leave `#` if there's no link yet (an item with `#` is simply left out of the live order table/cart, by design)
- `qtyPerUnit` — how many `unit`s one finished device consumes (can be a fraction, e.g. `0.18` spools of filament per device)

Rows with a blank/malformed field (missing category, spec, etc.) will get flagged rather than guessed at — fill in every column before it's picked up.

## Adding PDFs or STL files

Drop the file into `docs/` or the right `stl/<phone-model>/` folder using the filenames above and push. The live page links directly to these files by path, so once the file is in the repo it's live — nothing else to do.

## License

TBD — add a `LICENSE` file at the repo root (MIT and CC-BY-4.0 are both common choices for hardware/build-guide projects like this).
