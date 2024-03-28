[[Linear Regression Ideas]]

[[APR 2022]]
[[APR 2023]]

The statistical interpretation for a multiple linear regression coefficient (B) for variable (X) is: 
	_an increase in X by one unit is associated with an increase in Y of B when all other variables in the model are held constant._

# Things to check:

## CuEq: does LV1 == sum(LV2)?
1. Check Lv1 CuEq equals to the sum of Lv2 CuEq etc. Perhaps it is better to fit an all Rio model to Lv1 even if there is less data/rows?

# Next Steps Part 2
- [x] Predicted vs actual plots over time
- [x] Predictor "effect size" on Response plots (linear over predictor range)
- [x] Predictor value plots over 
	1. Get model vars
	2. Loop over model vars
	3. Plot model var vs Calday



Interpret the combination of these three with the model summary output to get a story for each model. 

# Next Steps Part 1

## Results to refine:
1. All Rio model (PG, LV2 seems appropriate, try lvl 1 but has less data)
2. Specific model for each PG

## What's to refine:
1. Pick a "best" model for each split. 
2. Choose a fixed set of features, fit models (Rio and PG split) with those fixed features. This might be preffered for comparitive purposes when interpreting the results for different splits - even though the model accuracy score might be lower, model assumptions not as nicely met, and some features in the model might not be statistically significant. 

## What to include in results:
1. Model summary
2. Example predictions using a reasonable range of feature values to give a more concrete example of how the model relates CuEq to the HR metrics. 


# Business interpretation of insights
[[Contacts and SMEs]]
