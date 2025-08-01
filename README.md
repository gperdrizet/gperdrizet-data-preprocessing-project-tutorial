# Air BnB EDA & data cleaning instructions

Include the following in your solution:

## 1. Investigate each feature separately (distributions)

This should include summary statistics and plots, each feature should be handled appropriately based on the data type:

1. **Numerical features**

    - **Descriptive statistics**: mean, standard deviation etc., hint: use Pandas `df.describe()`.
    - **Distribution plots**: use histograms to get an idea of the data's shape. Be sure to label plots & axes and use a scale that makes sense for the data.

2. **Categorical features**

    - **Descriptive statistics**: feature levels and level counts, hint: use Pandas `df.nunique()` and/or `df.value_counts()`.
    - **Distribution plots**: for each feature, show how many observations fall into each category. Matplotlib or Seaborn bar plots are a good basic options here.

You should also include a short description of your findings. This is a good time to think about each feature's distribution type, possibly missing and/or extreme values or anything else strange/unexplained/interesting of note.

## 2. Investigate interactions between features (correlations)

This should include a plot and a quantification of the strength of relationship between each pair of features. Quantification can be done using a correlation coefficient or statistical test. Again, each pair of features should be handled correctly based on the data types.

1. **Nominal vs nominal**

    - **Quantification**: Chi-squared test for contingency tables of count data, hint: see [`scipy.stats.chisquare`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.chisquare.html).
    - **Plot**: Stratified bar plot. Matplotlib or Seaborn are a good basic options here.

2. **Nominal vs numerical**

    - **Quantification**: Kruskal-Wallis H-test for equality of medians, using a nominal feature as the independent variable and one of the numerical features as the dependent variable. hint: see [`scipy.stats.kruskal`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.kruskal.html). Question: why am I suggesting the H-test here, rather than ANOVA?
    - **Plot**: Stratified boxplot where nominal feature is x-axis and numerical feature is y-axis. Seaborn is a great option.

3. **Interval vs numerical**

    - **Quantification**: Spearman or Kendall correlation coefficient. SciPy.stats has pairwise implementations for both: [spearmanr](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.spearmanr.html) and [kendalltau](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.kendalltau.html). Pandas [`df.corr()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.corr.html) is another option to calculate a full cross-correlation matrix for a dataframe in one call.
    - **Plot**: Scatter plot using Matplotlib. Be sure to label axes and/or plot and pick appropriate scales. Adding a best fit line can be nice, but is not super important for this data. Question: why not? Related: why am I suggesting non-parametric rank based correlation coefficients above?

### 3. Data cleaning

1. **Feature selection**: decide what features to include in (or exclude from) you analysis. Base this decision on the type and quality of information contained in each feature. Will it be useful for modeling? Example: the listing id number is not needed. hThere are no features in this dataset which should be removed based on their correlation with other features.

2. **Missing values**: The only relevant feature in the dataset that contains obviously missing data is `reviews_per_month`. Think about why this column might have so much missing data and where it came from. Then come up with a strategy to handle the missing data appropriately by either excluding it or filling it in with a meaningful value.

3. **Extreme values**: Remove or replace any extreme values for which you think action is warranted. Note: it is not required for you to take any action based solely on the identification of an observation or observations as 'statistical' outliers. Examples: the `minimum_nights` column contains 999 values for several listings, these could be removed or filled based on the assumption that they are placeholders or errors. The `price` column has several very expensive listings, but on inspection they do seem to be real data (one is a 70 foot yacht parked on Manhattan!). These could be excluded or clipped, but a justification should be made in terms of the goal of the analysis.

### 4. Feature engineering

1. **Feature encoding**: The dataset contains two nominal features which need to be encoded to numbers: `neighbourhood_group` and `room_type`. Nominal features should be one-hot encoded. See [`sklearn.preprocessing.OneHotEncoder`](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html).

2. **Data scaling & transformation**: Model performance can often be improved by transforming and/or scaling the features and labels, but this depends on the model type. The features and labels in this dataset are not normally distributed, so a Box-Cox transformation will improve the performance of many common model types. See [`sklearn.preprocessing.PowerTransformer`](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PowerTransformer.html).

3. **Other** The sky is the limit. It is common and often very effective to make new features by combining features already present, or bringing in external data. For example: what if you normalized the `price` feature by the mean residential property value in dollars per square foot for the 5 boroughs? You also could probably calculate an estimated listing age from the total reviews and the reviews per month. Be creative and do experiments. I was able to improve linear regression performance on price from under 50% of variance explained to almost 60% by adding polynomial combinations of the features to the data.
