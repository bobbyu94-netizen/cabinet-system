# Cabinet System Standards

version: 1.0
owner: Bobby Umphlette
units: imperial
default_material_thickness: 0.75

---

# system_goals

* formula_driven_dimensions
* repeatable_construction_logic
* workflow_optimized_cutlists
* reusable_project_overrides
* ai_assisted_build_generation
* sketch_to_build_workflows
* automated_material_estimation
* automated_cut_optimization

---

# global_rules

minimum_usable_offcut_width: 1.5

default_saw_kerf: 0.125

default_overlay: 0.5

default_back_reveal: 0.25

visible_interior_finish: clear_coated

construction_priority_order:

* durability
* workflow_efficiency
* waste_reduction
* visual_consistency

---

# material_standards

cabinet_box_material:
material: birch_plywood
thickness: 0.75
finish: clear_coated_interior

face_frame_material:
material: poplar

door_material:
material: poplar

door_panel_material:
material: birch_plywood
thickness: 0.25

drawer_box_material:
material: birch_plywood
thickness: 0.5

drawer_bottom_material:
material: birch_plywood
thickness: 0.25

wet_area_rules:
avoid_mdf: true
use_water_resistant_base: true
seal_lower_edges: true

---

# workflow_rules

## plywood_workflow

sequence:

* track_saw_breakdown
* manageable_sections
* table_saw_final_dimensioning

optimization_priority:

* workflow_efficiency
* grain_direction
* material_yield

---

## poplar_workflow

sequence:

* longest_crosscuts_first
* grouped_length_batches
* joint_and_plane_batches
* final_rip_widths_last

offcut_rules:
minimum_usable_width: 1.5
reusable_offcuts: true

---

# joinery_rules

preferred_joinery_order:

* pocket_screws_hidden
* brad_nails_fill_and_sand
* glue_and_clamps

glue_type: titebond_3

drawer_joinery:
bottom_dado_depth: 0.25
assembly_method:
- glue
- clamps

---

# face_frame_rules

face_frame_width: 1.5

bottom_rail_extension:
enabled: true
default_extension: 0.75

rail_formula:
formula: overall_width - left_stile - right_stile

---

# door_rules

door_style: five_piece_shaker

rail_stile_width: 3.0

tenon_allowance_per_side: 0.375

panel_oversize_per_side: 0.3125

rail_formula:
formula: door_width - stile_width_x2 + tenon_allowance_x2

panel_formula:
formula: visible_opening + groove_allowance_all_sides

panel_capture_method:
type: groove

---

# cabinet_box_rules

## upper_cabinet

overall_dimensions:
reference_type: finished_exterior_dimensions

side_depth_formula:
formula: overall_depth - face_frame_thickness

back_panel_rules:
placement: between_sides
width_formula:
formula: overall_width - material_thickness_x2 - side_reveal_x2

top_bottom_rules:
width_formula:
formula: back_panel_width

depth_formula:
formula: overall_depth - face_frame_thickness - back_material_thickness

side_and_back_height_rule:
same_height: true

---

## base_cabinet_standard

toe_kick_type: integrated

height_formula:
formula: overall_height - countertop_thickness

toe_kick_height_deduction:
enabled: false

construction_method:
same_as_upper_cabinet: true

---

## base_cabinet_wet_area_override

override_type: project_specific

base_type: elevated_water_resistant_platform

hidden_base_height:
default: 4.0

height_formula:
formula: overall_height - countertop_thickness - hidden_base_height

toe_kick_height_deduction:
enabled: true

construction_method:
same_as_upper_cabinet: true

---

# hardware_preferences

drawer_slides:
type: undermount_soft_close

hinges:
type: concealed_soft_close

---

# finishing_rules

primer:
type: bin_shellac

topcoat_application:
type: graco_sprayer

visible_interiors:
finish: clear_coated

exteriors:
finish: painted

---

# optimization_logic

dimension_strategy:
avoid_magic_numbers: true
prefer_formula_driven_dimensions: true

material_strategy:
reuse_offcuts_first: true
optimize_board_width_usage: true

cutting_strategy:
prioritize_longest_parts_first: true

---

# project_overrides

garage_cabinet_project:
wet_area_override: true
elevated_base: true
vented_drawers: true
clear_coated_interiors: true