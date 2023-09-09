## Repository for the 2023 Polymath Jr. frog model project

This repository contains code used to exactly compute and estimate the upper bounds to $S_m \coloneqq \sup_{d \geq m} p_d$ in the paper. We use SageMath in Jupyter Notebook for symbolic and numeric computation.

To run the exact S_m finder, one also needs to install Mathematica on the computer, and set things up to call Mathematica function `CountRoots` within SageMath. To know how to do this please run `print(mathematica._install_hints())` in SageMath. This [documentation link](https://doc.sagemath.org/html/en/reference/interfaces/sage/interfaces/mathematica.html) can be helpful.

For $2 \leq m \leq 13$ The exact bounds are listed in the table below.

|     $m$   |$S_m \leq$| $\max g(y) \approx$ |
|:----------|:---------|:----------|
|     2     | 55/159   | Cell 3    |
|     3     | 42/145   | Cell 3    |
|     4     | 40/153   | Cell 3    |
|     5     | 23/94    | Cell 3    |
|     6     | 46/197   | Cell 3    |
|     7     | 23/102   | Cell 3    |
|     8     | 38/173   | Cell 3    |
|     9     | 20/93    | Cell 3    |
|    10     | 15/71    | Cell 3    |
|    11     | 5/24     | Cell 3    |
|    12     | 7/34     | Cell 3    |
|    13     | 11/54    | Cell 3    |

Due to the precision limitation of `find_root` in SageMath (which uses Brent's method), the technique developed to compute exact upper bounds to $S_m$ cannot go beyond $m = 13$. However, with the distribution of $U(d)$ in hand and some additional observations, we may approximate the upper bounds to $S_m$ numerically for arbitrarily high $m$'s.
