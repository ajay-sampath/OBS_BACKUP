
| Method                  | Advantages                                       | Usage Context                                  | When to Use                      | When Not to Use                  |
|-------------------------|--------------------------------------------------|------------------------------------------------|----------------------------------|----------------------------------|
| Missing Value Treatment | - Prevents biased analysis due to incomplete data<br>- Maintains dataset integrity | - Data with missing values<br>- Inconsistent datasets | - Critical data is missing<br>- Patterns in missing data | - Data is missing at random<br>- Excessive missing data |
| Outlier Treatment       | - Reduces skewness in data<br>- Improves model accuracy | - Data with extreme values<br>- Skewed datasets | - Data has significant outliers<br>- Outliers affect model performance | - Outliers are valuable (e.g., fraud detection) |
|   - Z-score             | - Identifies outliers based on standard deviation<br>- Useful for normally distributed data | - Data with clear mean and standard deviation<br>- Comparing values within a dataset | - Normally distributed data<br>- Data without extreme skew | - Non-normally distributed data<br>- Small datasets |
|   - Interquartile Range (IQR) | - Robust against outliers<br>- Good for skewed data | - Data with outliers<br>- Skewed distributions | - Non-parametric data<br>- Data with many outliers | - Normally distributed data<br>- When precision is key |
| Feature Engineering    | - Improves model performance<br>- Reveals hidden patterns | - Complex datasets<br>- Datasets lacking informative features | - Need to enhance data quality<br>- Complex relationships in data | - Simple, well-structured datasets<br>- Limited computational resources |


### Missing Value Treatment
| Type                   | Advantages                                             | Usage Context                              | When to Use                                   | When Not to Use                      |
|------------------------|--------------------------------------------------------|--------------------------------------------|-----------------------------------------------|--------------------------------------|
| Imputation             | - Preserves data size<br>- Can be simple or complex   | - Datasets with random missing values      | - Missing data is not informative             | - Data missing not at random         |
| Deletion               | - Simplifies the dataset<br>- Removes potential biases | - Datasets with few missing values         | - Missing data is random and non-informative   | - Significant amount of missing data |
| Predictive Modeling    | - Utilizes patterns in data<br>- Can be very accurate  | - Datasets with informative missing values | - Missing data has identifiable patterns       | - No clear patterns in missing data  |

### Outlier Treatment

| Type                   | Advantages                                               | Usage Context                              | When to Use                                   | When Not to Use                  |
|------------------------|----------------------------------------------------------|--------------------------------------------|-----------------------------------------------|----------------------------------|
| Z-score                | - Identifies outliers based on standard deviation<br>- Effective for normally distributed data | - Data with clear mean and standard deviation | - Normally distributed data<br>- Standard deviation is a reliable measure | - Non-normally distributed data<br>- Data with extreme skew |

IQR

| Type                   | Advantages                                               | Usage Context                              | When to Use                                   | When Not to Use                  |
|------------------------|----------------------------------------------------------|--------------------------------------------|-----------------------------------------------|----------------------------------|
| Interquartile Range    | - Robust against outliers<br>- Effective for skewed data | - Data with outliers<br>- Skewed distributions | - Non-parametric data<br>- Data with many outliers | - Normally distributed data<br>- When precision is key |

### . Feature Engineering
| Type                   | Advantages                                               | Usage Context                              | When to Use                                   | When Not to Use                  |
|------------------------|----------------------------------------------------------|--------------------------------------------|-----------------------------------------------|----------------------------------|
| Transformation         | - Normalizes data<br>- Improves model interpretability   | - Data with non-linear patterns            | - Skewed data<br>- Data requiring normalization | - Already normalized data        |
| Feature Creation       | - Unveils new insights<br>- Enhances data representation | - Datasets lacking informative features    | - Complex relationships in data<br>- Need for additional insights | - Simple, well-understood datasets |
| Feature Selection      | - Reduces complexity<br>- Improves model performance     | - High-dimensional datasets                | - Irrelevant or redundant features present     | - Small or simple datasets       |

'

Data Transformation

