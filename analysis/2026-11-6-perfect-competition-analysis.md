# Perfect Competition Analysis

## Where Does the Money Crop Stop, and Why?
Tomatoes generate the highest revenue per bed at $8,800. The model's marginal cost schedule shows that marginal cost rises as additional tomato beds are planted. The marginal cost curve crosses the tomato price line near 6 beds, showing where additional tomato production becomes less attractive.

The Tomato Marginal Cost schedule currently shows marginal cost crossing the tomato price of $8,800 between beds 5 and 6. Specifically, marginal cost at bed 5 is approximately $8,623, while marginal cost at bed 6 is approximately $9,812.

However, Solver selected 10 tomato beds in the optimal solution. Because a price-taking producer should continue production until price is approximately equal to marginal cost, this inconsistency suggests that either the marginal-cost schedule or the optimization model requires further review.

The workbook's Solver solution remains 10 tomato beds, but the marginal-cost schedule currently indicates that tomato production becomes uneconomic after approximately 5-6 beds.
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

My hypothesis underestimated the number of tomato beds. My original hypothesis predicted 7 tomato beds, while Solver selected 10 tomato beds. The marginal-cost schedule currently suggests tomato production becomes uneconomic between beds 5 and 6, which does not fully agree with the Solver solution. This indicates that additional investigation is needed to reconcile the marginal-cost schedule with the optimization results. The optimization process improved on my original estimate.

## Which Constraints Bind?
The tomato bed cap was not binding because the model selected 10 of the 20 available tomato beds.

The carrot bed cap was binding because the model selected all 20 available carrot beds.

The mesclun bed cap was binding because the model selected all 30 available mesclun beds.

The total bed constraint was not binding because the model used 60 of the 64 available beds, leaving 4 unused beds.

The labor constraint was not fully used because total labor remained below the 6,480-hour limit.

## Does Any Marginal Cost Curve Fall? 
The tomato marginal cost curve does not fall between beds 5 and 6. Marginal cost increases from approximately $8,623 at bed 5 to approximately $9,812 at bed 6.

The increase occurs because the labor requirement increases under the diminishing-returns labor function. As more tomato beds are planted, each additional bed requires more labor hours, causing marginal cost to rise.

The carrot marginal cost curve crosses the carrot price line near 10 beds. This supports the validation rule that carrots should reach P ≈ MC near 10 beds.

The marginal cost schedules show how costs change as production expands. Marginal cost increases because additional production requires more labor and resources, not because the crops themselves change physically. The behavior of the curves reflects the increasing labor required by the production process.

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
