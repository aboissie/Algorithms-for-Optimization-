# TP1 : Minimisation de fonctions quadratiques

## Exercice 0: Exemple explicite

1. If f is *convex*, then $\forall x \in \mathbb{R}^n$, $x \cdot Qx \geq 0$. We have:

$$x \cdot Qx = \frac{1}{2}(\lambda_1 x_1^2 + \lambda_2 x_2^2)$$

$\texttt{WLOG}$ suppose $\lambda_1 = -1$: 
- If $\lambda_2 = 0$: consider $x=(1, 0)$, then $f$ is not convex
- Otherwise: consider $x=(1, \frac{1}{\sqrt{2 \lambda_2}})$ if $\lambda_2 > 0$ and $x=(1, 0)$ otherwise.

Reciprocally, if $\lambda \geq 0$, $x \cdot Qx \geq 0$ since, $x_1^2 \geq 0$, 
$x_2^2 \geq 0$.

2. $\texttt{WLOG}$ suppose $\lambda_1 < 0$. Then consider $x = (t, 0)$. We can see that $\lim_{t\rightarrow\infty} f(x) = - \infty$, and $f$ is not bounded.

3. $\nabla f(x^{*}) = \lambda_1 x_1^{*} + \lambda_2 x_2^{*} = 0$. Additionally, when $\lambda \geq 0$, we know that $\nabla^{2} f \geq 0$, so therefore, it can be stated that $x^{*}$ is a global minimizer. In all other cases, $\nabla^{2} f $ is not a SDP matrix, so it is not possible to state whether $x^{*}$ is a global minimizer.