| Type                   | Advantages                                                      | Usage Context                                     | When to Use                                       | When Not to Use                                 |
|------------------------|-----------------------------------------------------------------|---------------------------------------------------|--------------------------------------------------|-------------------------------------------------|
| Logarithmic            | - Reduces skewness<br>- Handles large range of values           | - Highly skewed data<br>- Multiplicative relationships | - Positive skewed data<br>- Non-zero values present | - Negative or zero values present              |
| Square Root            | - Reduces right skewness<br>- Less drastic than logarithmic    | - Moderately skewed data                          | - Right-skewed data<br>- All values are positive    | - Contains negative values                     |
| Box-Cox                | - Handles various distributions<br>- Optimizes normalization   | - Skewed data with unknown distribution          | - Continuous and positive data                    | - Zero or negative values present              |
| Yeo-Johnson            | - Generalizes Box-Cox to handle negative values                | - Skewed data including negatives                | - Continuous data with any range                  | - Categorical data                             |
| Power                  | - Customizable transformation<br>- Adjusts data distribution   | - Data not fitting standard transformations      | - Custom distribution adjustments needed          | - Standard transformations are sufficient      |
| Quantile (Rank)        | - Produces uniform distribution<br>- Robust to outliers        | - Non-normal distributions<br>- Outlier-prone data| - Outliers present<br>- Desire for uniformity      | - Normal distribution not desired              |
'
DATA SCALING 

| Type                   | Advantages                                                      | Usage Context                                     | When to Use                                       | When Not to Use                                 |
|------------------------|-----------------------------------------------------------------|---------------------------------------------------|--------------------------------------------------|-------------------------------------------------|
| Min-Max Scaling        | - Preserves relationships<br>- Easy to understand              | - Data requiring bounded range<br>- Image data   | - Features need to be on the same scale           | - Outliers present (they can skew the scale)    |
| Standardization (Z-score) | - Centers data around zero<br>- Useful in algorithms assuming zero mean | - Data with Gaussian distribution               | - Algorithms sensitive to scale of data           | - Data with non-Gaussian distribution           |
| Robust Scaling         | - Robust to outliers<br>- Centers and scales using quartiles   | - Data with outliers<br>- Heterogeneous features | - Presence of outliers<br>- Diverse feature scales | - Data without significant outliers            |
| Normalization (L2 Norm)| - Scales data to unit norm<br>- Useful in vector space models  | - Text data<br>- Cosine similarity calculations  | - Data with varying length<br>- Angle-based comparisons | - Magnitude of data points is important        |
| Max Abs Scaling        | - Scales to absolute maximum<br>- Preserves zero in sparse data| - Sparse data<br>- Data with clear max values    | - Preserving sparsity of data<br>- Known maximum value | - Data without a clear maximum                |



### Types of Hypotheses

| Hypothesis Type        | Description                                                  | Acceptance Criteria                             | Rejection Criteria                              | Other Details                                        |
|------------------------|--------------------------------------------------------------|-------------------------------------------------|-------------------------------------------------|-----------------------------------------------------|
| Null Hypothesis (H₀)   | Assumes no effect or no difference in the populations         | Insufficient evidence from data to refute H₀    | Statistical evidence suggests it's unlikely H₀ is true | - Often represents status quo or a default position  |
| Alternative Hypothesis (H₁ or Ha) | Suggests an effect or difference exists in the populations | Statistical evidence refutes H₀                 | Insufficient evidence to support H₁             | - Directly opposes the null hypothesis                |


### Acceptance and Rejection of Hypotheses



| Criteria               | Acceptance of H₀                     | Rejection of H₀                             | Notes                                                    |
|------------------------|--------------------------------------|---------------------------------------------|----------------------------------------------------------|
| p-value                | p-value > significance level (α)     | p-value ≤ significance level (α)            | - p-value indicates the probability of observing data at least as extreme as the sample data, assuming H₀ is true |
| Confidence Interval    | 95% CI includes the value of parameter under H₀ | 95% CI does not include the value of parameter under H₀ | - CI is a range of values within which the true population parameter is expected to lie |
| Test Statistic         | Test statistic falls within the acceptance region | Test statistic falls in the critical region | - Depends on the chosen statistical test and distribution |


### Considerations in Hypothesis Testing


