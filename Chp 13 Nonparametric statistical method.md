# Chp 13 Nonparametric statistical method

## 1. Sign test for the median of one group

## 2. Wilcoxon signed rank test for median of one group (needs data to be symmetric)

## 3. Independences for two independent samples

Wilcoxon rank sum test and Mann and Whitney U-test
## Wilcoxon signed rank test

`wilcox.test(x, y = NULL, alternative='two.sided', mu=200, conf.level = 0.95)`

`wilcox.test(x, y, alternative = 'two.sided', conf.level = 0.95)`
## 4. Inference for several independent samples
Kruskal-Wallis test~CHISQ(a-1), a is the number of groups

Kruskal–Wallis test
In this case, there is a significant difference in the distributions of values among groups, as is evident both from the histograms and from the significant Kruskal–Wallis test.  Only in cases where the distributions in each group are similar can a significant Kruskal–Wallis test be interpreted as a difference in medians.

```
kruskal.test(Value ~ Group, 
             data = Data)


Kruskal-Wallis chi-squared = 7.3553, df = 2, p-value = 0.02528
```

## 5. Pearson linear correlation Spearman rank correlation coefficient and Kendall rank correlation coefficient

Test for association or correlation between paired samples

`cor.test(x, y,
         alternative = c("two.sided", "less", "greater"),
         method = c("pearson", "kendall", "spearman"),
         exact = NULL, conf.level = 0.95, continuity = FALSE, ...)'
         
Pearson Linear correlation

`cor.test(x, y, method='pearson', conf.level=0.95)`

```	Pearson's product-moment correlation

data:  x and y
t = 10.523, df = 6, p-value = 4.327e-05
alternative hypothesis: true correlation is not equal to 0
95 percent confidence interval:
 0.8585052 0.9954403
sample estimates:
      cor 
0.9739638 
```

Spearman rank correlation

`cor.test(x, y, method='spearman', conf.level=0.95)`

```	Spearman's rank correlation rho

data:  x and y
S = 0, p-value = 4.96e-05
alternative hypothesis: true rho is not equal to 0
sample estimates:
rho 
  1 
 ``` 
Kendall rank correlation

`cor.test(x, y, method='kendall', conf.level=0.95)`

```	Kendall's rank correlation tau

data:  x and y
T = 28, p-value = 4.96e-05
alternative hypothesis: true tau is not equal to 0
sample estimates:
tau 
  1 
  
