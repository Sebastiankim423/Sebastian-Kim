# Farm Marginal Analysis Model Specification

## Inputs

### Farm Inputs

- WEEKS = 36
- FIXED COST = $20,000
- TOTAL_BEDS = 64
- FARMER_HOURS = 720
- TEMP_WORKERS_MAX = 4
- TEMP_WORKER_HOURS = 1440
- TEMP_WORKER_RATE = $17.36/hr
- FARMER_RATE = $34.72/hr

### Tomatoes
- BED_CAP = 20
- REVENUE_PER_BED = $8,800
- HRS_PER_WEEK_PER_BED = 2.5
- FERTILIZER_PER_BED = $880
- DIM_PCT = 10%

### Carrots
- BED_CAP = 20
- REVENUE_PER_BED = $2,094
- HRS_PER_WEEK_PER_BED = 0.833
- FERTILIZER_PER_BED = $440
- DIM_PCT = 2.5%

### Mesclun
- BED_CAP = 30
- REVENUE_PER_BED = $2,700
- HRS_PER_WEEK_PER_BED = 1.25
- FERTILIZER_PER_BED = $880
- DIM_PCT = 1.25%

## Model Structure

The workbook will contain an Inputs section identifying all farm-level
and crop-level assumptions.

The workbook will contain a Cost Structure section calculating total
labor requirements, permanent labor, temporary labor, total labor cost,
and the blended labor rate.

The workbook will contain marginal-cost schedules for Tomatoes, Carrots,
and Mesclun showing production quantity and marginal cost at each
quantity.

The workbook will contain an Optimization section containing the three
crop bed decisions, total revenue, total cost, season profit, and all
model constraints.

The workbook will contain a Checks section that verifies the model
against the stated acceptance criteria.

## Calculation Logic

## Validation Rules

## Outputs
