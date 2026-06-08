# Cut List Output Format Standards

## File Naming
`<width>x<height>-<type>-cut-list.xlsx`
Example: `36x34.5-base-cut-list.xlsx`

## Workbook Structure

Sheet order (mandatory):
1. **Summary** — material purchase summary (what to buy)
2. **3-4 Birch Parts** — 3/4" birch plywood cabinet box parts (sides, top, bottom, shelf, back)
3. **3-4 Birch Sheet Plan** — optimized cutting layout for 3/4" sheets
4. **1-2 Birch Parts** — 1/2" birch plywood drawer box parts (sides, front, back)
5. **1-4 Birch Parts** — 1/4" birch plywood drawer bottom parts
6. **1-4 MDF Door Panels** — 1/4" MDF door panel parts
7. **Poplar Parts** — face frame and door frame parts (solid lumber)
8. **Poplar Cut Plan** — board breakdown and offcut tracking

Calculation sheets (hidden from print output — do not show formulas in final output).

## Standard Sheet Layout (all sheets)

| Row | Content |
|---|---|
| 1 | Title (bold, 14pt) |
| 2 | Explanatory note (italic, 13pt) |
| 3 | Spacer (empty) |
| 4 | Column headers (bold, 14pt, light gray fill) |
| 5+ | Data rows (13pt, alternating white/very light gray) |

## Column Structures

### Summary Sheet
Part Name | Material | Qty | Unit | Unit Cost | Extended Cost | Vendor | Notes

