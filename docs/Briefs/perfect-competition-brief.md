---
type: brief
engagement: perfect-competition 
capability: marginal analysis
date: 2026-09-07
status: committed
hypothesis: "Mesclun-heavy mix with most remaining beds allocated to carrots"
---

# <Engagement> — Engagement Brief

## The Problem 

The farm owns a small 1.5-acre market garden with 64 beds and limited labor. Before the 36-week growing season starts, the farm must decide how many beds to dedicate to tomatoes, carrots, and mesclun. Once those decisions are made, they cannot be changed during the season. The goal is to make the most profit while staying within the limits on land and labor. The farm also has a $20,000 fixed cost for the season that must be covered before the farm earns a profit. The decision is difficult because planting more of a crop makes it less efficient and more expensive to manage. The farm needs to find the best mix of crops that earns the most money without exceeding the 64 available beds or the total labor hours available over the 36-week season.
## What is Fixed, What Can Be Chosen, and What Limits the Choice? 

The market prices, production costs, season length, available labor, total beds, and crop bed caps are all fixed. The only factor the farmer can choose is how many beds to dedicate to tomatoes, carrots, and mesclun. The goal is to find the right combination of crops that will maximize profits. The farmer's decisions are limited by the amount of land, labor, and crop space available. The farm has only 64 beds, each crop has a maximum number of beds that can be planted, and labor hours in the 36-week season are limited. Costs also increase as more beds of the same crop are planted due to diminishing returns.

## What I Am Assuming

I am assuming that the prices, labor, fertilizer cost, and diminishing return rates are correct and will stay the same for the 36-week season. I am also assuming that all the crops produced can be sold at the listed prices.  If I had more time, I would test how changes in available labor hours and diminishing returns affect total profit because either one could change the best crop mix.

## Hypothesis

For my hypothesis, I would say the farm should use all 7 tomato beds, 20 beds of carrots, and 30 beds of mesclun. I would have 7 empty beds left. 

## Reasoning

I would use 7 tomato beds because tomatoes make the most starting revenue at $8,800 per bed. Next, I would use 30 beds for mesclun because mesclun makes $2,700 per bed, compared with $2,094 for carrots, and has the lowest diminishing return rate at 1.25%, compared with 2.5% for carrots and 10% for tomatoes. I would also use 20 carrot beds to take advantage of the remaining labor and land available. Labor is an important constraint because the farm only has 6,480 labor hours available for the 36-week season. Because of the labor restriction, I would leave 7 beds empty instead of trying to use all 64 beds. Therefore, my hypothesis is that 7 tomato beds, 20 carrot beds, and 30 mesclun beds will provide a good balance between revenue and the farm’s limited resources. I will use Solver to determine whether this combination is the optimal solution and stays within all of the farm’s constraints.

Finally, I will subtract the $20,000 fixed cost from the total crop profit to determine the farm's actual seasonal profit.

Labor cost = rate × 36 × (1 + rate)^q

- Mesclun: 30 beds x 2.5 labor hours per bed = 75 hours
 
- Carrots: 12 beds x 0.833 labor hours per bed = 9.996 hours
 
- Tomatoes: 20 beds x 1.25 labor hours per bed = 25 hours
 
- Total labor hours = 80 + 9.996 +  = 109.996 hours

## How I Would Know I Was Wrong

I would know my plan was wrong if the optimization model found that a different combination of crops makes more profit. For example, I would be wrong if it is better to use fewer than 20 tomato beds, more than 12 carrot beds, fewer than 30 mesclun beds, or leave some beds empty. The labor limit, $20,000 fixed cost, and diminishing returns could also make another combination more profitable than my proposed 20 tomato, 12 carrot, and 30 mesclun bed plan.
