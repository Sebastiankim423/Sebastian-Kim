# Perfect Competition Analysis

## Where Does the Money Crop Stop, and Why?
Tomatoes generate the highest revenue per bed at $8,800. The model's marginal cost schedule shows that marginal cost rises as additional tomato beds are planted. The marginal cost curve crosses the tomato price line near 6 beds, showing where additional tomato production becomes less attractive.

Despite this crossing, the optimization model selected 10 tomato beds because the solution considers all farm constraints and crop interactions rather than marginal cost alone.

## Tomato Marginal Cost Curve

<img width="1653" height="993" alt="image" src="https://github.com/user-attachments/assets/ec3a0fd5-cd8a-4d30-b406-36aff4048d2d" />

- The tomato marginal cost curve crosses the tomato price line near 6 beds.

## Carrot Marginal Cost Cruve

<img width="1653" height="993" alt="image" src="https://github.com/user-attachments/assets/290252e9-95d0-48fe-8b83-d3d9c2ea03ed" />

- The carrot marginal cost curve crosses the carrot price line near 10 beds.

## Comparison with Initial Hypothesis

My original hypothesis predicted: 
- Tomatoes = 7
- Carrots = 20
- Mesclun = 30

The Solver model found: 
- Tomatoes = 10
- Carrots = 20
- Mesclun = 30

My hypothesis underestimated the number of tomato beds. The model showed that additional tomato production could be profitable while remaining within the farm's constraints. The optimization process improved on my original estimate.

## Which Constraints Bind?
The tomato bed cap was not binding because the model selected 10 of the 20 available tomato beds.

The carrot bed cap was binding because the model selected all 20 available carrot beds.

The mesclun bed cap was binding because the model selected all 30 available mesclun beds.

The total bed constraint was not binding because the model used 60 of the 64 available beds, leaving 4 unused beds.

The labor constraint was not fully used because total labor remained below the 6,480-hour limit.

## Does Any Marginal Cost Curve Fall? 
The Tomato Marginal Cost curve crossed the tomato price line near 6 beds.

The Carrot Marginal Cost curve crossed the carrot price line near 10 beds.

These crossing points support the principle that production should continue until price is approximately equal to marginal cost (P ≈ MC).

As production increases, diminishing returns cause marginal cost to rise.

The marginal cost schedules show changes in cost as production increases. The shape of the curves is caused by the labor equation and diminishing returns. As more beds are planted, labor requirements grow and marginal costs increase.

Marginal cost does not change because the crops become physically different. Instead, the cost changes because additional production requires more labor and resources.

## Would Each Crop Make Money on Its Own? 
If the full fixed cost were assigned to a single crop, that crop might not make a profit on its own. However, the planting decision is based on marginal cost rather than fixed cost.

Fixed costs must be paid regardless of whether one more bed is planted. Therefore, the decision to plant another bed should compare price to marginal cost rather than price to average total cost.

## Recommendation 
The recommended planting strategy is:

- 10 Tomato Beds
- 20 Carrot Beds
- 30 Mesclun Beds

This combination produces the highest profit while satisfying labor, bed, and crop-cap constraints.

The model produced a season profit of approximately $42,775.
