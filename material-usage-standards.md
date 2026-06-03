# Material Usage Standards

## Purpose

This document defines rough material usage allowances for cabinet and woodworking estimates.

These standards are intended to help create quick estimates before a final optimized cut list is available.

The values in this document are preliminary estimating allowances. They should be replaced or refined when actual project dimensions, cut lists, supplier quotes, or purchase data are available.

---

# Source Files Used With This Document

This document works with:

| File                            | Purpose                                           |
| ------------------------------- | ------------------------------------------------- |
| `cabinet-system-standards.md`   | Cabinet construction rules and material standards |
| `material-pricing-standards.md` | Material pricing rules                            |
| `material-price-table.csv`      | Material unit costs                               |
| `labor-standards.md`            | Labor hours and labor cost rules                  |
| `estimating-standards.md`       | Overall estimating workflow                       |

---

# General Rules

## Use These Allowances Only for Preliminary Quotes

Use these material allowances when:

* A quick cabinet quote is needed
* An optimized cut list is not available
* Exact project drawings are not complete
* The customer needs a budgetary estimate

Do not treat these allowances as final production cut lists.

---

## Use Actual Cut Lists When Available

If an actual optimized cut list exists for the project, use the optimized cut list instead of these rough allowances.

The optimized cut list should override this document for material quantities.

---

## Do Not Silently Substitute Materials

Use the materials listed in this document unless the user or project override specifies otherwise.

If a material is missing from `material-price-table.csv`, flag it for review.

Return:

```text
Manual Review Required
```

---

# Default Cabinet Material Assumptions

Unless project-specific overrides exist, use these material assumptions:

* Standard cabinets use face frame construction.
* Cabinet backs use 3/4 Birch Plywood, item ID `PLY-075-BIRCH`.
* 1/4 Birch Plywood is used only for drawer bottoms, shaker door panels, and project-specific thin panels unless otherwise specified.

| Cabinet Component            | Default Material             | Pricing Item ID       |
| ---------------------------- | ---------------------------- | --------------------- |
| Cabinet box parts            | 3/4 Birch Plywood            | PLY-075-BIRCH         |
| Shelves                      | 3/4 Birch Plywood            | PLY-075-BIRCH         |
| Cabinet backs                | 3/4 Birch Plywood            | PLY-075-BIRCH         |
| Drawer boxes                 | 1/2 Birch Plywood            | PLY-050-BIRCH         |
| Drawer bottoms               | 1/4 Birch Plywood            | PLY-025-BIRCH         |
| Face frames                  | Poplar                       | POP-1X2-8 / POP-1X3-8 |
| Shaker door rails and stiles | Poplar                       | POP-1X3-8             |
| Shaker door panels           | 1/4 MDF                      | PLY-025-MDF           |
| Edge banding                 | Birch Edge Banding           | EDGE-BIRCH-075        |
| Hinges                       | Soft Close Concealed Hinge   | HINGE-SC-FRAMLESS     |
| Drawer slides                | Soft Close Drawer Slide Pair | SLIDE-22-SC           |
| Pulls                        | Basic Cabinet Pull           | PULL-5IN-BASIC        |
| Glue                         | Wood Glue                    | GLUE-TB3-16           |
| Screws                       | Cabinet Screws               | SCREW-CAB-250         |

---

# Standard Base Cabinet Material Allowances

## Standard Base Cabinet Assumptions

Unless otherwise specified, a standard base cabinet assumes:

* 24 inch depth
* 34.5 inch height
* Face frame construction
* CNC cut cabinet box
* 3/4 inch birch plywood cabinet back
* 1 drawer
* 2 doors
* 1 adjustable shelf
* Standard soft close hardware
* Standard shaker fronts
* Painted exterior
* Clear-coated or finished interior
* No countertop
* No installation material
* No specialty inserts

These allowances are rough preliminary estimating values and are not final optimized cut lists.

---

