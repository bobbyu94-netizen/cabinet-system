# Cut List Output Standards

version: 1.0
owner: Bobby Umphlette

---

# purpose

This document defines the formatting, layout, readability, and print-output standards for all generated cabinet production cut lists.

The primary goal is to create:

* clean
* readable
* printer-friendly
* shop-optimized

production documents.

These standards are intended to create consistent output across all future cabinet projects and AI-generated production packages.

---

# output_philosophy

Cut lists are production documents.

The output should prioritize:

1. shop usability
2. readability
3. workflow efficiency
4. print consistency
5. material organization

The cut list is intended to function as:

* a shop traveler
* a build reference
* a cutting workflow guide

The output should NOT prioritize:

* spreadsheet complexity
* visible formulas
* engineering-style calculation sheets
* decorative formatting

---

# workbook_structure

preferred_workbook_type:

* print_only

calculation_sheets:

* excluded_from_final_output

visible_logic:

* minimized

final_output_goal:

* printable_shop_sheets_only

---

# worksheet_structure

organization_method:

* one_material_per_sheet

preferred_sheet_order:

1. material_summary
2. plywood_parts
3. plywood_optimization
4. hardwood_parts
5. hardwood_optimization
6. hardware_summary
7. finishing_summary

sheet_naming_rules:

* short
* readable
* print-friendly

example_sheet_names:

* PLYWOOD
* POPLAR
* HARDWARE
* SUMMARY

---

# exact_workbook_format

The required Excel workbook output must follow this exact print-only workbook structure unless the user specifically requests a different format.

| Sheet Order | Sheet Name | Purpose |
| ---: | --- | --- |
| 1 | Summary | Material purchase summary |
| 2 | 3-4 Birch Parts | Final 3/4 inch birch plywood cabinet box parts (sides, top, bottom, shelf, back) |
| 3 | 3-4 Birch Sheet Plan | Rough 3/4 inch plywood sheet breakdown and optimized cutting plan |
| 4 | 1-2 Birch Parts | 1/2 inch birch plywood drawer box parts (sides, front, back) |
| 5 | 1-4 Birch Parts | 1/4 inch birch plywood drawer bottom parts |
| 6 | 1-4 MDF Door Panels | 1/4 inch MDF shaker door center panels |
| 7 | Poplar Parts | Final poplar face frame and door rail/stile parts |
| 8 | Poplar Cut Plan | Optimized poplar board breakdown |

Do not use slash characters in Excel sheet names. Use `3-4 Birch Parts`, not `3/4 Birch Parts`.

## standard_sheet_layout

Every worksheet must follow this row structure:

| Row | Content |
| ---: | --- |
| 1 | Sheet title |
| 2 | Short note explaining assumptions, exclusions, workflow, or review items |
| 3 | Blank spacer row |
| 4 | Table headers |
| 5+ | Table data |

## summary_sheet_format

The `Summary` sheet must use these columns:

| Column | Header |
| --- | --- |
| A | Material |
| B | Purchase Qty |
| C | Used For |
| D | Notes |

Column width guidelines:

| Column | Width |
| --- | ---: |
| A | 24 |
| B | 16 |
| C | 36 |
| D | 38 |

## three_quarter_birch_parts_sheet_format

The `3-4 Birch Parts` sheet is for final part dimensions, not rough sheet breakdowns.

The sheet must use these columns:

| Column | Header |
| --- | --- |
| A | Cab |
| B | Part |
| C | Qty |
| D | Width |
| E | Ht/Len |
| F | Depth |
| G | Formula / Notes |

Column width guidelines:

| Column | Width |
| --- | ---: |
| A | 12 |
| B | 18 |
| C | 7 |
| D | 12 |
| E | 12 |
| F | 12 |
| G | 42 |

## three_quarter_birch_sheet_plan_format

The `3-4 Birch Sheet Plan` sheet is for rough sheet breakdown and optimized cutting sequence.

The sheet must use these columns:

| Column | Header |
| --- | --- |
| A | Sheet |
| B | Order |
| C | Rough Section |
| D | Parts Produced |
| E | Final Size |
| F | Qty |
| G | Why This Cut |

Column width guidelines:

| Column | Width |
| --- | ---: |
| A | 12 |
| B | 8 |
| C | 20 |
| D | 32 |
| E | 18 |
| F | 8 |
| G | 42 |

## one_quarter_mdf_door_panels_sheet_format

The `1-4 MDF Door Panels` sheet is for 1/4 inch MDF shaker door center panels only. In wet area cabinets, use 1/4 inch birch plywood instead.

The sheet must use these columns:

| Column | Header |
| --- | --- |
| A | Cab |
| B | Part |
| C | Qty |
| D | Width |
| E | Height |
| F | Formula / Notes |

Column width guidelines:

| Column | Width |
| --- | ---: |
| A | 12 |
| B | 24 |
| C | 8 |
| D | 14 |
| E | 14 |
| F | 46 |

## poplar_parts_sheet_format

The `Poplar Parts` sheet includes final poplar parts for face frames and shaker door rails/stiles.

The sheet must use these columns:

| Column | Header |
| --- | --- |
| A | Category |
| B | Part |
| C | Qty |
| D | Length |
| E | Width |
| F | Formula / Notes |

