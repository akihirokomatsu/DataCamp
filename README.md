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
