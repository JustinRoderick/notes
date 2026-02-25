Attempts to form a linear relationship between input variables and an output, or the dependent variable. The goal of Linear Regression is to minimize the [[Loss Function]] of a model by adjusting the weights of input variables.

One important thing to note as that it is important to remove variables that have high correlation before performing linear regression as these variables can have adverse affects on the model.
- Small change in variables with high correlation can have dramatic effects on the output value.
- Can inflate the importance/weight of these variables making other features insignificant.
- The model will struggle to determine which of correlated features actually results in changes.

Common remedies are:
- Remove one of the correlated variables.
- Combine them in a meaningful way.
- Perform PCA (Principal Component Analysis) [[Dimensionality Reduction]]
  

