# Compute-Risk-Lower-Bounds
## Example 1 ($k$-ary symmetric channel)
### Setting: 
* $\mathcal{W}=\{1,\dots, k\}$
* $\mu_W$ is uniform over $\mathcal{W}$
* for any $w,\widehat{w}\in\mathcal{W}$,
```math
  \mu_{\widehat W\mid W}(\widehat w\mid w)=
  \begin{cases}
  1-\epsilon, & \widehat w = w,\\
  \dfrac{\epsilon}{k-1}, & \widehat w \ne w.
  \end{cases}
```
* These imply that $\mu_{\widehat{W}}(\widehat{w})=\frac{1}{k}$ and $\bar{\mu}(w,\widehat{w})=\frac{1}{k^2}$. 
* Zero-one loss: $\ell(a,b)=\mathbb{1} [a\neq b]$.

### Bounds in this setting:
KL divergence:
```math
  R_{\rm chen} =
  \begin{cases}
  0 ,& 1-\frac{1+\sqrt{1-\exp(-2I(W,\widehat{W}))}}{2}\leq \frac{1}{k}  \\
  \frac{1}{2},&   otherwise\\
  \end{cases}
```
```math
R_{\rm int}=R_{\rm mkv}=R_{0-1}=1-\eta_f\left(I(W;\widehat{W})\Vert \frac{1}{k}\right)
\geq 1-\frac{I(W;\widehat{W})+\log(2-\frac{1}{k})}{\log k}
```
TV distance:
```math
  R_{\rm chen} =
  \begin{cases}
  0 ,& 1-\min\left\{1,\; J_{\rm TV}(W,\widehat{W})+\frac{1}{2}\right\} \leq \frac{1}{k} \\
  \frac{1}{2},&   otherwise\\
  \end{cases}
```
```math
R_{\rm int}=R_{\rm mkv}=R_{0-1}= 1-\min\left\{1,\; I_{\rm TV}(W,\widehat{W})+\frac{1}{k}\right\} 
```

Chi2 divergence:
```math
  R_{\rm chen} =
  \begin{cases}
  0 ,& 1- \frac{1}{2}\left(1+\sqrt{\frac{J_{\mathcal{X}^2}(W,\widehat{W})}{1+J_{\mathcal{X}^2}(W,\widehat{W})}}\right)\leq \frac{1}{k} \\
  \frac{1}{2},&  otherwise\\
  \end{cases}
```
```math
R_{\rm int}=R_{\rm mkv}=R_{0-1}= 1-\sqrt{\frac{1}{k}\left(1-\frac{1}{k}\right)I_{\mathcal{X}^2}(W,\widehat{W})}-\frac{1}{k}
```

## Example 2 (Additive Gaussian noise channel)
Setting: 
* $W\sim \mathcal{N}(0,1)$
* $\widehat{W}=\rho W+\sqrt{1-\rho^2} Z$ where $Z\sim \mathcal{N}(0,1)$, $Z\perp W$ and $\rho \in [0,1)$. 
* These imply that, $\mu=\mathcal{N}(0,\Sigma_\rho)$ where
```math
\Sigma_\rho=\begin{bmatrix}1 & \rho \\\rho & 1\end{bmatrix}
```
* and $\bar{\mu}=\mathcal{N}(0,\mathbf{I})$.
* Mean squared error: $\ell(a,b)=(a-b)^2$.