| Factor                 | Consideration                                          | Impact on Testing                              | Example                                            |
|------------------------|--------------------------------------------------------|------------------------------------------------|----------------------------------------------------|
| Significance Level (α) | Probability of rejecting H₀ when it's true (Type I error) | Lower α reduces risk of Type I error, but increases risk of Type II error | Common α values: 0.05, 0.01                         |
| Sample Size            | Larger sample sizes provide more reliable results     | Smaller samples might lead to inconclusive or incorrect conclusions | Increasing sample size decreases the standard error |
| Power of the Test      | Probability of correctly rejecting a false H₀ (1 - Type II error) | Higher power reduces the risk of Type II error | Power depends on α, effect size, and sample size    |
| Effect Size            | Size of the difference or effect being tested         | Small effect sizes may require larger samples to detect | Effect size can be measured in various ways (Cohen's d, etc.) |



uni


| Parameter            | Description                                  | Methods                           | Considerations                          |
|----------------------|----------------------------------------------|-----------------------------------|-----------------------------------------|
| Central Tendency     | Measures the central point of the data       | Mean, Median, Mode                | Identifies the most typical value       |
| Dispersion           | Indicates the spread of the data             | Range, Variance, Standard Deviation| Measures the extent to which data values differ |
| Skewness             | Measures asymmetry in the data distribution  | Skewness coefficient              | Positive skew (right), Negative skew (left) |
| Kurtosis             | Indicates the 'tailedness' of the data       | Kurtosis coefficient              | High kurtosis (heavy tails), Low kurtosis (light tails) |
| Frequency Distribution| Counts occurrences of each value             | Frequency tables, Histograms      | Useful for categorical data             |


bi

| Parameter            | Description                                   | Methods                           | Considerations                                  |
|----------------------|-----------------------------------------------|-----------------------------------|-------------------------------------------------|
| Correlation          | Measures the strength of association between two variables | Pearson, Spearman Correlation   | Values range from -1 to 1; doesn’t imply causation |
| Cross-tabulation     | Examines the relationship between two categorical variables | Contingency Tables                | Useful for examining the relationship in categorical data |
| Comparisons          | Compares two groups                            | t-tests, ANOVA                    | Used to understand differences between groups   |
| Regression Analysis  | Understands how the dependent variable changes with the independent variable | Linear Regression                 | Useful for predicting outcomes and understanding relationships |


multi

| Parameter            | Description                                   | Methods                                 | Considerations                                  |
|----------------------|-----------------------------------------------|-----------------------------------------|-------------------------------------------------|
| Multiple Regression  | Examines relationship between one dependent and multiple independent variables | Multiple Linear Regression              | Used for prediction and causal analysis         |
| Factor Analysis      | Reduces the number of variables by grouping correlated variables | Exploratory, Confirmatory Factor Analysis| Useful in identifying underlying factors        |
| Cluster Analysis     | Groups data points into clusters based on similarity | K-means, Hierarchical Clustering       | Used for market segmentation, data grouping     |
| MANOVA               | Extension of ANOVA with multiple dependent variables | Multivariate ANOVA                      | Tests multiple dependent variables simultaneously |
| Principal Component Analysis | Reduces dimensionality while retaining most of the variability | PCA                                       | Used for data reduction, feature extraction     |




| Measure  | Description                                                  | Function in Pandas               | Interpretation                                      |
|----------|--------------------------------------------------------------|---------------------------------|-----------------------------------------------------|
| Skewness | Measures the degree of asymmetry of a distribution.          | `dataframe['column'].skew()`    | - Positive value: right (positive) skew.<br>- Negative value: left (negative) skew.<br>- Value near 0: symmetric distribution. |
| Kurtosis | Measures the 'tailedness' of the distribution.               | `dataframe['column'].kurtosis()`| - High value: heavy tails (leptokurtic).<br>- Low value: light tails (platykurtic).<br>- Value near 0: similar to normal distribution (mesokurtic). |




| Measure  | Description                                                  | Function in Pandas               | Interpretation                                      |
|----------|--------------------------------------------------------------|---------------------------------|-----------------------------------------------------|
| Skewness | Measures the degree of asymmetry of a distribution.          | `dataframe['column'].skew()`    | - Positive value: right (positive) skew.<br>- Negative value: left (negative) skew.<br>- Value near 0: symmetric distribution. |
| Kurtosis | Measures the 'tailedness' of the distribution.               | `dataframe['column'].kurtosis()`| - High value: heavy tails (leptokurtic).<br>- Low value: light tails (platykurtic).<br>- Value near 0: similar to normal distribution (mesokurtic). |




### Skewness

1. **Finding Skewness**:
    
    - Skewness is calculated using the formula: Skewness=�(�−1)(�−2)∑(��−�ˉ�)3Skewness=(n−1)(n−2)n​∑(sXi​−Xˉ​)3, where �n is the number of observations, ��Xi​ is each individual observation, �ˉXˉ is the mean, and �s is the standard deviation.
    - In software like Excel, Python (Pandas or SciPy), and R, skewness can be calculated using built-in functions.
2. **Types of Skewness**:
    
    - **Positive Skewness**: Tail on the right side of the distribution, indicating that the right tail is longer or fatter than the left.
    - **Negative Skewness**: Tail on the left side of the distribution, showing that the left tail is longer or fatter than the right.
3. **Handling Skewness**:
    
    - **Transformation**: Apply transformations to reduce skewness. For positive skew, use logarithmic, square root, or inverse transformations. For negative skew, use square or cube transformations.
    - **Normalization**: Use statistical methods like normalization to adjust the data.

### Kurtosis

1. **Finding Kurtosis**:
    
    - Kurtosis is calculated using the formula: Kurtosis=�(�+1)(�−1)(�−2)(�−3)∑(��−�ˉ�)4−3(�−1)2(�−2)(�−3)Kurtosis=(n−1)(n−2)(n−3)n(n+1)​∑(sXi​−Xˉ​)4−(n−2)(n−3)3(n−1)2​.
    - Similar to skewness, kurtosis can be easily calculated using statistical software.
2. **Types of Kurtosis**:
    
    - **High Kurtosis (Leptokurtic)**: A distribution with a sharper peak and fatter tails, indicating more outliers.
    - **Low Kurtosis (Platykurtic)**: A distribution with a flatter peak and thinner tails, indicating fewer outliers.
    - **Mesokurtic**: A distribution with kurtosis similar to the normal distribution.
3. **Handling Kurtosis**:
    
    - **Data Investigation**: High kurtosis often indicates the presence of outliers. Investigate and possibly remove these outliers.
    - **Data Transformation**: Applying transformations like logarithmic or square root can help reduce kurtosis.

### General Considerations

- **Understanding Data**: Before applying any transformation, it's crucial to understand the nature of the data and the reasons for its skewness or kurtosis.
- **Impact on Analysis**: Consider how transformations might affect the interpretation of the data and subsequent analysis.
- **Statistical Significance**: Sometimes, slight deviations from normality (in skewness or kurtosis) may not be statistically significant, especially in large samples.



### Understanding the ROC Curve

1. **Axes**:
    
    - **X-Axis (False Positive Rate)**: The False Positive Rate (FPR) is plotted on the x-axis. FPR is calculated as FPR=False PositivesFalse Positives + True NegativesFPR=False Positives + True NegativesFalse Positives​.
    - **Y-Axis (True Positive Rate)**: The True Positive Rate (TPR), also known as sensitivity or recall, is plotted on the y-axis. TPR is calculated as TPR=True PositivesTrue Positives + False NegativesTPR=True Positives + False NegativesTrue Positives​.
2. **Curve**:
    
    - The ROC curve plots TPR against FPR at various threshold settings. The threshold is the point at which the model's predicted probabilities are turned into class predictions.
3. **Interpreting the Curve**:
    
    - **Closer to the Top-Left Corner**: The closer the curve comes to the top-left corner, the better the model's performance. It means a high TPR and a low FPR.
    - **Area Under the Curve (AUC)**: The AUC measures the entire two-dimensional area underneath the ROC curve. An AUC of 1 indicates a perfect model; an AUC of 0.5 suggests no discriminative power (equivalent to random guessing).
    - **Trade-off Between Sensitivity and Specificity**: The ROC curve illustrates the trade-off between sensitivity (TPR) and specificity (1 - FPR). As the sensitivity increases, the model may also start to falsely classify more negatives as positives, increasing the FPR.
4. **Points on the Curve**:
    
    - **Upper Left Point**: Represents the ideal point where the TPR is 1, and FPR is 0. It indicates perfect classification.
    - **Point on the 45-Degree Line**: Points on the line �=�y=x indicate random chance. The closer the curve is to this line, the less effective the model is at discrimination.

### Practical Use

- **Model Comparison**: ROC curves are useful for comparing the performance of different models. A model with a ROC curve that is more toward the top-left corner, or with a higher AUC, is generally considered better.
- **Threshold Selection**: It helps in selecting the optimal threshold for classification, balancing sensitivity, and specificity based on the problem's requirements.

In summary, the ROC curve is a valuable tool for evaluating and comparing binary classification models, providing insights into their ability to distinguish between classes under various threshold settings.