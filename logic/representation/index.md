---
layout: post
title: Propositional Logic
---

### 2-SAT

1. \$$\Gamma\leftarrow KB$$
1. while $$\Gamma$$ is not empty do:
    1. \$$L\leftarrow\text{pick a literal from }\Gamma$$
    1. \$$\Delta\leftarrow\text{UP}(\Gamma,L)$$
    1. if $$\{\}\in\Delta$$ then
        1. \$$\Delta\leftarrow\text{UP}(\Gamma,\neg L)$$
        1. if $$\{\}\in\Delta$$ then return unsatisfiable
    1. \$$\Gamma\leftarrow\Delta$$
1. Return satisfiable


- \$$\Gamma\leftarrow KB$$
- while $$\Gamma$$ is not empty do:
    - \$$L\leftarrow\text{pick a literal from }\Gamma$$
    - \$$\Delta\leftarrow\text{UP}(\Gamma,L)$$
    - if $$\{\}\in\Delta$$ then
        - \$$\Delta\leftarrow\text{UP}(\Gamma,\neg L)$$
        - if $$\{\}\in\Delta$$ then return unsatisfiable
    - \$$\Gamma\leftarrow\Delta$$
- Return satisfiable


inequalities hold for the transition probabilities:

$$
\begin{eqnarray*}
P[X_{t+1}=j+1\mid X_{t}=j] & \geq & \frac{1}{2}\\
P[X_{t+1}=j-1\mid X_{t}=j] & \leq & \frac{1}{2}
\end{eqnarray*}
$$


By Stirling's approximation, $${3j \choose j} = \frac{(3j)!}{(2j)!j!}$$
so 

\$$
\begin{eqnarray*}
{3j \choose j} & = & \frac{(3j)!}{(2j)!j!}\\
 & \geq & \frac{c\sqrt{2\pi3j}}{\sqrt{2\pi j}\sqrt{2\pi2j}}(\frac{3j}{e})^{3j}(\frac{e}{2j})^{2j}(\frac{e}{j})^{j}\\
 & = & \frac{a}{\sqrt{j}}(\frac{27}{4})^{j}
\end{eqnarray*}
$$

$$
\begin{eqnarray*}
{3j \choose j} & = & \frac{(3j)!}{(2j)!j!}\\
 & \geq & \frac{c\sqrt{2\pi3j}}{\sqrt{2\pi j}\sqrt{2\pi2j}}(\frac{3j}{e})^{3j}(\frac{e}{2j})^{2j}(\frac{e}{j})^{j}\\
 & = & \frac{a}{\sqrt{j}}(\frac{27}{4})^{j}
\end{eqnarray*}
$$

\$$
\begin{eqnarray*}
{3j \choose j} & = & \frac{(3j)!}{(2j)!j!}\\
 & \geq & \frac{c\sqrt{2\pi3j}}{\sqrt{2\pi j}\sqrt{2\pi2j}}(\frac{3j}{e})^{3j}(\frac{e}{2j})^{2j}(\frac{e}{j})^{j}\\
 & = & \frac{a}{\sqrt{j}}(\frac{27}{4})^{j}
\end{eqnarray*}
$$
{: style="text-align: center"}

for $$j>0$$. Combining this bound with our previous expression, $$q_{j}\geq\frac{a}{\sqrt{j}}(\frac{1}{2})^{j}$$
for $$j>0$$. The boundary condition is $$q_{0}=1$$.