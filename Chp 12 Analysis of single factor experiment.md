# Chp 12 Analysis of single factor experiment

## 1. Completely randomized design
* Box plot to compare several groups
* One-way ANOVA is the extension of two sample independent t-test when we have more than two groups
## 2. Model and estimate of its parameters
* LS estimate of group effect ti, the grand mean and the pooled variance s^2
## 3. Analysis of variance and the F test

## 4. Model diagnosis of using residual plots
* ei vs yi^ to check constant variance assumption.
* qqnorm(ei), qqline(ei) to check normality
* If data are collected with time, run plot of ei to check autocorrelation
* eij*=eij/s can be used to check outlier. abs(eij*)>2 is regarded as outlier
## 5. Multiple comparison of means

From least conservative to most conservative, most powerful to least powerful
* LSD (least significant differnce)
* Tukey menthod by using the Studentized range distribution
* Bonferroni method, 
