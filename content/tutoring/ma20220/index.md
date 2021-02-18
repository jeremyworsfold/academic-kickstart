---
type: talk
title: "Week 2: 09/02/21"
event: Tutoring
draft: true

summary: "Definitions and First order ODEs"
abstract: "The development"

# Talk start and end times.
date: "2021-02-09T10:15:00Z"
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: "2017-01-01T00:00:00Z"

authors: [admin]
tags: [odes]

# Is this a featured talk? (true/false)
featured: true



slides: ""



# Enable math on this page?
math: true
---

{{% toc %}}


## Problem sheet 1

The main point of these problems is to test your abilities

### Question 1




## Solving (in)homogeneous IVPs **(L2,L3)**

In lectures, it was presented to you that for the system of inhomogeneous ODEs $\dot{x}(t)=Ax(t) + {\color{CarnationPink}b(t)}$
the unique solution is given by:
$$
    \mathcal{L}\{x(t);s\} = (s\mathcal{I}-A)^{-1}(x_0 + \mathcal{B}(s)).
$$
In the types lecture notes **(L3)** you can see a quick derivation of where this comes from and I went over this in the tutorial so maybe take a quick look at that if you weren't there. In terms of how to implement this, below you can see a simple 4 step method of how to use the above theorem to solve specific examples.



Steps to find the solution for a system of homogeneous/{{< emph >}}inhomogeneous{{< /emph >}} IVPs using Laplace transforms. If the system is homogeneous you can ignore the bits which are in {{< emph >}}pink {{< /emph >}}.

Say we have 
$$\dot{x}(t)=Ax(t) + {\color{CarnationPink}b(t)}$$

1. Find $(s\mathcal{I}-A)^{-1}$
2. {{< emph >}} Find $\mathcal{B}(s) = \mathcal{L}\\\{b(t);s\\\}$ {{< /emph >}}
3.  Calculate $\mathcal{X}(s) = (s\mathcal{I}-A)^{-1}(x_0 {\color{darkcyan}+ \mathcal{B}(s)})$
4. Use the Laplace transform tables to find $x(t)$ s.t. $\mathcal{L}\\{x_i(t);s\\} = \mathcal{X}_i(s),\quad i=1,...,N$


When you get to step 3. and have two partial fraction decompositions to do where the denominators are the same, make your life easier by doing it generally like this from Q3a.
$$
    \mathcal{X}_1(s) = \frac{4s}{(s-3)(s+1)}, \quad \mathcal{X}_2(s) = \frac{2s +6}{(s-3)(s+1)}
$$

$$
    \mathcal{X}_i(s) = \frac{\alpha_i s +\beta_i}{(s-3)(s+1)}  = \frac{A_i}{s-3} + \frac{B_i}{s+1}, \quad i=1,2
$$
$$
    \alpha_i s + \beta_i = A_i(s+1) + B_i(s-3)
$$
$$
\begin{aligned}
    s=-1: & \quad \beta_i - \alpha_i = -4B_i \Rightarrow B_i = \frac{1}{4}(\alpha_i - \beta_i) \\\\\\
    s=3:  & \quad 3\alpha_i + \beta_i = 4A_i \Rightarrow A_i = \frac{1}{4}(3\alpha_i + \beta_i)
\end{aligned}
$$
Then substituting in for $\alpha_i$ and $\beta_i$,
$$
\begin{aligned}
    i=1: & \quad \alpha_i = 4, \beta_i=0 \Rightarrow \mathcal{X}_1(s) = \frac{3}{s-3} + \frac{1}{s+1} \\\\\\
    s=3: & \quad \alpha_i = 2, \beta_i=6 \Rightarrow \mathcal{X}_2(s) = \frac{3}{s-3} - \frac{1}{s+1}
\end{aligned}
$$