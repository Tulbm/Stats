---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/Inference for two means.md","permalink":"/stats/intro-to-stats/inference-for-two-means/","created":"2024-03-15T13:44:53.549-04:00","updated":"2025-07-07T17:21:02.327-04:00"}
---

- [[Academics/STATS/Intro to Stats/Sampling Distributions\|Sampling distribution]] of the difference in sample means
	- sampling independently from two populations
	- has a mean of $\mu_{1}-\mu_{2}$
		- $E(\bar{X}-\bar{X})=E(\bar{X})-E(\bar{X})=\mu_{1}-\mu_{2}$
	- has a standard deviation of $\sigma _{\bar{X_{1}}-\bar{X_{2}}}=\sqrt{ \frac{\sigma_{1}^2}{n_{1}}+\frac{\sigma_{2}^2}{n_{2}} }$
		- $Var(\bar{X}_{1}-\bar{X}_{2})=Var(\bar{X}_{1})+Var(\bar{X}_{2})=\frac{\sigma_{1}^2}{n_{1}}+\frac{\sigma_{2}^2}{n_{2}}$
	- is normally distributed if we are sampling from normally distributed populations
		- if the distributions are not normal but the sample sizes are large:
			- $\bar{X}_{1}, \bar{X}_{2}\text{ and }\bar{X}_{1}-\bar{X}_{2}$ will be approximately normal
