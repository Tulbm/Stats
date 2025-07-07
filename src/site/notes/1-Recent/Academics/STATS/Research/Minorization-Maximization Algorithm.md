---
{"dg-publish":true,"dg-path":"STATS/Research/Minorization-Maximization Algorithm.md","permalink":"/stats/research/minorization-maximization-algorithm/","created":"2025-06-03T18:32:39.445-04:00","updated":"2025-07-07T17:32:53.509-04:00"}
---



Surrogate function
$$
M(\theta _{m}|\theta _{m})=f(\theta _{m})
$$
then find $\theta _{m+1}=argmax\, M(\theta)$ such that $m(\theta|\theta _{m+1})=f(\theta _{m+1})$

## Beta binomial Regression Example

$$
Y_{i} \sim Binomial(m_{i},p _{i})
$$
where $Y_{i}$ is a count variable  
$$
E(Y_{i})=m_{i}p_{i}, \quad Var(Y_{i})=m_{i}p_{i}(1-p_{i})
$$

and $p _{i}$ is assumed to follow a [[1-Recent/Academics/STATS/Math Stats 1/Beta Distribution\|Beta Distribution]] $(\alpha _{i_{1}},\alpha _{i_{2}})$

$$
E(p_{i})=\frac{\alpha _{i_{1}}}{\alpha _{i_{1}}+\alpha _{i_{2}}}= \frac{\alpha _{i_{1}}}{\alpha _{i+}}
$$
$$
Var(p_{i})= \frac{\alpha _{i_{1}}\alpha _{i_{2}}}{\alpha _{i+}^{2}(1+\alpha _{i+})^{2}}
$$

$Var(p_{i})$ dependds on the size of $\alpha _{i_{1}}$ and $\alpha _{i_{2}}$

Beta Binomial distribution of $Y$ and $p_{i}$

$$\begin{align}
f_{B B} (y_{i};\underset{\sim}{\alpha _{i}}) & =\int_{p_{i}} f_{Bin}(y_{i};p_{i})f_{Beta}(p_{i};\alpha _{i}) \, dx \\

\end{align} 
$$

$$
= \frac{m_{i}!}{y_{i}!(m_{i}-y_{i})!} \frac{\Gamma(\alpha _{i+})}{\Gamma(\alpha _{i_{1}})\Gamma(\alpha _{i_{2}})} \frac{\Gamma(y_{i}+\alpha _{i_{1}})\Gamma(m_{i}-Y_{i}+\alpha _{i_{2}})}{\Gamma(m_{i}+\alpha _{i+})}
$$

The mean and variance of the $Y_{i}$ with the BB distribution are then given by
$$
E(Y_{i})=E(E(Y_{i}|p_{i}))=E(m_{i}p_{i})=m_{i} \frac{\alpha _{i_{1}}}{\alpha _{i+}}
$$
$$\begin{align}
Var(Y_{i}) & =Var(E(Y_{i}|p_{i}))+E(Var(Y_{i}|P_{i}))=Var(m_{i}p_{i})+E(m_{i}p_{i}(1-p_{i})) \\
 & = m_{i}^{2} \frac{\alpha _{i_{1}}\alpha _{i_{2}}}{\alpha _{i+}^{2}(1+\alpha _{i+}^{2})}+E(m_{i}p_{i})-E(m_{i }p_{i}^{2}) \\
 & =m_{i} \frac{\alpha _{i 1}}{\alpha _{ i +}} \left( 1- \frac{\alpha _{i 1}}{\alpha _{i+}} \right) \frac{m_{i }+\alpha _{i 1}}{1+ \alpha _{i+}}
\end{align}
$$
$$
L(\underset{\sim}{\beta};x_{i})=f_{B B}(y_{i};\alpha _{i})
$$
$y_{i 1}$ is the number of successes on the sample $m_{i}$
$$
l(\underset{\sim}{\beta})=\sum \log f_{B B }(y_{i};\underset{\sim}{\beta})= \sum_{i=1}^{n} \left[ \sum_{l=0}^{y_{i 1}-1} \log (e^{x_{i}\beta+l}) +\sum _{l=0}^{m_{i}-y_{i}-1} \log(e^{})  \right]
$$

