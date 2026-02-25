Loss Functions are a mathematical formula that determines the difference between a ML models predicted score and actual score. It is used to measure a models performance and also guide optimization models like [[Gradient Descent]] when updating model parameters.

## Common Loss Functions
- Regression
	- Mean Squared Error (MSE): Measures the average squared differences between the predicted and actual value.
	- Mean Absolute Error (MAE): Measures the average absolute difference, without the square. This makes it more robust to outliers.
- Classification
	- Cross-Entropy Loss: Measures performance based on the probability that a predicted value belongs in that class. 
	- Hinge Loss: Mainly used in [[Support Vector Machine]] to maximize the margin between classes to get the most accurate boundary line.