## Base Cabinet Width Allowance Table

Use this table for rough material estimating before an optimized cut list exists.

3/4 Birch Plywood values include: 2 sides, top, bottom, shelf, and 3/4 back. Formula: 1,604 + (W - 2) × 100.75 sq in ÷ 4,608 × 1.15 waste. 1/2 Birch and 1/4 Birch are per standard drawer (multiply by drawer count). 1/4 MDF is for door panels.

| Cabinet Width | 3/4 Birch Plywood | 1/2 Birch Plywood | 1/4 Birch Plywood | 1/4 MDF | Poplar 1x3 8 ft | Birch Edge Banding | Hinges | Drawer Slide Pairs |  Pulls |
| ------------: | ----------------: | ----------------: | ----------------: | ------: | --------------: | -----------------: | -----: | -----------------: | -----: |
|     12 inches |        0.65 sheet |        0.06 sheet |        0.05 sheet | 0.02 sheet |         1 board |       12 linear_ft | 2 each |             1 pair | 2 each |
|     18 inches |        0.80 sheet |        0.07 sheet |        0.08 sheet | 0.04 sheet |         1 board |       16 linear_ft | 2 each |             1 pair | 2 each |
|     24 inches |        0.95 sheet |        0.08 sheet |        0.11 sheet | 0.04 sheet |        2 boards |       20 linear_ft | 4 each |             1 pair | 3 each |
|     30 inches |        1.10 sheet |        0.09 sheet |        0.14 sheet | 0.07 sheet |        2 boards |       24 linear_ft | 4 each |             1 pair | 3 each |
|     36 inches |        1.25 sheet |        0.10 sheet |        0.17 sheet | 0.10 sheet |        2 boards |       28 linear_ft | 4 each |             1 pair | 3 each |
|     42 inches |        1.41 sheet |        0.11 sheet |        0.20 sheet | 0.12 sheet |        3 boards |       32 linear_ft | 4 each |             1 pair | 3 each |
|     48 inches |        1.56 sheet |        0.12 sheet |        0.24 sheet | 0.15 sheet |        3 boards |       36 linear_ft | 4 each |             1 pair | 3 each |

---

# Standard Upper Cabinet Material Allowances

## Standard Upper Cabinet Assumptions

Unless otherwise specified, a standard upper cabinet assumes:

* 30 inch height
* 12 inch depth
* Face frame construction
* CNC cut cabinet box
* 2 adjustable shelves
* 3/4 inch cabinet back
* Standard soft close hinges
* Standard shaker doors
* Painted exterior
* Clear-coated or finished interior
* No crown molding
* No lighting
* No glass doors
* No installation material
* No specialty inserts

## Upper Cabinet Width Allowance Table

Use this table for rough material estimating before an optimized cut list exists.

3/4 Birch Plywood values include: 2 sides, top, bottom, shelf, and 3/4 back. Formula: 675 + (W - 2) × 60.25 sq in ÷ 4,608 × 1.15 waste. 1/4 MDF is for door panels.

| Cabinet Width | 3/4 Birch Plywood | 1/4 MDF | Poplar 1x3 8 ft | Birch Edge Banding | Hinges | Pulls |
| ------------: | ----------------: | ------: | --------------: | -----------------: | -----: | ----: |
|     12 inches |        0.32 sheet | 0.02 sheet |         1 board |       10 linear_ft | 2 each | 1 each |
|     18 inches |        0.41 sheet | 0.02 sheet |         1 board |       12 linear_ft | 2 each | 1 each |
|     24 inches |        0.50 sheet | 0.05 sheet |        2 boards |       16 linear_ft | 4 each | 2 each |
|     30 inches |        0.59 sheet | 0.08 sheet |        2 boards |       20 linear_ft | 4 each | 2 each |
|     36 inches |        0.68 sheet | 0.11 sheet |        2 boards |       24 linear_ft | 4 each | 2 each |
|     42 inches |        0.77 sheet | 0.14 sheet |        3 boards |       28 linear_ft | 4 each | 2 each |
|     48 inches |        0.86 sheet | 0.17 sheet |        3 boards |       32 linear_ft | 4 each | 2 each |

