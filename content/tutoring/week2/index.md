---
type: talk
title: "Week 2: 16/02/22"
event: Tutoring
draft: false

summary: "Definitions and First order ODEs"

# Talk start and end times.
date: "2023-02-16T17:15:00Z"
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: "2023-02-14T00:00:00Z"

authors: [admin]
tags: [odes]

# Is this a featured talk? (true/false)
featured: true

slides: "ma20221week2"

# Enable math on this page?
math: true
---

{{% toc %}}

## Outline of lecture content

### What makes a well posed problem?

- solution exists (for at least as long as the prediction is required)
- the solution is unique
- the solution depends continuously on the initial condition and model parameters

### What is a positively invariant set?

A set $Y \subset X$ is positively invariant if $x(0) \in Y$ implies that $x(t) \in Y$ for all $t \in T$ with $t > 0$. (It
is negatively invariant if the same is true for all $t \in T$ with $t < 0$.)


### Stability

- Steady state: $x^\*$, is where $f(x^\*)=0$
- Stable: for any $\epsilon > 0$ there exists $\delta > 0$ such that $|x(t) − x^\*| < \epsilon$ for all positive $t \in T$ whenever $|x_0 − x^\*| < \delta$, and unstable otherwise.
- Asymptotically stable: if it is stable and there exists $\delta > 0$ such that $|x− x^\*| \rightarrow 0$ as $t → \infty$ whenever $|x_0 − x^\*| < \delta$.
- stable: start close, stay close. 
- asym. stable: start close, converge to steady state.

### Time dependent solution

If $\frac{dx}{dt}=f(x)$ and $f(x_0)\neq0$, then
$$
t = \int_{x_0}^{x(t)}\frac{ds}{f(s)}
$$
- If $x(t)$ is not a steady state, $x^\*$,then it either tends to a steady state or it tends to $\pm\infty$
- If the model system is well-posed, then $x(t)$ must either be a steady state solution, $x^\*$, or strictly monotonic.
