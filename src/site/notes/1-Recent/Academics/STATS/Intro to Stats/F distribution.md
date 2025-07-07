---
{"dg-publish":true,"permalink":"/1-recent/academics/stats/intro-to-stats/f-distribution/","created":"2024-03-25T13:53:55.514-04:00","updated":"2025-07-07T17:21:02.337-04:00"}
---

- $F$ distribution
	- the ratio of two sample variances has an $F$ distribution
		- if both populations are normally distributed
	- has 2 parameters
		- $\nu_{1}$
			- degrees of freedom for the numerator
		- $\nu_{2}$
			- degrees of freedom for the denominator
		- $\frac{S_{1}^2}{S_{2}^2}\sim F(n_{1}-1,n_{2}-1)$
			- (numerator df, denominator df)
			- ![](https://i.imgur.com/4k5h3M8.png)
	- distribution of the F test statistic under $H_{0}$
		- if the null hypothesis is true, the value we get from F is contained in that distribution
			- extreme outlier $\to$ low [[1-Recent/Academics/STATS/Intro to Stats/P-values\|p-value]] $\to$ low chance that our hypothesis is true
			- area to the right only, [[1-Recent/Academics/STATS/R\|R]]
			- 