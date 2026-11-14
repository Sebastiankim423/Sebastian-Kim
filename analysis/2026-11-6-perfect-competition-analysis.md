# Perfect Competition Analysis

## Where Does the Money Crop Stop, and Why?
Tomatoes generate the highest revenue per bed at $8,800. The Tomato Marginal Cost schedule shows marginal cost is approximately $8,248 at bed 10 and approximately $9,390 at bed 11.

Because the tomato price is $8,800, price is greater than marginal cost at bed 10 but lower than marginal cost at bed 11. This indicates that the profit-maximizing production level is approximately 10 tomato beds, where P ≈ MC.

This result is consistent with the Solver solution, which also selected 10 tomato beds.
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

My original hypothesis predicted 7 tomato beds, 20 carrot beds, and 30 mesclun beds. The optimization model found 10 tomato beds, 20 carrot beds, and 30 mesclun beds.My hypothesis underestimated tomato production. The corrected Tomato Marginal Cost schedule shows that marginal cost remains below the tomato price at bed 10 and exceeds the tomato price at bed 11. This explains why the optimal solution includes 10 tomato beds.

## Which Constraints Bind?
The tomato bed cap was not binding because the model selected 10 of the 20 available tomato beds.

The carrot bed cap was binding because the model selected all 20 available carrot beds.

The mesclun bed cap was binding because the model selected all 30 available mesclun beds.

The total bed constraint was not binding because the model used 60 of the 64 available beds, leaving 4 unused beds.

The labor constraint was not fully used because total labor remained below the 6,480-hour limit.

The carrot and mesclun bed caps appear to be binding because Solver selects the maximum number of beds allowed for both crops.

To evaluate the value of relaxing constraints, I increased the carrot bed cap from 20 to 21 and ran Solver again. The optimal solution did not change and Solver continued to select 20 carrot beds.

I then increased the mesclun bed cap from 30 to 31 and ran Solver again. The optimal solution again remained unchanged and Solver continued to select 30 mesclun beds.

Because neither change increased profit, both additional beds had a shadow price of approximately $0. This suggests that relaxing either cap would not increase profit under the current conditions.


This suggests that an additional mesclun bed has a shadow price of approximately $0 and does not increase profit. Relaxing the mesclun cap would therefore provide little or no economic benefit.

## Does Any Marginal Cost Curve Fall? 
The tomato marginal cost curve briefly falls between beds 5 and 6 before rising again.

Marginal cost decreases from approximately $7,660 at bed 5 to approximately $4,906 at bed 6. This change is not caused by tomatoes becoming physically easier to produce. Instead, it reflects a change in how labor costs are priced under the model's labor-cost assumptions.

This demonstrates that a marginal cost curve can be influenced by changes in both production requirements and input costs. After bed 6, marginal cost begins increasing again as diminishing returns continue to raise labor requirements.

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
