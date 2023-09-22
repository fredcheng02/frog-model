## Repository for the 2023 Polymath Jr. frog model project

This repository contains code used to exactly compute and estimate the upper bounds to $S_m \coloneqq \sup_{d \geq m} p_d$ in the paper. We use SageMath in Jupyter Notebook for symbolic and numeric computation.

To run `exact-Sm-bound-finder.ipynb`, one also needs to install Mathematica on the computer, and set things up to call Mathematica function `CountRoots` within SageMath. To know how to do this please run `print(mathematica._install_hints())` in SageMath. This [documentation link](https://doc.sagemath.org/html/en/reference/interfaces/sage/interfaces/mathematica.html) can be helpful.

For $2 \leq m \leq 13$ The exact bounds are listed in the table below. If you run the code and look at the explanation included, you will see these are optimal upper bounds on $p_m$ that results from the *boostrapping argument*.

|     $m$   |$S_m \leq$|
|:---------:|:--------:|
|     2     | 55/159   |
|     3     | 42/145   |
|     4     | 40/153   |
|     5     | 23/94    |
|     6     | 46/197   |
|     7     | 23/102   |
|     8     | 38/173   |
|     9     | 20/93    |
|    10     | 15/71    |
|    11     | 5/24     |
|    12     | 7/34     |
|    13     | 11/54    |

Due to the precision limitation of `find_root` in SageMath (which uses Brent's method), the technique developed to compute exact upper bounds to $S_m$ cannot go beyond $m = 13$. However, with the distribution of $U(m)$ in hand and some additional observations, we may approximate the upper bounds to $S_m$ numerically for arbitrarily high $m$. See the code and explanantion in `approx-Sm-bound-finder.ipynb` for detail.

See the plot below for the overall trend of these upper bounds on $S_m$.

![](https://github.com/fredcheng02/frog-model/blob/main/plot_of_upper_bounds_git.png?raw=true)

Using the method introduced in `approx-Sm-bound-finder.ipynb`, we observe that $q_d$ (introduced in the paper) becomes approximately less than 1.8 for the first time when $d = 230$. The rate of convergence of $q_d$ (introduced in the paper) is really slow.
