# Quadratic equations solver

If you have an equation of the form `ax2 + bx + c = 0`, this module can solve it for you.
Just enter the values of a, b and c as parameters.

# How to use

Example of script launch on Linux, Python 3.5:

```bash
$ python3

>>> import quadratic_equation 

>>> quadratic_equation.get_roots(1, -1, -6) 
(-2.0, 3.0)
```

# How to Launch Unit Tests

```bash
$ python3 tests.py

....
----------------------------------------------------------------------
Ran 4 tests in 0.001s

OK
```

# How to use auto-tests

This project includes pre-commit script, which makes pre-commit tests.

For auto-test usage one should:
* make pre-comit file executable, executing the following command:
```bash
chmod +x pre-comit
```
* copy pre-comit file to `.git/hooks` directory of your local repository.

Auto-test executes `tests.py` before commit, and if failed, it rejects commitment.


## Example of failed test

```bash
$ git commit -m '<comment>'

ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "/Users/User/devman/problem14/14_pre_commit_hook/quadratic_equation.py", line 6, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error
----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (errors=1)
> Unit tests didn't pass. Commit rejected.
```


# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)







