---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/Percentiles.md","permalink":"/stats/intro-to-stats/percentiles/","created":"2024-04-19T18:16:21.587-04:00","updated":"2025-07-07T17:21:02.392-04:00"}
---


- The pth percentile is the value of the variable such that p% of the ordered data values are less than or equal to this value
	- ![](https://i.imgur.com/pnnJF9t.png)
	- Empirical Cumulative Distribution Function (ECDF)
		- all values <= percentile
		- 510 = 78th percentile
		- ![](https://i.imgur.com/PZgHh0x.png)
	- quartiles
		- Q1 = 25th percentile
		- Q2 = median = 50th percentile
		- Q3 = 75th percentile
	- five-number summary
		- listing of minimum,Q1,median,Q3,maximum
		- boxplot = a plot of the number summary
			- jittered boxplot
				- all sample points appear on the plot
			- whiskers always stop at a value in the dataset
				- cannot be bigger than 1.5xIQR
				- values bigger than that are outliers
			- large samplesize = more outliers, while the plot stays the same
				- can lead to false conclusions
				- keep in mind that ~1% will be outliers
			- ![](https://i.imgur.com/erXBWY8.png)
	- Interquartile Range (IQR)
		- IQR = Q3 - Q1
		- a descriptive measure of variability