the negative log is not concave

In the application of Jensen's inequality, for a concave function $\phi(\cdot)$ with contants $a$'s 

$$
a_{1}=\exp (\underset{\sim}{x_{i}})
$$

Surrogate of the first function $f_{1}$
$$
\log(e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{i}}}+l)=\log (a_{1}v_{1}+a_{2}v_{2}) \geq a_{1}\log v_{1}+a_{2}  \log v_{2}
$$
$$
=\exp(\underset{\sim}{x_{i}}\beta)
$$

Surrogate of the second function 
$$
f_{2}(\beta)=- \sum_{i=1}^{n}\sum_{l=0}^{m_{i}-1}\log (e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{i}}}+e^{\underset{\sim}{x_{i}\underset{\sim}{\beta _{2}}}}+l)
$$
because $log(\cdot)$ is concave, $-log(\cdot)$ is convex, choose $\phi(\cdot)=-log(\cdot)$
$$\begin{align}
\log(v) & =-\log (e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{i}}}+e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{2}}}+l) \\
 & \geq -\log(v^{(t)})+ \frac{d(-log(v))}{dv}|_{v=v^{(t)}}(v-v^{(t)}) \\
 & = -\log(v^{(t)})- \frac{1}{v^{(t)}} (v-v^{(t)}) \\
 & =-\log (e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{i}}}+e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{2}}}+l) - \frac{e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{i}}}+e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{2}}}-e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{i}}^{(t)}}-e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{2}}^{(t)}}}{e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{i}}^{(t)}}+e^{\underset{\sim}{x_{i}}\underset{\sim}{\beta _{2}}^{(t)}}+l}  \\
f_{2}(\underset{\sim}{\beta })  & \geq g_{2}(\underset{\sim}{\beta}|\underset{\sim}{\beta}^{(t)})= - \sum_{\alpha=1 }^{2} \sum_{i=1}^{n} \sum_{l=0 }^{m_{i}-1} \exp(\underset{\sim}{x_{i}}\underset{\sim}{\beta _{d}})
\end{align}
$$

In combination we have a surrogate function $g(\beta)$ for the objective $f(\beta)$ as
$$\begin{align}
f(\underset{\sim}{\beta}) & =f_{1}(\beta)+f_{2}(\beta)\geq g(\underset{\sim}{\beta}|\underset{\sim}{\beta}^{(t)})=g_{1}(\underset{\sim}{\beta}|\underset{\sim}{\beta}^{(t)})+g_{2}(\underset{\sim}{\beta}|\underset{\sim}{\beta}^{(t)}) \\
 & = \sum _{\alpha=1 }^{2}\sum_{i=1}^{n}\left( \sum_{l=0}^{y_{id}-1} \frac{\exp(\underset{\sim}{x_{i}}\beta _{d}^{(t)})}{\exp(\underset{\sim}{x_{i}}\underset{\sim}{\beta _{d}^{(t)}})+l} \underset{\sim}{x_{i}} \beta _{d}+ \sum_{l=0}^{m_{i}-1} \frac{1}{\sum_{d=1 }^{2}\exp(\underset{\sim}{x_{i}}\underset{\sim}{\beta _{d}^{(t)}})+l}\exp(\underset{\sim}{x_{i}}\underset{\sim}{\beta _{d}}) \right) + C^{(t)} \\
 & = \left[ \sum_{\alpha=1}^{2}\sum_{i=1 }^{n} W_{i}^{(t)} ( y_{id}^{*(t)}\underset{\sim}{x_{i}}\underset{\sim}{\beta _{d}} - \exp(\underset{\sim}{x_{i}}\underset{\sim}{\beta _{d}})) \right] + c^{(t)}
\end{align}
$$


