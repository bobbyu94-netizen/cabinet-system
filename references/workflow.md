# Cabinet Production Workflow (13 Stages)

**Owner:** Bobby Umphlette | **Version:** 1.0

## Pipeline Overview

Customer concept → Project requirements → Geometry definition → Customer rendering → Standards application → Cabinet geometry generation → Material calculation → Material optimization → Labor estimation → Proposal generation → Customer approval → Production package generation → Cabinet construction

## Stage Details

### Stage 1: Customer Concept Capture
- Gather: room type, cabinet types wanted, approximate sizes, finish preference, budget range
- Note: special conditions (wet area, corner units, appliance openings, ADA height)

### Stage 2: Project Requirements Validation
- Confirm standard vs. non-standard dimensions
- Flag any constraints (ceiling height, existing walls, plumbing locations)
- Establish face-frame vs. frameless (default: face-frame)

### Stage 3: Geometry Definition
- Convert requirements into specific cabinet dimensions (W × H × D per cabinet)
- Assign cabinet type codes (BASE, UPPER, PANTRY, VANITY, SINK, CORNER, DRAWER)

### Stage 4: Customer Rendering
- Describe or generate visual preview showing materials, finish, hardware style
- Get customer confirmation before proceeding to technical stages

### Stage 5: Standards Application
- Apply construction standards from `construction-standards.md`
- Document any project-specific overrides explicitly

### Stage 6: Cabinet Geometry Generation
- Calculate all part dimensions using formulas (no arbitrary values)
- Produce parts list: Name | Material | Width | Length | Qty

### Stage 7: Material Calculation
- Tally parts by material type
- Apply waste factors
- Convert to purchase units

### Stage 8: Material Optimization
- Group parts to minimize sheet waste
- Propose cutting layout narrative
- Flag oversized parts

### Stage 9: Labor Estimation
- Apply baseline hours per cabinet type
- Apply width and complexity multipliers
- Calculate total hours and cost

### Stage 10: Proposal Generation
- Line-item quote: materials + labor + consumables
- Labor rate already includes overhead and profit — do not add separately
- Flag low-confidence prices

### Stage 11: Customer Approval
- Present proposal
- Capture approval or revision requests
- Document any approved changes as project overrides

### Stage 12: Production Package Generation
- Generate cut list Excel file (see `cutlist-format.md`)
- Produce material purchase list
- Produce labor summary

### Stage 13: Cabinet Construction
- Shop follows cut list, purchase list, and assembly sequence
- Track actual hours vs. estimated for future calibration

## Design Principles

- Standards are separate from project overrides — never mix them
- Formula-based dimensions, not disconnected arbitrary values
- Printable production documents are the final deliverable
- Practical shop usability over analytical complexity
