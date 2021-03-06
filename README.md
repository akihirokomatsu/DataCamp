# DataCamp

# Statistical Thinking in Python (Part 1)
- learn the importance of viewing initial data via histograms, swarmplots, and empirical cumulative distribution functions (ECDF)
- learn how to write an ecdf function that will take one dimension arrays
- learn how to plot ecdf graphs
- percentiles and box plots: middle 50% of data is the IQR, the whiskers extend out to extent of data or 1.5-2 IQR, anything beyond the whiskers are outliers
- covariance, a measure of how two quantities vary together 
- pearson correlation, unitless measure of how two quantities vary together, (cov)/[(std x)(std y)], between -1 and 1
- probabilistic thinking and statistical inference, such as using probability to estimate the mean
- hacker statistics: simulation of repeated measurements to compute probabilities 
- Bernoulli trial: an experiment that has two outcomes: true or false, such as a coin flip
- Poisson process: timing of events are independent of when the previous event happened
- Poisson distribution: number of events (r) in a given time interval with an average rate of λ arrivals per interval  
- Normal/Gaussian distribution: the effect of std dev on the PDF and CDF, warnings of when data looks normally distributed but when its not
- Exponential distribution - the timing between incidents of a Poisson distribution is exponentially distributed 

# Statistical Thinking in Python (Part 2)
- Optimal parameters - parameter values that bring the model in closest agreement with the data, but the model should be right, or else the optimal parameters are not useful
- linear regression by least squares, a line that produces the minimal sum of the squares of the residuals
- linear regression where degree = 1: slope, intercept = np.polyfit(x, y, degree of polynomial)
- Importance of exploratory data analysis: Anscombe's quartet shows that the blindly calcalating mean, regression line, etc. is dangerous
- bootstrapping/sampling with replacement: from a data set, choose a random element and copy into resampling data set. Repeat until resampled set is the szme size as the original data set. Note: after each time a random element is chosen from the data set, the element is replaced and is eligible for random selection again
- bootstrap sample: a resampled array of the data
- bootstrap replicate: statistic computed from a resampled array, ie mean
- bootstrap confidence intervals: if we repeated measurements over and over again, p% of the observed values would be within the p% confidence interval
- pairs bootstrap for linear regression: resample data in pairs, based on the x and y variables; beneficial in instances with two existing variables (ex: state county and democratic voting); then use resampled pairs to calculate slope & intercept (each slope&intercept is a bootstrap replicate); repeat multiple times to compute confidence intervals from percentiles of boostrap replicates
- hypothesis testing: an assessment of how reasonable the observed data are assuming a hypothesis is true
- permutation: random reordering of entries in an array, especially useful where null hypothesis is assuming the two quantities are identically distributed
- test statistic: a single number that can be computed from observed data and from data you simulate under the null hypothesis, ex: mean
- p value: the probability of obtaining a value of your test statistic that is at least as extreme as what was observed, under the assumption the null hypothesis is true. It is NOT the probability that the null hypothesis is true
- Null hypothesis significance testing (NHST): statistically significant difference between two quantities is determined by the smallness of a p-value.
- statistical significant =/= practical significance
- bootstrap hypothesis testing for two sample test: pipeline - 1) clearly state null hypothesis 2) define test statistic 3) generate many sets of simulated data assuming the null hypothesis is true 4) compute the test statistic for each simulated set 5) calculate p-value
- A/B Testing: address the difference in the A and B cases using hypothesis testing; null hypothesis is that the test statistic is impervious to the change
- hypothesis test of correlation: null hypothesis is two variables are uncorrelated, Pearson coefficient is the test statistic, compute p value as fraction of replicates that have Pearson coefficient at least as large as observed

# Supervised Learning with scikit-learn
- machine learning: art and science of giving computers the ability to learn to make decisions from data without being explicitly programmed
- supervised learning uses labeled data, unsupervised learning uses unlabeled data
- unsupervised learning: uncovering hidden patterns from unlabeled data, ex: grouping customers into distinct categories (clustering)
- reinforcement learning: software agents interact with an environment, learn how to optimize their behavior, given a system of rewards and punishments
- supervised learning: predictor variables/features and a target variable
- aim of supervised learning is to predict the target variable, given the predictor variables
- classification: use if the target variable consists of categories (i.e. spam or not spam)
- regression: use if the target variable is continuous (ie price of a house)
- goal of supervised learning is often (1) automate time-consuming or expensive manual tasks (doctor's diagnosis), (2) make predictions about the future (ie will a customer click on an ad or not)
- k-Nearest Neighbors: predict the label of a data point by looking at the 'k' closest labeled data points; k-NN can create decision boundaries, lines that separate a graph into regions where points within them are all labeled the same
- training a model on the data = 'fitting' a model to the data, using .fit() method
- to predict the labels of new data: .predict() method
- measuring model performance: fraction of correct predictions
- the predictions on a test set is not indicative of ability to classify, so common practice is split data into training and test set
- fit/train the classifier on the training set, make predictions on the test set, compare predictions with the known labels, using train_test_split() from sklearn.model_selection, KNeighborsClassifier(), knn.fit(), knn.predict(), knn.score()
- model complexity: larger k = smoother decision boundary = less complex model; smaller k = more complex model = can lead to overfitting



