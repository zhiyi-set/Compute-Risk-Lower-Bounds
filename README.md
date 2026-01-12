# Compute-Risk-Lower-Bounds
## Example 1 ($k$-ary symmetric channel)
Setting: 
* $\mathcal{W}=\{1,\dots, k\}$
* $\mu_W$ is uniform over $\mathcal{W}$
* for any $w,\widehat{w}\in\mathcal{W}$,
```math
  \mu_{\widehat W\mid W}(\widehat w\mid w)
  =
  \begin{cases}
  1-\epsilon, & \widehat w = w,\\
  \dfrac{\epsilon}{k-1}, & \widehat w \ne w.
  \end{cases}
```
* These imply that $\mu_{\widehat{W}}(\widehat{w})=\frac{1}{k}$ and $\bar{\mu}(w,\widehat{w})=\frac{1}{k^2}$. 
* Zero-one loss: $\ell(a,b)=\mathbb{1} [a-b]$.

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
