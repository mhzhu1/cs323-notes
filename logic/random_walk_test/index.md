---
layout: post
title: 'Inference - random walk satisfiability solvers'
---



In either the case where one of the variables is set
incorrectly or both of the variables are set incorrectly, the following
inequalities hold for the transition probabilities:

$$\begin{aligned}
P[X_{t+1}=j+1\mid X_{t}=j] & \geq & \frac{1}{2}\\
P[X_{t+1}=j-1\mid X_{t}=j] & \leq & \frac{1}{2}\end{aligned}$$

for any 