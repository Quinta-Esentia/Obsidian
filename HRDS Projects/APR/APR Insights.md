[[Linear Regression Ideas]]


Results to refine:
1. All Rio model (PG, LV2 seems appropriate, try lvl 1 but has less data)
2. Specific model for each PG

What's to refine:
1. Pick a "best" model for each split. 
2. Choose a fixed set of features, fit models (Rio and PG split) with those fixed features. This might be preffered for comparitive purposes when interpreting the results for different splits - even though the model accuracy score might be lower, model assumptions not as nicely met, and some features in the model might not be statistically significant. 

What to include in results:
1. Model summary
2. Example predictions using a reasonable range of feature values to give a more concrete example of how the model relates CuEq to the HR metrics. 