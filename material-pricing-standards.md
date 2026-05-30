# Material Pricing Standards

## Purpose

This document defines how material prices are stored, updated, and used for cabinet and woodworking estimates.

The purpose of this system is to create a simple, AI-readable material pricing workflow that supports:

* Cabinet estimating
* Material cost forecasting
* Quote preparation
* Job costing
* Future automation
* Easy manual updates

The material price table is not expected to be perfectly accurate at first. It is intended to provide a consistent starting point that can be improved with real purchase data over time.

---

# Source Files

## Primary Material Price Table

The primary material pricing source is:

```text
material-price-table.csv
```

This CSV file stores estimated unit prices for common cabinet and woodworking materials.

The CSV should be treated as the first source to check when estimating material cost.

---

# Material Price Table Columns

The material price table should use the following columns:

| Column              | Purpose                                                                            |
| ------------------- | ---------------------------------------------------------------------------------- |
| item_id             | Unique ID used to reference the material                                           |
| category            | Broad material category                                                            |
| item_name           | Human-readable material name                                                       |
| description         | Short description of the material                                                  |
| size                | Material size or package size                                                      |
| unit                | Pricing unit such as sheet, each, pair, box, pack, gallon, quart, or linear_foot   |
| vendor              | Vendor or supplier name                                                            |
| estimated_unit_cost | Estimated cost per unit                                                            |
| cost_basis          | Explains whether the cost is estimated, quoted, receipt-based, or manually updated |
| last_updated        | Date the price was last updated                                                    |
| price_confidence    | Confidence level for the price                                                     |
| notes               | Notes about the material, source, or limitations                                   |

---

# Preferred Vendors

## Home Depot

Home Depot is the default vendor for commonly available materials and supplies.

Home Depot should be used for:

* Common cabinet plywood
* MDF
* Melamine
* Poplar boards
* Select pine
* Red oak boards
* Hardware
* Edge banding
* Screws
* Glue
* Sanding supplies
* Paint supplies
* General shop supplies

Home Depot purchase exports may be used for business expense tracking and receipt lookup.

If a Home Depot export contains only transaction summaries and does not include item-level detail, it should not be used as the only source for material unit prices.

---

## W&W Lumber

W&W Lumber may be used for higher quality plywood, special order sheet goods, or materials not reliably available from Home Depot.

W&W Lumber often has to quote material from their supplier before providing a final price.

When using W&W pricing:

* Use the most recent quote available.
* Mark `cost_basis` as `quoted`.
* Set `vendor` to `W&W Lumber`.
* Add quote notes in the `notes` column.
* Update `last_updated` to the quote date.

---

# Pricing Priority

When estimating material costs, use pricing sources in this order:

1. Exact item match in `material-price-table.csv`
2. Most recent supplier quote
3. Receipt-based price from actual purchase history
4. Manual estimate
5. Flag for review

Do not silently substitute materials when the exact material is missing.

If no suitable price is found, return:

```text
Manual Review Required
```

---

# Price Confidence Levels

Use the following confidence levels:

| Confidence | Meaning                                                           |
| ---------- | ----------------------------------------------------------------- |
| high       | Price is based on a recent receipt or supplier quote              |
| medium     | Price is based on a known vendor price that may need verification |
| low        | Price is a rough estimate or placeholder                          |
| review     | Price is missing, outdated, unclear, or needs manual review       |

---

# Cost Basis Values

Use the following `cost_basis` values:

| Cost Basis   | Meaning                                                   |
| ------------ | --------------------------------------------------------- |
| estimated    | Placeholder estimate used until actual pricing is entered |
| quoted       | Supplier quote, such as W&W Lumber                        |
| receipt      | Actual purchase price from receipt or purchase history    |
| manual       | Manually entered or adjusted price                        |
| online_check | Price checked online but not verified by purchase         |
| review       | Price needs manual review                                 |

---

# General Material Pricing Rules

## Rule 1: Use Exact Matches First

When estimating, search for the closest exact material match by:

* Item name
* Item ID
* Size
* Unit
* Vendor

