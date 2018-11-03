Chp 9 Inferences for Proportions and Count Data
===============================================

1. One sample proportion test for population parameter p from Binomial(n,p)
-------------------------------------------------------------------------------
Inferences on p are based on the central limit theorem that for large n, the sample proportion p^ is approximately normal with mean p and standard deviation 
`sqrt(p*q/n)`. A large sample two-sided 95% confidence interval for p is
`p^+c(-1,1)*qnorm(0.975)*sqrt(P^*q^/n)`

A large sample test on p to test H0: P=P0 can be based on the test
z=(p^-p0)/sqrt(p^q^/n) or z=(p^-p0)/sqrt(p0*q0/n)
Both statistics are asymptotically standard normal under H0

2. Two sample proportions test for p1, p2 based on two random samples of size n1 and n2. 
----------------------------------------------------------------------------------------------
The basis for inference on p1-p2 is the result for large n1 and n2,
the difference in the sample proportions p1^-p2^, is approximately normal with mean p1-p2 and standard deviation `=sqrt(p1*q1/n1+p2*q2/n2)`. 
A large sample two-sided 100(1-alpha)% confidence interval for p1-p2 is given by

`p1^-p2^+c(-1,1)*z0.975*sqrt(p1*q1/n1+p2*q2/n2)`

A large sample two-sided z-test can be used to test H0: p1=p2 vs H1: p1^=p2 by using the test statistics

`z=(p1^-p2^)/sqrt(p1*q1/n1+p2*q2/n2)` or `z=(p1^-p2^)/sqrt(p^*q^(1/n1+1/n2))`, p^ is the pooled variance=`(x+y)/(n1+n2)`

3. Chi-square goodness of fit test
------------------------------------
A generation of the test on the binomial proportion p is a test on the cell probability of a multinomial distribution. 
Based on the random sample of size n from a c-cell multinomial distribution (one-way count data) with cell probability p1,p2,...,pc, the test of 
`H0: p1=p10, p2=p20,..., pc=pc0 vs H1: At lease one pi^=pi0`
is based on the chi-square statistics having the general form

`chisq=sum((observed-expected)^2/expected)`
Observed refers to the observed cell counts ni and expected refer to the expected cell count ei=npio under H0. The degree of freedom of the chi-square statistics are c-1. The primary use of this statistics is for the goodness of fit test of a specified distribution to a set of data. If any parameter 
of the distribution are estimated from the data, then one d.f. is deducted from each independent estimated parameter from the total d.f. c-1.

Feel free to access [my linkedin] (https://www.linkedin.com/in/junyingzhang/)
