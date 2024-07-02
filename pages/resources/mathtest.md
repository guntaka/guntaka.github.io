---
layout: default
title: Test Page
permalink: /resources/math-test-page
---

<script type="text/javascript" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
# MathJax
## A complex mathematical formuala using MathJax

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$


## Unit Circle
### Distance between the point on circle and tangent line to x-intercept

$$
\begin{align*}
Tangent & = \sqrt { \left( {1 \over a} - a \right)^2 + \left( 0 - b \right)^2 } \\
& = \sqrt { \left( {1 \over a^2 } - {2a \over a} +a^2 \right)  + b^2} \\
& = \sqrt { {1 \over a^2} - 2 + (a^2 + b^2 ) } \\
& = \sqrt { {1 \over a^2} - 2 + 1} \\
& = \sqrt { {1 \over a^2} -  1} \\
& = \sqrt { (1 - a^2) \over a^2 } \\
& =\sqrt { b^2 \over a^2 } \\
& = { b \over a }
\end{align*}
$$