Example:

```text
3/4 Maple Plywood
4 x 8 x 3/4 in
sheet
Home Depot
```

---

## Rule 2: Do Not Guess Premium Material Substitutions

Do not substitute lower-grade material for higher-grade material unless specifically instructed.

Examples:

* Do not substitute MDF for plywood.
* Do not substitute red oak plywood for maple plywood.
* Do not substitute paint-grade plywood for cabinet-grade plywood.
* Do not substitute unfinished plywood for prefinished plywood.

If the exact material is unavailable, flag it for review.

---

## Rule 3: Separate Material Price From Labor

Material pricing should not include labor.

Labor should be calculated separately using:

```text
labor-standards.md
```

---

## Rule 4: Separate Material Price From Markup

The material price table stores raw estimated material cost only.

Markup, overhead, profit, delivery, tax, and waste factors should be handled separately in estimating rules.

---

## Rule 5: Track Unit Clearly

Always respect the unit listed in the CSV.

Examples:

| Unit        | Meaning                   |
| ----------- | ------------------------- |
| sheet       | Price per sheet           |
| each        | Price per individual item |
| pair        | Price per pair            |
| box         | Price per box             |
| pack        | Price per pack            |
| gallon      | Price per gallon          |
| quart       | Price per quart           |
| linear_foot | Price per linear foot     |

---

# Plywood Pricing Rules

Plywood should be priced by sheet unless otherwise specified.

Common cabinet plywood should include:

* 3/4 Birch Plywood
* 3/4 Maple Plywood
* 3/4 Red Oak Plywood
* 3/4 Sande Plywood
* 3/4 Prefinished Maple Plywood
* 1/2 Birch Plywood
* 1/2 Maple Plywood
* 1/4 Birch Plywood
* 1/4 Maple Plywood
* 3/4 MDF
* 1/2 MDF
* 1/4 MDF
* 3/4 White Melamine
* 1/2 White Melamine

When plywood pricing is uncertain, estimate should clearly say:

```text
Plywood pricing should be verified before final quote.
```

---

# Purchase History Rules

Home Depot purchase history exports may be useful for:

* Tracking total spending
* Matching receipts to projects
* Finding invoice numbers
* Reviewing purchase dates
* Supporting expense tracking

Home Depot purchase history exports should only be used for material unit pricing if they include:

* Item name
* SKU or item number
* Quantity
* Unit price
* Total line cost

If the export only includes receipt totals or transaction summaries, use it for job costing support but not as a primary material price source.

---

# Estimating Output Requirements

When an AI agent uses material pricing, it should return:

* Item name
* Item ID
* Vendor
* Unit
* Estimated unit cost
* Quantity used
* Extended material cost
* Price confidence
* Cost basis
* Any missing information or manual review items

Example output:

| Item              | Item ID       | Vendor     | Unit  | Qty | Unit Cost | Extended Cost | Confidence |
| ----------------- | ------------- | ---------- | ----- | --: | --------: | ------------: | ---------- |
| 3/4 Maple Plywood | PLY-075-MAPLE | Home Depot | sheet |   2 |    $95.00 |       $190.00 | low        |

---

# Updating Prices

When updating prices manually:

1. Locate the matching `item_id`.
2. Update `estimated_unit_cost`.
3. Update `cost_basis`.
4. Update `last_updated`.
5. Update `price_confidence`.
6. Add notes if needed.

Do not change the `item_id` unless the item itself is being replaced or renamed.

---

# Future Improvements

Possible future improvements include:

* Add actual Home Depot SKU numbers
* Add W&W Lumber quote history
* Add item-level receipt imports
* Add supplier-specific price tables
* Add material waste factors
* Add sales tax rules
* Add markup rules
* Add automatic price aging warnings
* Add review flags for outdated prices

---

# Revision Notes

## Version 1.0

Initial material pricing standards created to support AI-readable cabinet and woodworking estimating.

The first version uses `material-price-table.csv` as the primary pricing source and assumes many prices are rough estimates until replaced with actual purchase or supplier quote data.