Notes:

* These allowances are preliminary estimating values only.
* They include a 3/4 inch back.
* They assume standard face frame construction.
* They should be replaced by an optimized cut list when actual project drawings are available.

---

# Hardware Allowance Rules

## Doors

Use the following rough hinge allowance:

| Door Count |            Hinges |
| ---------: | ----------------: |
|     1 door |          2 hinges |
|    2 doors |          4 hinges |
|  Tall door | 3 hinges per door |

---

## Drawers

Use the following drawer hardware allowance:

| Drawer Count | Drawer Slide Pairs |
| -----------: | -----------------: |
|     1 drawer |             1 pair |
|    2 drawers |            2 pairs |
|    3 drawers |            3 pairs |
|    4 drawers |            4 pairs |

---

## Pulls and Knobs

Use the following default hardware allowance:

| Opening Type               | Pulls / Knobs |
| -------------------------- | ------------: |
| Door                       |        1 each |
| Drawer                     |        1 each |
| Wide drawer over 30 inches |        2 each |

---

# Consumables Allowance

Consumables should be estimated separately from the raw material list.

Use this rough allowance unless a project-specific override exists:

| Consumable Category      | Estimating Rule     |
| ------------------------ | ------------------- |
| Screws                   | 3% of material cost |
| Glue                     | 2% of material cost |
| Sandpaper                | 3% of material cost |
| General shop consumables | 5% of material cost |

Default total consumables allowance:

```text
13% of material cost
```

This is a rough allowance and should be refined with actual project tracking.

---

# Finish Material Allowance

Paint and finishing supplies are not included in the standard base or upper cabinet material tables unless specifically requested.

For rough cabinet finishing estimates, use:

| Finish Item      | Estimating Rule            | Pricing Item ID           |
| ---------------- | -------------------------- | ------------------------- |
| Primer           | 0.25 gallon per cabinet (2 coats)    | PRIMER-GAL                |
| Cabinet paint    | 0.25 gallon per cabinet (2 coats minimum)    | PAINT-CAB-GAL             |
| Caulk            | 0.25 tube per cabinet      | CAULK-PAINTABLE           |
| Wood filler      | 0.10 container per cabinet | FILLER-WOOD               |
| Sanding supplies | Include in consumables     | See consumables allowance |

For painted cabinets, also apply the painted finish labor rules from `labor-standards.md`.

---

# Poplar Rip Yield Standards

Poplar parts are ripped from full-width boards. Do not treat each part as requiring its own linear foot — calculate how many parts fit across the board face, then determine board LF needed.

## Rip Yield from 1x10 (9.25" face)

| Part Type | Rip Width | Parts per LF of Board |
| --------- | --------- | --------------------: |
| Face frame stiles/rails | 1.5" | 6 |
| Door rails/stiles | 3.0" | 3 |
| Drawer front frame | 3.0" | 3 |

## Rip Yield from 1x8 (7.25" face)

| Part Type | Rip Width | Parts per LF of Board |
| --------- | --------- | --------------------: |
| Face frame stiles/rails | 1.5" | 4 |
| Door rails/stiles | 3.0" | 2 |
| Drawer front frame | 3.0" | 2 |

## Calculation Method

1. List all poplar parts with their lengths and rip widths
2. Group by rip width (1.5" face frame vs. 3.0" door/drawer)
3. For each group: sum total linear inches needed
4. Divide by parts-per-LF for the chosen board width → LF of board required per group
5. Sum all groups → total raw LF
6. Apply 15% waste factor → purchase LF
7. Convert to board count using 10ft default board length

## Example — 48" Base Cabinet, 1x10 Stock

