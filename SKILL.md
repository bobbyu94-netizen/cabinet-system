---
name: cabinet-system
description: >
  Bobby Umphlette's cabinet shop production system. Use this skill whenever the user asks about cabinets, cut lists, cabinet quotes, cabinet materials, cabinet labor, face frames, shaker doors, drawer boxes, estimating a cabinet job, generating a cut list Excel file, or producing a shop production package. Even if the user just says "build me a base cabinet" or "quote this kitchen" or "what material do I need" — trigger this skill. It drives the full 13-stage workflow from customer concept → shop-ready cut list, applying Bobby's exact construction standards automatically.
---

# Cabinet System Skill

This skill encodes Bobby Umphlette's complete cabinet production system. Your job is to take a customer cabinet request and walk it through the workflow stages below, applying the construction standards to produce accurate, shop-ready outputs.

## Reference Files

Load these as needed — don't load all of them at once:

| File | When to load |
|---|---|
| `references/construction-standards.md` | Always — core rules for every cabinet |
| `references/workflow.md` | When planning stages or the user wants to understand the process |
| `references/cutlist-format.md` | When generating a cut list Excel file |
| `references/estimating.md` | When producing a quote or estimate |
| `references/labor.md` | When calculating labor hours or cost |
| `references/material-usage.md` | When calculating material quantities |
| `references/material-pricing.md` | When looking up or applying material costs |
| `references/price-table.md` | When you need actual unit prices |
| `references/build_cutlist.py` | When generating a cut list Excel file — read and modify this script, do not rewrite from scratch |

---

## Core Workflow

The production system has 13 stages. Move through them in order, but adapt to what the user actually needs — if they hand you a fully specified cabinet, skip the early discovery stages.

### Stage 1–3: Capture & Define
- Ask for: cabinet type (base/upper/pantry/vanity), width, height, depth (use standards if omitted), finish (painted/stained), wet area (yes/no), special conditions
- Validate against standard dimensions from `references/construction-standards.md`
- Flag any non-standard overrides explicitly

### Stage 4: Customer Rendering (optional)
- Describe the cabinet visually in text if the user wants a preview before proceeding
- Note finish, hardware, door style

### Stage 5–6: Apply Standards & Generate Geometry
**Read `references/construction-standards.md` now.**

Apply these rules to calculate all part dimensions:
- Box: birch plywood, 3/4" thick. Cabinet width is measured to the outside of the face frame.
  - Back width = cabinet width - 2×(3/4" sides) - 2×(1/4" reveal) = cabinet width - 2". Applies to all cabinet types.
  - Top, bottom, and shelf width = back width (all dependent on back dimensions).
  - Base cabinet bottom depth = side depth − 3/4" (back panel) = cabinet depth − 1-1/2". Upper cabinet top/bottom depth = cabinet depth − 3/4" (face frame) − 3/4" (back panel) = cabinet depth − 1-1/2". Both resolve to the same formula — the bottom panel cannot extend behind the back panel or past the face frame.
  - Side height = full cabinet height. Side depth = cabinet depth - 3/4" (face frame).
  - Back height = cabinet height - 2×(3/4") top and bottom panels.
  - Back material = 3/4" birch (structural, face frame construction).
- Face frame: poplar, 1.5" wide stiles, 1.5" wide rails. Overlay: 1/2" on all sides.
- Doors: 5-piece shaker, 3" rail/stile, panel = 1/4" MDF (not birch). Doors are overlay — they are LARGER than the opening, not smaller. Single door (width < 24"): door = opening + 1" each axis. Double door (width ≥ 24"): each door width = (opening / 2) + 1/2" hinge-side overlay - 1/16" center gap; door height = opening height + 1". Panel = door dimension - 5.25" each axis. See `references/construction-standards.md` for full formula.
- Drawer boxes: 1/2" birch sides/front/back, 1/4" birch bottom. Width = opening - slide clearance (1" total for undermount).
- Shelves: 3/4" birch, width = back width (cabinet width - 2"), depth = side depth - 2".

All dimensions must be derived from formulas, not guessed. Show your math.

### Stage 7: Material Calculation
**Read `references/material-usage.md`.**

- Tally all parts by material type (3/4" birch, 1/2" birch, 1/4" birch, 1/4" MDF, poplar)
- Apply waste factors: plywood 10–15%, poplar 15%
- Convert to purchase units (sheets, linear feet)

### Stage 8: Material Optimization
- Group parts by sheet type and propose a cutting layout narrative (which parts share sheets)
- Flag any parts that require a dedicated sheet due to size

### Stage 9: Labor Estimation
**Read `references/labor.md`.**

- Apply standard hours per cabinet type and width factor
- Apply complexity multipliers if applicable (painted finish, specialty hardware, inset doors, wet area)
- Total hours × $65/hr default rate

### Stage 10–11: Proposal / Quote
**Read `references/estimating.md` and `references/material-pricing.md`.**

- Materials: use price table values, apply waste, add consumables (13% of material subtotal)
- Labor: hours × rate (rate already includes overhead and profit — do not add separately)
- Present as a clean quote summary

### Stage 12: Cut List (Excel)
**Read `references/cutlist-format.md`.**

Use the xlsx skill to generate the cut list workbook. The workbook must follow the exact sheet order and formatting spec in `references/cutlist-format.md`. File name: `<width>x<height>-<type>-cut-list.xlsx`.

### Stage 13: Production Package
- Summarize: cut list file, material purchase list, labor hours, quote total
- Note any overrides or special instructions for the shop

---

## Key Rules (always apply)

- **Formula-driven, not arbitrary.** Every dimension must be derived. Show the calculation.
- **Wet area override.** When wet area = yes: use water-resistant plywood base, seal lower edges. Door panels revert to 1/4" birch (no MDF in wet areas).
- **Frameless is non-standard.** Default is always face-frame construction unless user explicitly overrides.
- **Poplar for visible wood.** Face frames and doors are poplar. Box interiors are birch plywood.
- **Standard hardware.** Undermount soft-close drawer slides, concealed soft-close hinges unless specified otherwise.
- **Durability over material savings.** When in doubt, use more material, not less.
- **Flag missing info.** Never silently substitute materials or dimensions. Ask or flag for review.

---

## Quick Reference: Standard Dimensions

| Cabinet Type | Standard Width | Standard Height | Standard Depth |
|---|---|---|---|
| Base | 12–48" (3" increments) | 34.5" | 24" |
| Upper | 12–48" (3" increments) | 30" | 12" |
| Pantry | 18–36" | 84–96" | 24" |
| Vanity | 18–48" | 34.5" | 21" |

Material thickness default: 3/4" (0.75").
