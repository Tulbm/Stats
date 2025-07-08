---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/Test Statistics.md","permalink":"/stats/intro-to-stats/test-statistics/","created":"2024-04-03T13:37:20.516-04:00","updated":"2025-07-07T17:21:02.512-04:00"}
---

# Z test
- uses $\sigma$, if we don't know that [[Academics/STATS/Intro to Stats/Population and Samples\|parameter]] then we need to use the T test
- $Z=\frac{\bar X-\mu}{\sigma/\sqrt n}$ has the standard normal distribution
	- converts our $\bar X$ to $N\sim (0,1)$
## For proportions
$Z=\frac{\hat{p}_{H}-\hat{p}_{N}}{SE_{0}(\hat{p}_{H}-\hat{p}_{N})} =\frac{\hat{p}-p_{0}}{\sqrt{ \frac{p_{0}(1-p_{0})}{n} }}$
# T test
- used when we dont know $\sigma$
- test statistic $t=\frac{\bar X-\mu}{s/\sqrt n}$ has the [[Academics/STATS/Intro to Stats/Normal Distribution#T distribution\|t distribution]] with $n-1$ degrees of freedom
- the observed value of the test(t) statistic tells us how many standard errors of the value of $\bar X$ is from the hypothesized value of $\mu$
	- $\text{Test Statistic} = \frac{\text{Estimator}-\text{Hypothesized Value}}{SE\text{(Estimator)}}$
	- $t = \frac{\bar X - \mu_0}{SE(\bar X)}$
		- SE = standard error
	- $t = \frac{\bar X - \mu_0}{s/\sqrt n}$  
- when comparing the difference in two means
	- $t=\frac{\bar{X}_1-\bar{X}_2}{SE(\bar{X}_1-\bar{X}_2)}$ 
		- $\mu$'s cancel each other
# [[Academics/STATS/Intro to Stats/Chi-Squared Test\|Chi-Squared Test]]
# F test
[[Academics/STATS/Intro to Stats/F distribution\|F distribution]]