Face frame parts (1.5" rip, 6 per LF):
- 2 stiles × 34.5" = 69"
- 3 rails × 45" = 135"
- Total: 204" ÷ 6 = 34" = 2.83 LF of board

Door parts (3.0" rip, 3 per LF), 2 doors at 22.25"W × 23.75"H:
- 4 stiles × 23.75" = 95"
- 4 rails × 22.25" = 89"
- Total: 184" ÷ 3 = 61.3" = 5.11 LF of board

Raw total: 2.83 + 5.11 = 7.94 LF × 1.15 waste = **9.13 LF → 1 × 10ft board**

---

# Installation Material Allowance

Installation materials are not included in the standard cabinet material allowance unless specifically requested.

For rough installation estimating, use:

| Installation Item | Estimating Rule       |
| ----------------- | --------------------- |
| Cabinet screws    | 0.10 box per cabinet  |
| Shims             | 0.25 pack per cabinet |
| Caulk             | 0.25 tube per cabinet |
| Touch-up supplies | Manual review         |

---

# Material Usage Output Requirements

When an AI agent estimates cabinet material cost, it should return:

* Cabinet type
* Cabinet width
* Material item
* Item ID
* Vendor
* Unit
* Quantity used
* Unit cost
* Extended cost
* Price confidence
* Cost basis
* Any manual review items

Example output:

| Item              | Item ID       | Vendor     | Unit  |  Qty | Unit Cost | Extended Cost |
| ----------------- | ------------- | ---------- | ----- | ---: | --------: | ------------: |
| 3/4 Birch Plywood | PLY-075-BIRCH | Home Depot | sheet | 0.75 |    $85.00 |        $63.75 |
| 1/2 Birch Plywood | PLY-050-BIRCH | Home Depot | sheet | 0.25 |    $60.00 |        $15.00 |
| 1/4 Birch Plywood | PLY-025-BIRCH | Home Depot | sheet | 0.25 |    $35.00 |         $8.75 |
| 1x3 Poplar        | POP-1X3-8     | Home Depot | each  |    2 |    $18.00 |        $36.00 |

---

# Quote Calculation Rules

For preliminary cabinet quotes:

1. Read cabinet type and width.
2. Find the matching cabinet in this file.
3. Get material quantities from the usage table.
4. Get material unit costs from `material-price-table.csv`.
5. Calculate material extended cost.
6. Add consumables allowance if requested.
7. Get labor hours from `labor-standards.md`.
8. Get labor cost using the labor rate in `labor-standards.md`.
9. Return material cost, labor cost, and total estimated cost.
10. Clearly label the result as a preliminary quote.

---

# Rounding Rules

Use the following rounding rules:

* Material quantities: use listed quantity unless project override exists
* Unit costs: display to nearest cent
* Extended costs: calculate from unrounded values and display to nearest cent
* Labor hours: follow `labor-standards.md`
* Labor cost: follow `labor-standards.md`
* Total estimate: display to nearest cent

---

# Known Limitations

These allowances are not optimized cut lists.

They do not account for:

* Exact nesting
* Grain direction
* Defects
* Damaged material
* Offcut inventory
* Job-specific drawer sizes
* Non-standard openings
* Specialty hardware
* Appliance openings
* Tall panels
* Finished end panels
* Decorative trim
* Delivery or installation conditions

Use actual project drawings and optimized cut lists for final production.

---

# Future Improvements

Possible future improvements include:

* Add pantry cabinet usage allowances
* Add drawer base usage allowances
* Add sink base usage allowances
* Add finished end panel rules
* Add face frame linear foot formulas
* Add door and drawer front formulas
* Add waste factor rules
* Add offcut inventory tracking
* Add CSV version for machine-readable material usage

---

# Revision Notes

## Version 1.0

Initial material usage standards created for preliminary cabinet quoting.

The first version focuses on standard base and upper cabinets and uses rough material allowances until optimized cut lists are available.
