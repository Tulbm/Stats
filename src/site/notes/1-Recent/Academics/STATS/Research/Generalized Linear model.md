---
{"dg-publish":true,"dg-path":"Research/Generalized Linear model.md","permalink":"/research/generalized-linear-model/","created":"2025-05-20T18:46:29.297-04:00","updated":"2025-07-07T17:32:53.483-04:00"}
---




# Iteratively Reweighted Least Square Algorithm

Likelihood functions for binomial regression

$$
P(Y=y;\pi)= \prod{m_{i}\choose y_{i}}\pi_{i}^{y_{i}}(1-\pi_{i})^{m_{i}-y_{i}}
$$
The likelihood and the log-likelihood function of $\pi$ are:
$$
\begin{align}
L(\pi;y,m) & = \prod \exp\left\{ y_{i}\log \frac{\pi_{i}}{1-\pi_{i}}+m_{i}\log(1-\pi_{i})+\log {m_{i}\choose y_{i}} \right\} \\
 & = \exp\left\{ \sum y_{i}\log \frac{\pi_{i}}{1-\pi _{i}}+m_{i}\log(1-\pi_{i})+\log {m_{i}\choose y_{i}} \right\} \\
l(\pi;y,m) & = \sum \left[ y_{i} \log \frac{\pi_{i}}{1-\pi_{i}}+m_{i}\log(1-\pi_{i})+\log {m_{i}\choose y_{i}} \right] \\
 & =\sum [y_{i}\theta_{i}-m_{i}\log(1+e^{\theta i})+c_{i}]
\end{align}
$$
Using the logistic link, we can re-parameterize the log0likelihood function fo $\pi$ to the log-likelihood of $\beta$

$$
\theta_{i}=g(\mu_{i})= \eta_{i} =\beta_{0}+\beta_{1}x_{i_{1}}+\dots+\beta _{p}x_{ip}= x_{i}^T \beta
$$

$$
\begin{align}
l(\beta ;x,y,m) & = \sum [y_{i} \eta_{i}-m_{i}\log(1+e^{\eta i}+c_{i})] \\
 & = \sum [ y_{i} x_{i}^T \beta - m_{i}\log(1+e^{x_{i}^T\beta})+c_{i}] \\
\end{align}
$$
Suppose $p+1<n$, we now have enough dfs

...
MLE of $\beta$

...


$$\begin{align}
\frac{ \partial l_{i} }{ \partial \theta_{i} }  & =\frac{y_{i}-b'(\theta_{i})}{a(\phi)}=\frac{y_{i}-\mu_{i}}{a(\phi)} \\
\frac{ \partial \theta_{i} }{ \partial \mu_{i} }  & = \frac{1}{\frac{ \partial \mu_{i} }{ \partial \theta_{i} } }= \frac{1}{b''(\theta_{i})}=\frac{1}{v(\mu_{i})} \\
\frac{ \partial \eta_{i} }{ \partial \beta_{j} }  & =\frac{ \partial  }{ \partial \beta_{j} } \beta_{0}+\beta_{1}X_{i_{1}}+\dots+B_{p}X_{ip}=x_{ij} \\
\text{Let }W_{i} & = \frac{1}{V(\mu_{i})}\left( \frac{ \partial \mu_{i} }{ \partial \eta_{i} }  \right)^{2}\\
\frac{ \partial l_{i} }{ \partial \beta_{j} }  & = \frac{y_{i}-\mu_{i}}{a(phi)}
\end{align}
$$


Information matrix

$$
\begin{align}I(\beta)_{rs} & =-\left[ \frac{ \partial S }{ \partial \beta }  \right]_{rs} = - \frac{ \partial^{2}l }{ \partial \beta_{r}\partial \beta_{s} }= - \frac{ \partial  }{ \partial \beta_{s} }  \sum (y_{i}-\mu_{i}) W_{i} \frac{ \partial \eta_{i} }{ \partial \mu_{i} }x_{ir} \\
 & = - \sum \left[  \frac{ \partial  }{ \partial \beta s } \frac{ \partial  }{ \partial \beta_{s} } (y_{i}-\mu_{i})w_{i} \frac{ \partial \eta_{i} }{ \partial \mu_{i} } x_{ir} + (y_{i}-\mu_{i})\frac{ \partial  }{ \partial \beta_{s} } \left( W_{i}\frac{ \partial \eta_{i} }{ \partial \mu_{i} } x_{i} \right) \right]
\end{align}
$$

The fisher 
$$\begin{align}
\mathcal{I} (\beta) & = -E(H(\beta)) \\
E(\mathcal{I} (\beta)_{r,s}) & =- \sum E\left( \frac{ \partial  }{ \partial \beta_{s} } (y_{i}-\mu_{i})w_{i} \frac{ \partial \eta_{i} }{ \partial \mu_{i} } x_{ir} \right)+ E  (y_{i}-\mu_{i})\frac{ \partial  }{ \partial \beta_{s} } \left( W_{i}\frac{ \partial \eta_{i} }{ \partial \mu_{i} } x_{i} \right)
\end{align}
$$

Now we have
$$
\beta^{(k+1)}=
$$
Multiply both sides by 
$$\begin{align}
\mathcal{I}_{\beta^{(k)}}\beta^{(k+1)}  & = \mathcal{I}_{\beta^{(k)}}\beta^{(k)}+S(\beta^{)k}) \\
\mathcal{I}(\beta^{(k)})\beta^{(k)} & = \begin{pmatrix}
\sum w_{i}^{(k)} x_{i_{0}}\eta_{i}^{(k+1)} \\
\dots \\
\sum w_{i}^{(k)}x_{ip}\eta_{i}^{(k+1)}
\end{pmatrix} \\
 & =\begin{pmatrix} 
\end{pmatrix}
\end{align}
$$

...

$$\begin{align}
\beta^{(k+1)} & =(X'W^{(k)}X)^{-1}X^TW^{(k)Z^{(k)}} \\
\text{with }W^{(k)} & = \begin{pmatrix}
W_{1}^{(k)} & 0 & 0\dots & 0 \\
0 & W_{2}^{(k)}  & 0\dots & 0 \\
\dots  &  &  & W_{p}^{(k)}
\end{pmatrix}
\end{align}
$$
$$
\pi \underline{\sim}
$$

$$
\pi _\text{}
$$