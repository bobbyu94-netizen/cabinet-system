# Material Pricing Standards

## Primary Data Source
`material-price-table.csv` (in the GitHub repo) is the single authoritative source for all material prices. `price-table.md` is a human-readable summary kept in sync with the CSV — update the CSV first, then update `price-table.md` to match.

## Vendor Defaults
- **Home Depot** — default for plywood, hardware, edge banding, shop supplies
- **W&W Lumber** — specialty items, higher-grade sheet goods (requires quote, marked as "quoted")

## Lookup Rules

1. **Exact match required** — match by item name, size, unit, and vendor before substituting
2. **No silent substitution** — if an item isn't in the table, flag it for manual review; do not guess
3. **No premium material downgrading** — do not substitute lower-grade alternatives without explicit instruction
4. **Labor excluded** — material pricing never includes labor or profit
5. **Unit clarity** — respect specified units: sheets, each, pairs, linear feet, board feet

## Confidence Levels
- `high` — based on receipt or confirmed quote
- `medium` — online check or recent estimate
- `low` — rough estimate, needs verification before quoting
- `review` — flagged, do not use without manual confirmation

All items in the current price table are marked `low` confidence (estimated 5/29/2026). Flag this to the customer: *"Pricing is based on estimated current costs — confirm with supplier before final quote."*

## Applying Prices to Estimate

1. Look up each material in the price table
2. Multiply unit cost × quantity (with waste factor from estimating-standards)
3. Sum all material lines
4. Add 13% consumables on top of material subtotal
5. Present each line with: Item | Qty | Unit | Unit Cost | Extended | Confidence | Vendor
