---
title: "MA20221 Week 2"
summary: "Definitions and First order ODEs"
authors: [admin]
tags: [ma20220]
categories: [odes]
date: 2020-12-14T21:44:52Z
lastmod: 2020-12-14T21:44:52Z
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: night
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula
---

# MA20221 Week 2

## Definitions


---

## What makes a well posed problem?

- {{% fragment %}}solution exists (for at least as long as the prediction is required){{% /fragment %}}
- {{% fragment %}}the solution is unique{{% /fragment %}}
- {{% fragment %}}the solution depends continuously on the initial condition and model parameters{{% /fragment %}}

---
## What is a positively invariant set?

A set $Y \subset X$ is positively invariant if $x(0) \in Y$ implies that $x(t) \in Y$ for all $t \in T$ with $t > 0$. (It
is negatively invariant if the same is true for all $t \in T$ with $t < 0$.)


---

## Stability

- Steady state: {{% fragment %}}$x^\*$, is where $f(x^\*)=0${{% /fragment %}}
- Stable: {{% fragment %}}for any $\epsilon > 0$ there exists $\delta > 0$ such that $|x(t) − x^\*| < \epsilon$ for all positive $t \in T$ whenever $|x_0 − x^\*| < \delta$, and unstable otherwise.{{% /fragment %}}
- Asymptotically stable: {{% fragment %}}if it is stable and there exists $\delta > 0$ such that $|x− x^\*| \rightarrow 0$ as $t → \infty$ whenever $|x_0 − x^\*| < \delta$.{{% /fragment %}}
- {{% fragment %}} stable: start close, stay close. asym. stable: start close, converge to steady state. {{% /fragment %}}

---

### Time dependent solution

If $\frac{dx}{dt}=f(x)$ and $f(x_0)\neq0$, then
$$
t = \int_{x_0}^{x(t)}\frac{ds}{f(s)}
$$
- If $x(t)$ is not a steady state, $x^\*$,then it either tends to a steady state or it tends to $\pm\infty$
- If the model system is well-posed, then $x(t)$ must either be a steady state solution, $x^\*$, or strictly monotonic.