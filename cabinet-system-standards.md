# Cabinet System Standards

version: 1.0
owner: Bobby Umphlette
units: imperial
default_material_thickness: 0.75
standard_construction: face_frame
frameless_construction: non_standard_override_only
standard_upper_height: 30 inches
standard_upper_depth: 12 inches

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
poplar_1x10_planning_width: 9.0
poplar_1x8_planning_width: 7.0
poplar_width_note: actual boards vary — use planning width to avoid mid-job shortages

default_saw_kerf: 0.125

default_overlay: 0.5

default_back_reveal: 0.25

visible_interior_finish: clear_coated

standard_construction: face_frame
frameless_construction: non_standard_override_only
standard_upper_height: 30 inches
standard_upper_depth: 12 inches

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

cabinet_back_material:
material: birch_plywood
thickness: 0.75
finish: clear_coated_interior

face_frame_material:
material: poplar

standard_construction:
type: face_frame

frameless_construction:
type: non_standard_override_only

standard_upper_dimensions:
height: 30 inches
depth: 12 inches

door_material:
material: poplar

door_panel_material:
material: mdf
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
door_panel_wet_area_override: birch_plywood_0.25

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

step_1: survey_all_parts — list every poplar part (width x length) before cutting
step_2: crosscut_to_length_first — miter cut to part length, starting with longest part
step_3: rip_for_width — extract maximum same-width parts from that section
step_4: track_kerf — deduct 0.125 per rip from remaining width
step_5: track_offcuts — record width and length of any remaining piece >= 1.5 wide
step_6: evaluate_all_material — at each decision, check remaining board and all offcuts for best utilization
step_7: crosscut_offcuts_as_needed — when using an offcut for a shorter part, crosscut first; remaining length is also an offcut if >= 1.5 wide

kerf: 0.125
minimum_usable_width: 1.5
scrap_threshold: below_1.5_width

offcut_states:
  offcut: width >= 1.5, no remaining use in project — record dimensions only
  scrap: width < 1.5 — not tracked

width_check_rule: offcut_width >= part_width + 0.125 kerf required to yield that part

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

standard_cabinet_construction:
face_frame_required: true
frameless_allowed_by_default: false

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

panel_formula:
formula: door_width - 5.25 (width), door_height - 5.25 (height)
note: 5.25 = (2 x 3.0 stile) - (2 x 0.375 tenon)

panel_capture_method:
type: groove

overlay: 0.5 (all exposed sides)

center_gap_double_door:
total: 0.125
per_door_deduction: 0.0625

door_height_gap: none

single_door_formula:
applies_when: cabinet_width < 24
door_width: opening_width + 1.0
door_height: opening_height + 1.0

double_door_formula:
applies_when: cabinet_width >= 24
each_door_width: (opening_width / 2) + 0.5 - 0.0625
door_height: opening_height + 1.0

---

# cabinet_box_rules

## upper_cabinet

overall_dimensions:
reference_type: finished_exterior_dimensions
standard_height: 30 inches
standard_depth: 12 inches
standard_construction: face_frame

side_depth_formula:
formula: overall_depth - face_frame_thickness

back_panel_rules:
material_thickness: 0.75
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
standard_construction: face_frame

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