Column width guidelines:

| Column | Width |
| --- | ---: |
| A | 24 |
| B | 22 |
| C | 8 |
| D | 14 |
| E | 12 |
| F | 42 |

## poplar_cut_plan_format

The `Poplar Cut Plan` sheet is for optimized poplar board breakdown and offcut tracking.

The sheet must use these columns:

| Column | Header |
| --- | --- |
| A | Board |
| B | Order |
| C | Length |
| D | Rip Parts From Section |
| E | Width Used |
| F | Offcut |
| G | Status |

Column width guidelines:

| Column | Width |
| --- | ---: |
| A | 14 |
| B | 8 |
| C | 12 |
| D | 36 |
| E | 14 |
| F | 20 |
| G | 30 |

---

# required_cut_list_behavior

When a user asks for an optimized cabinet cut list, the expected output is a downloadable Excel `.xlsx` workbook.

Rules:

* Do not return only a markdown table unless the user explicitly asks for a chat-only cut list.
* Use the exact workbook sheet structure documented in this file.
* Read `cabinet-system-standards.md` before creating the cut list.
* Read `material-usage-standards.md` when material quantity assumptions are needed.
* Standard upper cabinets should include two shaker doors unless the user says otherwise.
* Standard upper cabinets should include face frame parts, door parts, 3/4 inch plywood box parts, 3/4 inch plywood back, and 1/4 inch MDF door panels.
* Standard base cabinets should include face frame parts, door/drawer parts when applicable, 3/4 inch plywood box parts, 3/4 inch plywood back, 1/2 inch birch drawer box parts, 1/4 inch birch drawer bottoms, 1/4 inch MDF door panels, and integrated toe kick rules from `cabinet-system-standards.md`.
* Do not omit doors from a standard cabinet cut list unless the user explicitly says doors are excluded.

---

# file_naming_rules

Use this naming pattern:

`<width>x<height>-<cabinet-type>-cut-list.xlsx`

Examples:

* `26x30-standard-upper-cabinet-cut-list.xlsx`
* `36x34-5-standard-base-cabinet-cut-list.xlsx`

---

# review_warnings

The generated workbook summary or response should warn when:

* dimensions are inferred from a sketch
* depth is not shown and standard depth is assumed
* door overlay is assumed
* number of shelves is assumed
* material thickness is assumed
* a project override may apply
* the cut list is preliminary and should be verified before cutting

---

# print_settings

page_orientation:

* landscape

paper_size:

* standard_letter

fit_to_page:

* fit_width_to_single_page

height_scaling:

* automatic

margins:

* moderate

header_spacing:

* compact

footer_spacing:

* compact

page_break_behavior:

* avoid_unnecessary_page_breaks

---

# font_rules

font_family:

* Arial

default_font_size:

* 13

header_font_size:

* 14

minimum_font_size:

* 11

font_priority:

* readability_over_density

---

# color_and_fill_rules

preferred_fill_style:

* light_grayscale

avoid:

* dark_fills
* heavy_saturation
* ink_heavy_backgrounds

header_style:

* light_fill
* bold_text

table_style:

* printer_friendly

---

# column_width_rules

column_width_behavior:

* manually_optimized

rules:

* do_not_uniformly_auto_size_columns
* columns_should_match_content_type
* narrow_columns_for_quantity_fields
* medium_columns_for_dimensions
* wider_columns_for_notes
* wrap_long_text_instead_of_expanding_sheet_width

preferred_goal:

* maximize_printable_information_density_without_hurting_readability

---

# row_height_rules

row_behavior:

* auto_adjust_when_wrapped

header_rows:

* slightly_taller

data_rows:

* compact_but_readable

---

# text_wrapping_rules

wrap_text:

* enabled_when_beneficial

always_wrap:

* notes
* optimization_comments
* instruction_text
* long_headers

avoid_wrap_when_possible:

* dimensions
* quantities
* short identifiers

---

# table_layout_rules

preferred_layout:

* simple_flat_tables

avoid:

* excessive_merged_cells
* decorative_spacing
* oversized_titles
* unnecessary_blank_rows

table_priorities:

1. readability
2. cut_workflow_efficiency
3. print_efficiency

---

# optimization_output_rules

optimization_sections_should_include:

* material_type
* board_or_sheet_count
* optimized_cut_sequence
* reusable_offcuts
* scrap_identification

optimization_notes:

* concise
* wrapped
* readable_in_shop_environment

offcut_rules:

* offcuts_under_1.5_inches_are_scrap

---

# shop_usage_rules

documents_should_be:

* readable_from_distance
* printable_on_standard_printer
* usable_with_dirty_hands
* understandable_without_screen_zoom

preferred_usage_environment:

* woodworking_shop
* assembly_area
* cutting_station

---

# long_term_system_direction

future_outputs_should_support:

* automated_cut_packages
* AI-generated_production_documents
* cabinet_build_packets
* CNC-prep_documents
* install_documents

The final generated output should resemble:

* a professional production traveler
  more than
* a complex engineering spreadsheet.

---

# important_design_principles

* readability_over_maximum_density
* workflow_efficiency_over_visual_complexity
* printability_over_decorative_design
* consistency_across_projects
* generated_output_should_require_minimal_manual_cleanup
