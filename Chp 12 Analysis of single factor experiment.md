# Chp 12 Analysis of single factor experiment
Analysis of variance is used to compare whether the response variable is different between several groups. It is the extension of two sample independent t-test when we have more than three groups to compare. 
The assumption for ANOVA is 
* Independence, this can be done by randomly sampling
* Normality, the random error is assumed to be normally distributed.
* Constant variance, for each group, the variance is assumed to be the same

## 1. Completely randomized design
* Box plot to compare several groups
* One-way ANOVA is the extension of two sample independent t-test when we have more than two groups

## 2. Model and estimate of its parameters
The model is assumed to be
yij=ui+eij, i=1,2,...,r, 
eij~N(0,sigma2)
The null hypothesis is that ```H0: U1=U2=...=UR vs: H1: Not all of them are equal```.

## 3. Analysis of variance and the F test

The total sum of squares is ```SST=sum((yij-mean(y))^2)```
The model sum of squares is ```SSA=n1*(y1.-y..)^2+n2*(y2.-y..)^2+...+(yr.-y..)^2 ```
The residual sum of squares is ```SSE=sum((yij-yi.^)^2)```
The F test is ```F=MSA/MSE=(SSA/(r-1))/(SSE/(n-r))~F(r-1, n-r)``` under the null hypothesis.
We reject the null hypothesis if ```F>F(0.975, r-1, n-r)```
The pooled variance estimate is s^2=```SSE=sum((yij-yi.^)^2)/(n-r)```. It is unbiased estimate of sigma2.

## 4. Model diagnosis of using residual plots
* ei vs yi^ to check constant variance assumption.
* qqnorm(ei), qqline(ei) to check normality
* If data are collected with time, run plot of ei to check autocorrelation
* eij*=eij/s can be used to check outlier. abs(eij*)>2 is regarded as outlier

## 5. Multiple comparison of means
If we are comparing k confidence intervals, then the combined confidence will be <1-alpha. Let ki to denote the confidence level of the ith comparison, 
Insection(k1, k2, ...,kr)=1-Union(k1^, k2^, ..., kr^)>=1-sum(k1^, k2^, ..., kr^)=1-k*alpha
For the Bonferroni method, we set the significance level to alpha/k.

From least conservative to most conservative, most powerful to least powerful
* LSD (least significant differnce)
* Tukey menthod by using the Studentized range distribution
* Bonferroni method, 
