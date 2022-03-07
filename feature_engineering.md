### How to detect outliers and remove them?

Some of the common ways to detect outliers are:
1. IQR - we can define a threshold of (Q1 - 1.5 * IQR) and (Q3 + 1.5 * IQR) - apply it mainly when the data is skewed
2. Data points that falls outside of 3 standard deviations, we can use z score

z score is calculated as z = (x - mean)/ std dev -> scipy.stats.zscore(input_data)
if z score > 3, we can reject the point

This is generally applicable for normal distribution.
We take 3 std dev because within 3 std dev 99.7% of the data is present

3. Using scatter plot
4. Using box plot

### Which algorithms are impacted by outliers?

1. Naive Bayes Classifier - robust
2. SVM - robust
3. Linear Regression - sensitive
4. Logistic Regression - sensitive
5. Decision Trees - Robust
6. KNN - robust
7. Kmeans - sensitive
8. Hierarchical - sensitive
9. PCA - very sensitive
10. Neural Networks - sensitive

### Why is it important for data to have a Gaussian distribution and how to transform data so that it can have Gaussian distribution?

Some algorithms like linear and logistic regression have an underlying assumption that the data is normally distributed. Other models like Neural Nets, SVM and tree based do not have this assumption. But generally Gaussian distribution results in better models.

We can use a Q-Q plot to identify if the distribution of the data is Gaussian.  -> scipy.stats.probplot(data, dist="norm")

Some of the transformation that we can do are:

1. **Logarithmic Transformation** -> np.log10(data + 1)
2. **Reciprocal Transformation** -> 1/(data+1)
3. **Square Root Transformation** -> data ** 0.5
4. **Exponential Transformation** -> data ** (1/5)
5. **Boxcox Transformation** -> scipy.stats.boxcox(data + 1)

### How to handle missing data?

Missing data can be handled in the following ways:

1. Delete the record
**When to apply**
If the data set is large and removing records won't affect

2. Create a separate model to handle missing values
Consider the missing values as the test data and train a model to predict the missing values

3. Statistical Methods

4. Imputation
* Random Sample Imputation
* End of distribution Imputation
* Arbitrary Imputation

**One interesting way to visualise the missing values is to use the following line of code**
```sns.heatmap(data.isnull(),cbar=False,cmap="viridis")```
