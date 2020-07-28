![My Python app](https://github.com/panchul/Pytest-Actions-Demo/workflows/My%20Python%20app/badge.svg)
# Skeleton code for a Python application

See also my Python sanbdox [https://github.com/panchul/sb_python](https://github.com/panchul/sb_python)

## Prerequisites

You will need:

- have GitHub account
- enable Actions in your repository
- `pytest` Python package, if you already do not have it, install it with, for example, pip:

    $ pip3 install pytest flake8

## demo app

File demo.py contains a code for `factorial()` function. (so, the whole thing is a package, not an app, btw)

## local unit testing

File `test_demo.py` has a few tests to make sure the `factorial()` function works correctly.

To test the code from command line, run `pytest -v`. On Mac it looks like this:

    $ pytest -v
    ======================================================================= test session starts ============
    platform darwin -- Python 3.7.7, pytest-5.4.1, py-1.8.1, pluggy-0.13.1 -- /Users/path/anaconda3/bin/python
    cachedir: .pytest_cache
    hypothesis profile 'default' -> database=DirectoryBasedExampleDatabase('/Users/path/Pytest-Actions-Demo/.hypothesis/examples')
    rootdir: /Users/path/Pytest-Actions-Demo
    plugins: arraydiff-0.3, remotedata-0.3.2, hypothesis-5.8.3, openfiles-0.5.0, doctestplus-0.5.0, astropy-header-0.1.2
    collected 10 items                                                                                                                                                 
    
    test_demo.py::test_fact_0 PASSED        [ 10%]
    test_demo.py::test_fact_1 PASSED        [ 20%]
    test_demo.py::test_fact_2 PASSED        [ 30%]
    test_demo.py::test_fact_3 PASSED        [ 40%]
    test_demo.py::test_fact_10 PASSED       [ 50%]
    test_demo.py::test_fact_20 PASSED       [ 60%]
    test_demo.py::test_fact_30 PASSED       [ 70%]
    test_demo.py::test_fact_40 PASSED       [ 80%]
    test_demo.py::test_fact_50 PASSED       [ 90%]
    test_demo.py::test_fact_minus1 PASSED   [100%]
    
    ======================================================================== 10 passed in 0.05s ==================
    (base) apanchul@swing Pytest-Actions-Demo % ls

## Github push

With the `.github/workflows/pytest.yml`, you will have automated testing via Github Actions service.

After every commit, visit the Actions tab and review the results of automated linting and testing.

The status of your workflow can be embedded using the link to the badge:

`![My Python app](https://github.com/panchul/Pytest-Actions-Demo/workflows/My%20Python%20app/badge.svg)`

( Which looks like this: ![My Python app](https://github.com/panchul/Pytest-Actions-Demo/workflows/My%20Python%20app/badge.svg) )

Or, with explicit branch and event:

`![My Python app](https://github.com/panchul/Pytest-Actions-Demo/workflows/My%20Python%20app/badge.svg?branch=master&event=push)`

![My Python app](https://github.com/panchul/Pytest-Actions-Demo/workflows/My%20Python%20app/badge.svg?branch=master&event=push)


## Links:

 * https://realpython.com/pytest-python-testing/
 * https://docs.github.com/en/actions/language-and-framework-guides/using-python-with-github-actions
 * https://flake8.pycqa.org/en/latest/
 * https://vak.dreamwidth.org/657802.html
