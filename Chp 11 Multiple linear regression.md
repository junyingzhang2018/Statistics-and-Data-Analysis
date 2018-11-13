## Chp 11: Multiple Linear Regression

The multiple linear regression assumes that the response variable y is correlated with several independent variable x1, x2,...,xp

## 1. A probabilistic Model for multiple linear regression
```y=a+b1*x1+b2*x2+...+bp*xp+e, e~N(0, sigma2) ```

## 2. Fitting the multiple regression model (LS fit)
The matrix form for multiple regression model
```
Y=X*beta
TX*Y=TX*X*beta
beta=inv(TX*X)*TX*Y 
```

## 3. Goodness of fit of the model
The predicted value ```y^=X*beta^=X*inv(TX*X)*TX*Y =H*Y```
The residual is ```ei=yi-y^=(I-H)*Y```

## 4. Multiple regression in matrix notation

## 5. Statistical inference on beta

## 6. Extra sum of squares methods

## 7. Prediction of future observations

## 8. Residual diagnosis

## 9. R example of multiple linear regression

