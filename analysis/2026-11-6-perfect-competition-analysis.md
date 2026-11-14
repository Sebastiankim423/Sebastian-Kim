# Perfect Competition Analysis

## Where Does the Money Crop Stop, and Why?
Tomatoes generate the highest revenue per bed at $8,800. The current marginal cost schedule shows marginal cost rising from approximately $8,623 at bed 5 to approximately $9,812 at bed 6. This suggests that tomato production reaches the point where price is approximately equal to marginal cost between beds 5 and 6.

However, Solver selected 10 tomato beds as part of the optimal solution. Because a price-taking producer should continue production until price is approximately equal to marginal cost, this difference suggests that the marginal-cost schedule and optimization results should be examined further.

The optimization model selected 10 tomato beds, while the marginal-cost schedule suggests production becomes uneconomic after approximately 5-6 beds.
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

My hypothesis underestimated tomato production. However, the marginal-cost schedule currently indicates that tomato marginal cost exceeds price between beds 5 and 6, while the Solver solution includes 10 tomato beds. This inconsistency suggests that additional investigation of the marginal-cost schedule is needed.

## Which Constraints Bind?
The tomato bed cap was not binding because the model selected 10 of the 20 available tomato beds.

The carrot bed cap was binding because the model selected all 20 available carrot beds.

The mesclun bed cap was binding because the model selected all 30 available mesclun beds.

The total bed constraint was not binding because the model used 60 of the 64 available beds, leaving 4 unused beds.

The labor constraint was not fully used because total labor remained below the 6,480-hour limit.

The carrot and mesclun bed caps appear to be binding because Solver selects the maximum number of beds allowed for both crops.

To test the value of relaxing the constraints, I increased the mesclun bed cap from 30 to 31 and ran Solver again. Solver continued to select 30 mesclun beds, and the optimal solution did not change.

This suggests that an additional mesclun bed has a shadow price of approximately $0 and does not increase profit. Relaxing the mesclun cap would therefore provide little or no economic benefit.

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
