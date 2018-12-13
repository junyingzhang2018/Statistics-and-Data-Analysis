# Chapter 10: Simple Linear Regression

## 1. A probabilistic model for Simple Linear Regression
Simple linear regression studies the linear relationship between the response variable y and the indicator variable x. x is assumed to be fixed and y is a random variable. The probability model is

```
y=a+b*x+e, e~N(0, sigma2)
```
## 2. Four assumptions of linear regression
* y has a linear relationship with a, b
* The variables (x1,y1), (x2,y2),...,(xn,yn) are iid
* The random error e is normally distributed with mean 0 and variance sigma2
* Constant variance assumption, homogeneity

## 3. OLS estimation of model parameters
The OLS estimation tries to minimize the sum of squared difference between the observed variable yi and the predicted variable yi^. 
```
SSE=sum((yi-yi^)^2)=sum((yi-a^-b^*xi)^2)
```
By setting the first partial derivative of SSE to intercept a and slope b, we get the below normal equaltions
```
sum(ei)=0          b^=SXY/SXX
sum(ei*xi)=0       a^=mean(y)-b^*mean(x)
```

## 4. Parameter estimate and Statistical inference of slope b and intercept a
The parameter estimate of slope ```b^~N(b, sigma2/SXX)```
The parameter estimate of the intercept a is ```a^~N(a, (1/n+mean(x)^2/SXX)*sigma2) ```

## 5. Goodness of fit of the LS line, R^2, the coefficient of determination, ANOVA table
The goodness of fit of the simple linear regression can be seen from the R^2, coefficient of determination. R^2=SSR/SST. It is the percentage of variation in y that is explained by the linear model. 
```
The total sum of squares SST=sum((yi-mean(y))^2), SST has degree of freedom n-1
The regression sum of squares SSR=sum((yi^-mean(y))^2), SSR has degree of freedom 1
The residual sum of squares is SSE=sum((yi-yi^)^2), SSE has degree of freedom n-2
SST = SSR + SSE
The mean square is the sum of squares divided by its degree of freedom. 
The mean square of error MSE=SSE/(n-2) is an unbiased estimate of sigma2
```
To check the goodness of the regression line, the null hypothesis is that
```H0: b=0 vs H1: b^=0```
Under the null hypothesis, ```SSR/sigam2 ~chisq(1), SSE/sigma2~chisq(n-2)```
Under the alternative hypothesis, ```SSR/sigma2>chisq(1)```
So under the null hypothesis, ```(SSR/sigma2)/(SSE/sigma2/(n-2))~F(1,n-2)```
Under the H1, ```F=MSR/MSE>F(1,n-2)```
So we reject the null hypothesis if ```F>F(0.95, 1, n-2)```

## 6. Hypothesis testing and confience interval and p-value for b and a
For the slope b, ```b^~N(b, sigma2/SXX)```
```(b^-b)/(sqrt(s^2/SXX))~t(n-2)```
So the 95% CI for slope b is
```b^+-t(0.975, n-2)*sqrt(s^2/SXX)```
For the intercept a, ```a^~N(a, (1/n+mean(x)^2/SXX)*sigma2))```
(a^-a)/(sqrt((1/n+mean(x)^2/SXX)*sigma2)))~t(n-2)
So the 95% CI for a is
```a^+-t(0.975, n-2)*sqrt((1/n+mean(x)^2/SXX)*s^2))```

## 7. Confidence and prediction interval for u and new yi
For ```yi^=a^+b^*x0, yi^ ~N(a+b*x0,1/n+(mean(x0)-x0)^2/SXX)*sigma2) )```
So the 95% confidence interval is
```a^+b^*x0+c(-1,1)*t(0.975, n-2)*sqrt(1/n+(mean(x0)-x0)^2/SXX)*s^2)) ```

## 8. Model diagnosis by residual plot
* Residual plot of ei vs xi, if there is some pattern, this might means missing other predictor variables in regression
* ei vs yi^ to check constant variance
* Run plot of ei to check autocorrelation
* QQ plot to check normality

## 9. Standardized residual and influential plot
The standard residual is ```ei*=ei/(s*sqrt(1-1/n-(xi-mean(x))^2/SXX)=ei/(s*sqrt(1-hii))```
If abs(ei*)>2, then we regard it as an outlier.

Influential point, the predicted value ```yi^=x*b^=x*inv(tx*x)*tx*y=Hy```
```yi^=h11*y1+h12*y2+...+h1n*yn```
And ```h11+h12+...+h1n=(k+1)```
So the average value is (k+1)/n
If each ```hii>2*(k+1)/n```, we regard it as the influential point.

## 10. Variance stabilization transformation using delta method
If the var(X)=h(u) which is a function of the mean(u), then a suitable variance stabilization transformaiton would be
y~f(1/sqrt(h(u))du

## 11. Simple Linear regression example by R
