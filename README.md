
[![codecov](https://codecov.io/gh/sarajahedazad/Newton-Solver/graph/badge.svg?token=gjTEpB0RtP)](https://codecov.io/gh/sarajahedazad/Newton-Solver)
[![Run Tests](https://github.com/sarajahedazad/Newton-Solver/actions/workflows/test.yml/badge.svg)](https://github.com/sarajahedazad/Newton-Solver/actions/workflows/test.yml)
---
### Table of contents


---
# Newton Solver

This repository provides an implementation of [Newton's method](https://en.wikipedia.org/wiki/Newton%27s_method) (also known as the Newton–Raphson method) for finding roots (zeros) of functions or systems of equations. Newton's method is an iterative algorithm commonly used in numerical analysis and scientific computing.

## What is Newton's Method?

Newton's method is designed to find solutions to the equation $F(x) = 0$. It uses the first-order Taylor expansion to generate iterative approximations of the root. For a single variable, each iteration is:


$x_{k+1} = x_k - \frac{F(x_k)}{F'(x_k)}$


For multiple variables, the concept extends using the Jacobian matrix $J(x)$:

$x_{k+1} = x_k - J(x_k)^{-1} F(x_k)$

By iterating this process, we often converge quickly (quadratically, near the root) to a solution, given a good initial guess and certain regularity conditions on $ F $.


---

### Conda environment, install, and testing <a name="install"></a>
This section is entirely come and pasted from [Lejeune's Lab Graduate Course Materials: Bisection Method](https://github.com/Lejeune-Lab-Graduate-Course-Materials/bisection-method.git)

To install this package, please begin by setting up a conda environment (mamba also works):
```bash
conda create --name newton-solver-env python=3.12
```
Once the environment has been created, activate it:

```bash
conda activate newton-solver-env
```
Double check that python is version 3.12 in the environment:
```bash
python --version
```
Ensure that pip is using the most up to date version of setuptools:
```bash
pip install --upgrade pip setuptools wheel
```
Create an editable install of the bisection method code (note: you must be in the correct directory):
```bash
pip install -e .
```
Test that the code is working with pytest:
```bash
pytest -v --cov=newtonsolver --cov-report term-missing
```
Code coverage should be 100%. Now you are prepared to write your own code based on this method and/or run the tutorial. 


If you are using VSCode to run this code, don't forget to set VSCode virtual environment to bisection-method-env.

If you would like the open `tutorial_newton_solver.ipynb` located in the `tutorials` folder as a Jupyter notebook in the browser, you might need to install Jupyter notebook in your conda environment as well:
```bash
pip install jupyter
```
```bash
cd tutorials/
```
```bash
jupyter notebook tutorial_newton_solver.ipynb
```
### An alternative way to try the implemented Newton's method
Download the `newton_solver.py` file from the folder `src/newtonsolver`([here](https://github.com/sarajahedazad/Newton-Solver/tree/main/src/newtonsolver)). Place it in the same folder as your working directory. You can find the path to that folder by typing `pwd` in your terminal. Create a `.py` file that 
---