**Standard line item order (always include these in this sequence):**
1. 3/4" Birch Plywood — sheet goods for cabinet box
2. 1/2" Birch Plywood — only if drawers present
3. 1/4" Birch Plywood — only if drawers present
4. 1/4" MDF — door panels
5. Poplar (1x8 or 1x10) — priced per board (show LF needed + board count in Notes)
6. Concealed Soft-Close Hinge — 2 per door
7. Hinge Mounting Plate — 1 per hinge (same qty as hinges)
8. Undermount Drawer Slide — only if drawers present (1 pair per drawer)
9. Shelf Pin 5mm — 4 per shelf
10. Cabinet Pull — 1 per door (and 1 per drawer if applicable)
11. Cabinet Leveler — 4 per base or vanity cabinet
12. Consumables (13%) — 13% of material subtotal, label as "Supplies", no vendor
13. **Total row** — bold, gray fill (#D9D9D9), Extended Cost column only, label "Total Material Cost", note "Low confidence — verify all prices"

Prices must be shown formatted as currency (e.g., $89.00) in Unit Cost and Extended Cost columns.

### 3-4 Birch Parts Sheet
Part Name | Width (in) | Length (in) | Qty | Material | Notes

- Back panel must always be row 1 (first data row)
- All parts listed individually, qty 1 each — no grouping (e.g., Left Side and Right Side are separate rows, not "Side × 2")
- Standard base cabinet row order: Back, Left Side, Right Side, Top, Bottom, Shelf

### 3-4 Birch Sheet Plan
Sheet # | Parts Nested | Sheet Used % | Waste % | Notes

### 1-2 Birch Parts Sheet
Part Name | Width (in) | Length (in) | Qty | Material | Notes

### 1-4 Birch Parts Sheet
Part Name | Width (in) | Length (in) | Qty | Material | Notes

### 1-4 MDF Door Panels Sheet
Part Name | Width (in) | Length (in) | Qty | Notes

### Poplar Parts Sheet
Part Name | Width (in) | Length (in) | Qty | Notes

### Poplar Cut Plan

The Poplar Cut Plan is a multi-phase sheet. Each phase has its own header and its own column structure. Do not use a single uniform column layout across the whole sheet.

**Sheet title:** "Poplar — Board Breakdown & Cut Plan"
**Note row:** "Stock: N× 1x10 × Xft  |  Planning width: 9.0"  |  [summary, e.g. 'All parts from 1 board']"

---

#### Phase 1 — Main Board Crosscuts

- **Phase header row:** fill #BFBFBF (dark gray), bold — text: "PHASE 1 — MAIN BOARD CROSSCUTS" — spans all columns
- **Column header row:** fill #D9D9D9, bold — columns: Section | Crosscut Length | Purpose
- **Data rows:** alternating white / #F2F2F2
  - Section: letter (A, B, C…)
  - Crosscut Length: **fractional inches** (e.g., 34-1/2" not 34.5")
  - Purpose: what parts will be ripped from this section
- **Remnant row** (if board has leftover after all sections): fill #EBF1DE (light green) — label "Remnant", approximate length, "Offcut"
- Empty spacer row after Phase 1 before Phase 2

---

#### Phase 2 — Rip All Sections

- **Phase header row:** fill #BFBFBF, bold — text: "PHASE 2 — RIP ALL SECTIONS"
- For each section (in order A, B, C…):
  - **Section sub-header:** fill #E8EEF4 (light blue-gray), bold — text: "Section X — 9.0" × [length in fractional inches]"
  - **Column header row:** fill #D9D9D9, bold — columns: Rip Width | Part Produced | Remaining Width
  - **Data rows:** alternating white / #F2F2F2
    - Rip Width: dimension (e.g., 1.5" or 3.0")
    - Part Produced: "✓ Part Name N" — checkmark (✓) prefix, part name, sequential number
    - Remaining Width: remaining board width after this rip (e.g., "7.375""), or for the final rip: "Offcut X: W × L" (e.g., "Offcut A: 5.75" × 34-1/2"")
  - Empty spacer row after each section before the next

---

#### Phase 3 — Offcut Crosscuts & Rips

- **Phase header row:** fill #BFBFBF, bold — text: "PHASE 3 — OFFCUT CROSSCUTS & RIPS"
- If no offcut work is needed, add one data row: "No offcut cuts required for this job"
- For each offcut being used (in order):
  - **Offcut sub-header:** fill #E8EEF4, bold — text: "Offcut X (W × L) — [what it will yield]"
  - **Column header row:** fill #D9D9D9, bold — columns: Action | Part Produced | Result
  - **Data rows:** alternating white / #F2F2F2
    - Action: what cut is being made (e.g., "Crosscut to 25"", "Rip 3.0"")
    - Part Produced: "✓ Part Name" or "—" for intermediate cuts
    - Result: remaining piece or note (e.g., "5.75" × 9-1/2" → Offcut A2")
  - **Scrap row** (when final offcut is too small to use): fill #FCE4D6 (peach) — label result as "X" scrap note (e.g., "1-3/4" — scrap (too short)")
  - Empty spacer row after each offcut group

---

#### Dimension Notation

- **Always use fractional inches** in the Poplar Cut Plan (not decimals)
  - 34.5" → 34-1/2"
  - 5.6875" → 5-11/16"
  - 23.25" → 23-1/4"
- Decimal notation is acceptable on other sheets (Poplar Parts, Birch Parts) but the Cut Plan must use fractions

## Formatting Rules

- Font: Arial, 13pt default, 14pt headers
- Fill: light grayscale for headers (printer-friendly — no dark fills)
- Orientation: landscape
- Paper: letter size
- Scaling: fit-to-width
- Text wrap: on for Notes columns
- Column widths: manually optimized (not auto-sized uniformly)

## Standard Cabinet Assumptions (unless specified)

**Base cabinets:**
- Standard base: 2 shaker doors (width ≥ 24") + **1 drawer with 6" face** + 1 shelf, face frame, box components
- Standard base (width < 24"): 1 shaker door + 1 drawer with 6" face + 1 shelf
- Drawer base: all drawers, no doors — must be explicitly requested
- Top: two 4" nailers (front and back), not a full top panel

**Upper cabinets:**
- Upper cabinet (width ≥ 24"): 2 shaker doors, 2 adjustable shelves, face frame, box components
- Upper cabinet (width < 24"): 1 shaker door, 2 adjustable shelves, face frame, box components
- Top: solid full panel (not nailers). No toe kick. No drawer.
- All box components sit between the sides, pocket screwed.

**All cabinet types:**
- **Flag any assumption** not explicitly covered by the spec — add a note to the Summary sheet Notes column

## Generating the Workbook

**Always start from the reference script:** `references/build_cutlist.py`

Read that file first. It is the canonical implementation of this format spec — column widths, fill colors, font sizes, row structure, and cut plan layout are all locked in there. Do not rewrite it from scratch. Modify it for the cabinet being built (dimensions, part counts, board assignments) and run it.

If the script does not yet exist or cannot be found, rebuild it from this spec exactly and save it back to `references/build_cutlist.py` when done.

Output must be a properly formatted .xlsx file. Do not produce a CSV.
