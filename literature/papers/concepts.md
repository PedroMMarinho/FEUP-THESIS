
Feature selection has three families:

- Filter: Does not need a trained model. Uses a statistical scoring (e.g correlation) for choosing the most important features. 
- Wrapper: Trains a model with different feature subsets with the objective of getting the most performant model. Generaly very expensive. 
- Embedded: The model selects features while it trains. Does not need to retrain the model every time.


Some keywords I should know:

**Overfitting**: the model does well on the training data but badly on new data.
**Generalization**: performance of the model in unseen test data.
**Epistasis**: Interaction between genes.

Difference between GA and GP:

**Genetic Algorithms(GA):** Evolutionary search to get the most "fitest", meaning the best features/combination of feature subsets, using crossover and mutation of generations over each iteration. This can be represented as a bit string using 0's and 1's where 1 means use this feature/subset of features. The fitness (best answer) is how well a model performs in a subset. This means that this is a wrapper style approach.

**Genetic Programming(GP):** Same idea as the genetic algorithm, but instead of using features, we use formulas represented as trees, e.g (x3 + 1) * x4. Features selected are the ones that appear in the final formula that holds. This is used so as to find a formula that fits/is closest to the data. (E.g lets say target is y, the formula that can compute the value that is closest to the ground truth of y is the best formula). For SR(Symoblic Regression) this is used as an embedded method.

**Shapley Values(SHAP):** Is used to split fairly a team payout among players according to each of their contribution. Each contribution is averaged around all of the possible combinations with other features. This turns computation time costly but if we filter before hand a large number of features might be feasible to use.

**LIME Values:** Explains *one* prediction of a black-box model. It creates many different copies of one instance (randomly switching features off), gets the black-box prediction for each, weights them by similarity to the original, and fits a simple linear model on them. The linear model's coefficients = how much each feature pushed this specific prediction. Local (valid only near that instance), model-agnostic (only needs predictions), and non-deterministic (random sampling → results vary between runs).


**Wang 2025** talks about how we can use GP with Shapley values as a way to get the best features, using a regression approach. How it works, GP is computed after that we compute shapley values, and select the log2(n) with n being the number of features that the formula computed from the GP generated. Interesting idea to have about how to use Shapley values and GP. Something that showed me interest is that we can optimize this by doing the GP while also calculating the Shapley values (better in terms of faster runtimes).

**Rodrigues 2024 SLUG(SeLection Using Genetic algorithms and genetic programming)**: GAMETES is used as an artificial data generator. It basically generates hundreds or even thousands of features where only 3 are relevant. This and more can be easily changed using that tool. 
GA is used to reduce the number of features that can eventualy be good. GP is then used after with only those features. Features that are included in the final formula will be the ones selected.