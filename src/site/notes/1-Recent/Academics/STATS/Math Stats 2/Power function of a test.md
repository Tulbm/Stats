---
{"dg-publish":true,"dg-path":"Math Stats 2/Power function of a test.md","permalink":"/math-stats-2/power-function-of-a-test/","created":"2025-03-11T19:13:49.281-04:00","updated":"2025-07-07T17:32:42.530-04:00"}
---

The power function of a [[1-Recent/Academics/STATS/Math Stats 2/Test function\|test]] of $H_{0}: \theta \in \Theta_{0}$ against $H_{a}: \theta \in \Theta_{1}$
$$
\pi(\theta)=\begin{cases}
\alpha(\theta) & \text{for value of }\theta \text{ assumed under }H_{0} \\
1-\beta(\alpha) & \text{for value of }\theta \text{ assumed under }H_{a}
\end{cases}
$$
The power function is the probability of rejecting the $H_{0}$ for a given value of $\theta$, $\pi(\theta)=P(\text{reject }H_{0}|\theta)$
- at a single point, we can find the probability that our test will reject the null, $\alpha$ when $H_{0}$ is true, and $1-\beta$ when $H_{a}$ is true

Select a critical region that has a small $\alpha$ and largest power $(1-\beta)$ for the specific test being done

If a test satisfies $P(\text{reject }H_{0}|H_{0} \text{ is true})\leq\alpha$ then the test is called an $\alpha$ level significant test

An $\alpha$ level significant test with the smallest $\beta$ is called the **uniformly most powerful test** (UMPT)

When testing a simple null versus a simple alternative the [[1-Recent/Academics/STATS/Math Stats 2/Neyman-Pearson lemma\|N-P lemma]] gives the most powerful test

