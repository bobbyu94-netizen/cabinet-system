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
