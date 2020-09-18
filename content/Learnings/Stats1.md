---
date: 2020-09-03T10:58:08-04:00
featured_image: "/images/stat.png" 
title: "Exploratory Data Analysis using Basic Statistics "
text-align: justify

---

"Exploratory data analysis can never be the whole story, but nothing else can serve as the foundation stone." - Jhon Tukey

The Exploratory Data Analysis or EDA can be done in two parts : 

1. **Graphical EDA** : Graphical reprsentation of the tabular data

- **Histogram**
  - Binning Bias: One **disadvantage** of histogram is the same data may be interpreted differently depending on choice of bins. To tackle that we can use the swarm plot. It represents all the data points without a binning bias. 
  
- **Bee swarm Plot**
  - Problem with Bee swarm plot - it isnt very helpful for a large dataset as we will get edges with overlapping data points, which is necessacery in order to fit all points onto the plot.
  
- **ECDF Plot**

  Alternatively, we can compute Empirical Cumulative Distribution Function(ECDF). It shows all the data and gives the complete picture of how the data are distributed.
  - In an ECDF plot,
     - x-value is the quantity that we are measuring.
      - y-value is the fraction of data points that have a value smaller than the corresponding x-value.
 
- **Box plot**
  
   A box plot represents the salient features of dataset usng percentiles. It was invented by Jhon Tuckey. In a box plot, 
   - Middle line shows 50th percentile, edges show 25th and 75th percentile.
   - Interquartile range (IQR) - The total height of the box whcih contains the middle 50% of the data
   - The whiskers extend to the distance of 1.5 times IQR or to the extent of data whichever is more extreme. 
   - outliers - all data points outside of whiskers are plotted as indivival points. A common criteria is if a data point is 2 * IQR away from the median, it is considered as an outlier. 
  > Not all outliers are erroneous data points and depends on the context.
   - Advantage : Good representaion of large dataset which have cluttered bee swarm plots.


- **Scatter plot**
  - This supplements the quantitaive EDA and helpful to represent the correlation between two variables.
  
2. **Quantitative EDA** : Summary statistics of the tabular data 

- **Sample mean** : Sum of all the data divided by the number of data points
  - Problem : heavily influenced by outliers . Instead use median.
  
- **Sample median**: Calculated by sorting the data and choosing the datum in the middle. 
  - As it is derrived from the rank of the data and not from the value of the data, it is immune to extreme data points. 
  - The median is the 50th percentile of the data which means 50% of the data is below that value. 
  
- **Percentiles**: We can get the 25th and 75th percetile which represents 25% or 75 % data are below that point respectively. 

- **Variance** : The mean squared distance of the data from their mean.
   - Informally, a measure of the spread of data.
   - As calculation of variance involves sqaured quantities, it doesn't have the same units of what we have measured.
   
- **Standard deviation** : Square root of variance
   - Good representation of spread of data

- **Covariance** :A measure of how two quantities vary together.
   - if x and y both tend to be above or below ther respective means together, then covariance is positive so they are positively correlated. When x is high, so is y and vice versa.
   - if x is high when y is low, the covariance is negative, and the data are negatively or anticorrelated.
having a large variance does not mean the covariance is large.
   - To determine a generally applicable measure of how to variables depend on each other, we need it to be dimensionsless (without any unit). Covariance is not unitless/ dimensionless.

- **Pearson Correlation coefficient** : Also called the Pearson r it is obtained by dividing covariance by standard deviations of the x and y variables.
  - Denotes the variability due to codependence (the covariance) to the variability inherent to each variable independently (their standard deviations).
  - it is dimensionless and range from -1 (complete negative / anticorrelation) to 1 (complete positive correlation).
  - 0 shows no correlation at all.
  - A good metric for correlation between two variables.
  - Easier to interpret than covariance.


Python implementation of EDA with examples can be found [here.](https://github.com/KIRTISNIGDHA/Statistics/blob/master/Exploratory%20data%20analysis%20using%20basic%20statistics.ipynb)