# Cabinet Production Workflow

version: 1.0
owner: Bobby Umphlette

---

# purpose

This document defines the high-level workflow used to move from:

* customer concept
  to
* completed cabinet production package.

The goal is to create a repeatable, AI-assisted cabinet production system capable of:

* interpreting sketches
* generating customer renderings
* applying cabinet standards
* generating material lists
* optimizing cut lists
* estimating costs and labor
* generating proposals
* producing shop-ready cut packages

This workflow is intended to evolve over time.

---

# workflow_pipeline

customer_concept
→ project_requirements
→ geometry_definition
→ customer_rendering
→ standards_application
→ cabinet_geometry_generation
→ material_calculation
→ material_optimization
→ labor_estimation
→ proposal_generation
→ customer_approval
→ production_package_generation
→ cabinet_construction

---

# stage_definitions

## 1_customer_concept

### inputs

* customer photos
* sketches
* verbal descriptions
* inspiration images
* dimensions

### outputs

* initial project scope
* rough dimensions
* design intent

### goals

* understand customer requirements
* identify missing dimensions
* identify environmental concerns
* identify material expectations

---

## 2_project_requirements

### required_information

* cabinet dimensions
* installation location
* moisture exposure
* countertop type
* finish requirements
* hardware preferences
* delivery/install requirements

### outputs

* validated project requirements
* project constraints
* project overrides

---

## 3_geometry_definition

### goals

Convert customer dimensions into:

* cabinet geometry
* openings
* door sizes
* drawer sizes
* material assumptions

### dependencies

* cabinet-system-standards.md

### outputs

* cabinet geometry package
* dimensional formulas
* validated cabinet dimensions

---

## 4_customer_rendering

### goals

Generate:

* photorealistic customer images
* material previews
* finish previews
* hardware previews

### outputs

* customer presentation images
* design approval visuals

---

## 5_standards_application

### goals

Apply:

* cabinet standards
* material standards
* construction rules
* project overrides

### dependencies

* cabinet-system-standards.md

### outputs

* finalized construction logic
* validated cabinet build rules

---

## 6_cabinet_geometry_generation

### goals

Generate:

* cabinet box parts
* face frame parts
* door parts
* drawer parts
* shelf parts

### outputs

* production dimensions
* part lists

---

## 7_material_calculation

### goals

Calculate:

* plywood requirements
* hardwood requirements
* hardware requirements
* finishing materials

### outputs

* material lists
* board counts
* sheet counts

---

## 8_material_optimization

### goals

Optimize:

* plywood usage
* hardwood usage
* cut sequencing
* offcut reuse

### optimization_priorities

1. workflow efficiency
2. waste reduction
3. repeatable cutting process

### outputs

* optimized cut lists
* optimized board breakdowns
* printable shop sheets

---

## 9_labor_estimation

### goals

Estimate:

* build time
* finishing time
* installation time
* delivery time

### outputs

* estimated labor hours
* labor cost estimate

---

## 10_proposal_generation

### goals

Generate:

* customer proposal
* pricing
* renderings
* scope of work

### outputs

* printable proposal
* customer approval package

---

## 11_customer_approval

### goals

* finalize scope
* finalize dimensions
* finalize materials
* finalize pricing

### outputs

* approved project

---

## 12_production_package_generation

### goals

Generate:

* printable cut lists
* material purchase lists
* optimized cutting workflow
* assembly guidance

### outputs

* shop-ready production package

---

## 13_cabinet_construction

### goals

Use generated production package to:

* order materials
* build components
* assemble cabinets
* finish cabinets
* install cabinets

---

# long_term_automation_goals

future_system_capabilities:

* sketch interpretation
* automated geometry extraction
* automated cabinet generation
* automatic formula application
* automatic cut optimization
* material price integration
* automated labor estimation
* proposal generation
* CNC integration
* project archiving
* reusable cabinet templates

---

# important_design_principles

* standards should remain separate from project overrides
* dimensions should derive from formulas
* avoid disconnected magic-number dimensions
* optimize for real-world workflow efficiency
* generated outputs should prioritize shop usability
* printable production documents are the final deliverable
* cabinet logic should remain reusable across projects

---

# current_system_state

completed_or_working:

* photorealistic render generation
* cabinet standards documentation
* cabinet formula logic
* face frame formulas
* shaker door formulas
* project override structure
* print-friendly cut list generation
* poplar optimization logic
* plywood geometry logic

currently_in_development:

* automated cabinet geometry generation
* reusable cabinet templates
* project-driven automation
* cost estimation refinement
* workflow scaling

future_targets:

* sketch-to-production automation
* fully automated proposal generation
* CNC-ready file generation
* fully parametric cabinet generation
