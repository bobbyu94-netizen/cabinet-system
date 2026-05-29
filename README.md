# Bobby Cabinet System

## Purpose

This repository contains the construction standards, dimensional formulas, workflow logic, optimization rules, and project-specific overrides used in Bobby's cabinetry workflow.

The primary goal is to develop a repeatable, formula-driven cabinet system that can eventually support:

* automated cut lists
* material optimization
* cabinet configuration logic
* estimating workflows
* CNC preparation
* AI-assisted design/build packages

This repository is intended to separate:

* permanent cabinet-building logic
  from
* temporary project-specific decisions.

---

# Core Philosophy

The system prioritizes:

* durability over minimal material savings
* repeatable logic over arbitrary dimensions
* workflow efficiency while still reducing waste
* formula-driven dimensions instead of disconnected values
* practical real-world shop workflows

All critical dimensions should derive from:

* parent dimensions
* construction standards
* or reusable formulas

---

# Workflow Priorities

## Plywood Workflow

1. Break down full sheets using track saw first
2. Convert sheets into manageable sections
3. Perform final dimensioning at table saw
4. Prioritize grain direction on visible surfaces
5. Optimize for workflow efficiency, not only theoretical yield

## Poplar Workflow

1. Crosscut longest finished lengths first
2. Group similar lengths together
3. Joint and plane batches together
4. Perform final rip widths last
5. Treat offcuts under 1.5" wide as scrap
6. Reuse usable offcuts whenever practical

---

# Construction Standards

## Face Frames

* Standard width: 1.5"
* Standard overlay: 0.5"
* Bottom rail may extend below cabinet box to align with cabinet interior floor

### Rail Formula

Rail length = overall cabinet width - left stile - right stile

---

## Shaker Doors

* 5-piece construction
* Standard rail/stile width: 3"
* Tenon allowance: 0.375" per side
* Panel oversize allowance: 0.3125" per side

### Rail Formula

Rail length = door width - stile widths + tenon allowances

### Panel Formula

Panel size = visible opening + groove allowance on all sides

---

# Material Standards

## Cabinet Boxes

* Unfinished birch plywood
* Full 3/4" backs
* Visible interiors clear coated

## Face Frames / Doors / Trim

* Poplar

## Drawer Boxes

* 1/2" birch plywood
* 1/4" bottoms in dado

## Wet Area Projects

* Avoid MDF
* Use moisture-resistant base systems
* Seal vulnerable lower edges

---

# Cabinet Configuration Logic

## Standard Base Cabinet

* Toe kick integrated into side panel geometry
* No cabinet height deduction for toe kick

## Wet Area / Elevated Base Cabinet

* Cabinet sits on independent moisture-resistant platform
* Hidden base height deducted from cabinet box height
* Used for garage or wet-floor applications

---

# Automation Goals

Long-term system goals:

* Formula-driven cabinet generation
* Parametric cabinet sizing
* Automated cut lists
* Material optimization
* AI-assisted project generation
* Sketch-to-build workflows
* Reusable project overrides

The goal is to eventually allow AI systems to:

1. Read cabinet standards
2. Analyze project dimensions/sketches
3. Generate optimized build packages automatically
