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

The required formulas are
1. TOMATO_LABOR_HRS(q) = q × TOMATO_HRS_PER_BED × WEEKS × (1 + TOMATO_DIM_PCT)^q
2. CARROT_LABOR_HRS(q) = q × CARROT_HRS_PER_BED × WEEKS × (1 + CARROT_DIM_PCT)^q
3. MESCLUN_LABOR_HRS(q) = q × MESCLUN_HRS_PER_BED × WEEKS × (1 + MESCLUN_DIM_PCT)^q
4. TOTAL_REVENUE = TOMATO_REVENUE + CARROT_REVENUE + MESCLUN_REVENUE
5. TOTAL_FERTILIZER_COST = TOMATO_FERTILIZER + CARROT_FERTILIZER + MESCLUN_FERTILIZER
6. PROFIT = TOTAL_REVENUE − TOTAL_FERTILIZER_COST − TOTAL_LABOR_COST − FIXED_COST
7. TOTAL_BEDS = TOMATO_BEDS + CARROT_BEDS + MESCLUN_BEDS
8. TOMATO_REVENUE = TOMATO_BEDS × TOMATO_REVENUE_PER_BED
9. CARROT_REVENUE = CARROT_BEDS × CARROT_REVENUE_PER_BED
10. MESCLUN_REVENUE = MESCLUN_BEDS × MESCLUN_REVENUE_PER_BED
11. TOMATO_FERTILIZER = TOMATO_BEDS × TOMATO_FERTILIZER_PER_BED
12. CARROT_FERTILIZER = CARROT_BEDS × CARROT_FERTILIZER_PER_BED
13. MESCLUN_FERTILIZER = MESCLUN_BEDS × MESCLUN_FERTILIZER_PER_BED
14. TOTAL_LABOR_HOURS = TOMATO_LABOR_HRS + CARROT_LABOR_HRS + MESCLUN_LABOR_HRS
15. PERMANENT_LABOR_HOURS = MIN(TOTAL_LABOR_HOURS, FARMER_HOURS)
16. TEMPORARY_LABOR_HOURS = MAX(0, TOTAL_LABOR_HOURS - FARMER_HOURS)
17. TEMP_WORKERS_REQUIRED = TEMPORARY_LABOR_HOURS / TEMP_WORKER_HOURS
18. TOTAL_LABOR_COST = (PERMANENT_LABOR_HOURS × FARMER_RATE) + (TEMPORARY_LABOR_HOURS × TEMP_WORKER_RATE)

## Validation Rules

- No #REF! errors
- No #DIV/0! errors
- No #NAME? errors
- Every calculated cell contains a formula
- Every input is a named range

### Solver Constraints 
- TOMATO_BEDS <= 20
- CARROT_BEDS <= 20
- MESCLUN_BEDS <= 30
- TOTAL_BEDS <= 64
- TEMP_WORKERS_REQUIRED <= 4
- TOMATO_BEDS must be an integer
- CARROT_BEDS must be an integer
- MESCLUN_BEDS must be an integer

 ### Optimization Objective
  - Maximize PROFIT

### Hand Check
- Tomato Labor at q = 1
- 1 × 2.5 × 36 × 1.10 = 99 hours

### Acceptable Criteria 
Optimal Mix
- Tomatoes = 10
- Carrots = 20
- Mesclun = 30
Total Beds
- 60 beds
Season Profit
- $42,762
Standalone P ≈ MC
- Tomatoes ≈ 10
- Carrots ≈ 10
- Mesclun ≈ 6

Temporary Workers
- Must not exceed 4 workers

## Outputs
- Optimal tomato beds
- Optimal carrot beds
- Optimal mesclun beds
- Total beds planted
- Total labor hours
- Permanent labor hours
- Temporary labor hours
- Temporary workers required
- Total labor dollars
- Blended labor rate
- Total revenue
- Total costs
- Season profit
- Tomato marginal-cost schedule
- Carrot marginal-cost schedule
- Mesclun marginal-cost schedule
- Constraint status/checks
- Validation/check results
