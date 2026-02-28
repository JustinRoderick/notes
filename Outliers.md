Outliers are data points the differ from the rest of the observed values by a large amount. Outliers can greatly affect the accuracy when training a model and are removed during data cleaning.

## Ways to Detect Outliers

First lets mention Standard Deviation which measures the relative distance of data point when compared to their mean of all data points. This is important when determining how tightly data is clustered and therefore detecting outliers.

- Z-Score: Calculates how many standard deviations a specific point is from the mean of the data. A good score has a value of 0 and scores that are +- 3 are typically considered outliers.
- IQR (Interquartile Range): Divides a data set into 4 quadrants with Q1, Q2, and Q3 being the cutoff points. The IQR is then the range of values between Q1 and Q3 (Q3-Q1), and this is typically the standard range. Therefore, values that fall outside this range are likely outliers.