- [[Academics/STATS/Intro to Stats/Hypothesis Testing\|Hypothesis Testing]] and [[Academics/STATS/Intro to Stats/Confidence Intervals\|Confidence Intervals]] for $\mu_{1}-\mu_{2}$ when $\sigma_{1}$ and $\sigma_{2}$ are unknown
	- if we are drawing two independent samples from two normally distributed populations
		- (needed here as both procedures assume normality)
		- then
			- $\frac{(\bar{X}_1-\bar{X}_2)-(\mu_1-\mu_2)}{\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}}}\sim N(0,1)$
			- $\frac{(X_1-X_2)-(\mu_1-\mu_2)}{\sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}}$ has the t-distribution
	- two methods
		- both assume
			-  the two samples are simple random samples from their respective populations
				- or are the results of a randomized experiment
			- populations are normally distributed
				- not very important for large sample sizes ([[Academics/STATS/Intro to Stats/Central Limit Theorem\|Central Limit Theorem]])
					- two sample t procedures are more robust to violation of normality than the one sample t procedure as well
				- can be t
			- the two samples are independent
		- pooled-variance two-sample t
			- an exact procedure that requires the additional assumption that $\sigma_{1}^2=\sigma_{2}^2$
				- means that the distributions look the same but for a shift
				- ![](https://i.imgur.com/hDJlRuq.png)
					- $\sigma_{2}<\sigma_{1}$ 
			- math looks clean, but if assumption is false...
			- assumes normality
			- $SE_p(\bar{X}_1-\bar{X}_2)=\sqrt{\frac{s_p^2}{n_1}+\frac{s_p^2}{n_2}}$
				- $=s_p\sqrt{\frac1{n_1}+\frac1{n_2}}$
			- $df$ for the t: $n_{1}+n_{2}-2$
		- welch procedure
			- approximate procedure that does not assume $\sigma_{1}^2=\sigma_{2}^2$
			- assumes normality as well
			- $SE_W(\bar{X}_1-\bar{X}_2)=\sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}$
			- $df$ for the t: $\frac{(\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2})^2}{\frac1{n_1-1}(\frac{s_1^2}{n_1})^2+\frac1{n_2-1}(\frac{s_2^2}{n_2})^2}$ 
				- $\left( \frac{s_{1}^2}{n_{1}}+ \frac{s_{2}^2}{n_{2}} \right)^2 / \frac{1}{n_{1}-1}\left( \frac{s_{1}^2}{n_{1}} \right)+ \frac{1}{n_{2}-1}\left( \frac{s_{2}^2}{n_{2}} \right)^2$
		- to estimate the common population variance, we pool the sample variances together
			- $s_{p}^2=\frac{(n_{1}-1)s_{1}^2+(n_{2}-1)s_{2}^2}{n_{1}+n_{2}-2}$
	- the endpoints of a $(1-\alpha)100\%$ confidence interval for $\mu_{1}-\mu_{2}$ are given by 
		- $\bar{X}_1-\bar{X}_2\pm t_{\alpha/2}SE(\bar{X}_1-\bar{X}_2)$
	- [[Academics/STATS/Intro to Stats/Test Statistics#T test\|t test statistic]]
		- $t=\frac{\bar{X}_1-\bar{X}_2}{SE(\bar{X}_1-\bar{X}_2)}$ (no mean because we're assuming they're equal for the $H_{0}$)
			- t test is always done assuming $H_{0}$ is true
		- used to test the null hypothesis that the population means are equal $(H_{0}:\mu_{1}=\mu_{2})$
			- to choose between the 2 procedures consider
				- pooled-variance t is exact if the assumptions are true, while Welch is only an approximation
				- pooled-variance t is a special case of other common statistical methods (ANOVA/regression), while Welch is its own thing
				- pooled-variance t can perform horribly if the population variances are very different, while Welch does well
					- even worse if the sample sizes are also very different
				- when $\sigma_{1}^2=\sigma_{2}^2$ Welch performs only a little worse than the pooled-variance t
	- example
		- psychotic x nonpsychotic
			- ratio of $\frac{s_{1}}{s_{2}}<2$, in this case its 1.10
				- they're pretty close, and sample sd's are never gonna be equal, so its reasonable to say that $\sigma_{1}=\sigma_{2}$
				- both pooled-variance t and welch are reasonable
					- using pooled variance
						- $s_p^2=\frac{(n_1-1)s_1^2+(n_2-1)s_2^2}{n_1+n_2-2}=\frac{(10-1)5.27^2+(15-1)4.77^2}{10+15-2}=24.73$
						- $SE_p(\bar{X}_1-\bar{X}_2)=s_p\sqrt{\frac1{n_1}+\frac1{n_2}}$
							- $=\sqrt{24.73}\sqrt{\frac1{10}+\frac1{15}}=2.03$
						- $t=\frac{\bar{X}_1-\bar{X}_2}{SE_p(\bar{X}_1-\bar{X}_2)}$
							- $=\frac{24.25-16.47}{2.03}=3.83$
						- degrees of freedom are $n_{1}+n_{2}-2=23$
						- 95% confidence interval for $\mu_{1}-\mu_{2}$
							- $\bar{X}_1-\bar{X}_2\pm t_\text{.025}SE_p(\bar{X}_1-\bar{X}_2)$
							- $24.25 − 16.47 ± 2.069 × 2.03$
							- $=.78 ± 4.20$
							- for a 95% interval of $(3.58,11,98)$
					- using welch
						- $SE_W(\bar{X}_1-\bar{X}_2)=\sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}$
						- $t=\frac{\bar{X}_1-\bar{X}_2}{SE_W(\bar{X}_1-\bar{X}_2)}$
							- $=\frac{24.25-16.47}{2.07}=3.75$
						- $df=\frac{(\frac{s_{1}^{2}}{n_{1}}+\frac{s_{2}^{2}}{n_{2}})^{2}}{\frac{1}{n_{1}-1}(\frac{s_{1}^{2}}{n_{1}})^{2}+\frac{1}{n_{2}-1}(\frac{s_{2}^{2}}{n_{2}})^{2}}=18.053.$
						- 95% confidence interval for $\mu_{1}-\mu_{2}$
							- $\bar{X}_1-\bar{X}_2\pm t_\text{.025}SE_W(\bar{X}_1-\bar{X}_2)$ 
							- $24.25 − 16.47 ± 2.100 × 2.07$
							- $=7.78 ± 4.35$
								- for a 95% interval of $(3.43, 12.13)$
			- just use [[Academics/STATS/R\|R]] 
			- we can be $95\%$ confident that the difference in true mean dopamine levels $(\mu_{p}-\mu_{n})$ lies between $3.6$ and $12.0$ 
			- p-value = $0.0008569$
				- the mean of the group that became nonpshychotic was significantly lower than that of the group that remained psychotic (two-tailed t-test of independent means: $t(23)=3.83;P<.001).$
		- blood calcium level
			- group that drink orange juice vs one who didnt
			- confidence interval
				- 95% CI for $\mu_{d}-\mu_{c}$
					- $\mu_{d}$ = true mean change in calcium for the vitamin d group
					- $\mu_{d}-\mu_{c}=$ treatment effect
			- hypothesis
				- $H_{0}:\mu_{d}-\mu_{c}=0\to H_{0}:\mu_{d}=\mu_{c}$
				- $H_{a}:\mu_{d}\neq\mu_{c}$
			- plots look symmetric, we dont know if its normal tho
				- the t-procedure stull works well with normality violations so should be fine
				- sd's are close, either pooled-variance or welch are reasonable
			- [[Academics/STATS/R\|R]]
				- pooled
					- t.test(Fortified,Control,var.equal=TRUE)
				- welch
					- t.test(Fortified,Control,var.equal=FALSE)
				- $95\%$ CI for $\mu_{d}-\mu_{c}=(-3.3,2.6)$ mg/dl
					- we can be 95% confident that the difference in true mean of the change in calcium ($\mu_{d}-\mu_{c}$) lies between -3.3 and 2.6 ml/dl
				- t(23) = -0.24647
					- p-value is double the area to the left$\approx 0.81$
					- large p $\to$ no evidence against $H_{0}$
					- there is no evidence of a difference in the true mean change in calcium between the vitamin d and the control group
- paired-difference procedures (dependent samples)
	- both measurements are on the same sample, with different conditions
	- designs
		- pretest-posttest design
			- sketchy
			- measurements are taken on the same individuals before and after a treatment
				- normally we have a control group that doesnt get the treatment
		- crossover design
			- participants are randomly assigned to a time order of the treatments
				- treatment 1 $\to$ some time $\to$ treatment 2
				- treatment 2 $\to$ some time $\to$ treatment 1
		- matched pairs design
			- individuals are matched based on relevant variables
				- one will take treatment 1 the other treatment 2
	- paired-difference [[Academics/STATS/Intro to Stats/Test Statistics#T test\|t procedure]]
		- treat the observed differences as a single sample from a population of differences
			- one data using the difference between the 2
		- $\bar{X}\pm t_{\frac{\alpha}{2}}SE(\bar{X})$
			- $(1-\alpha)100\%$ confidence interval for the population mean difference $\mu$
			- $\bar{X}$= sample mean of the differences
			- $df = n-1$
				- $n$ is the number of differences
			- $SE(\bar{X})=\frac{s}{\sqrt{ n }}$
		- hypothesis
			- $H_{0}:\mu=\mu_{0}$ ; almost always $H_{0}:\mu=0$
				- difference between the 2 groups = 0 (theyre equal)
			- $t=\frac{\bar{X}-\mu_{0}}{SE(\bar{x})}$
			- 