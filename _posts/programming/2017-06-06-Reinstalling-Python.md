---
layout: single
title:  "Reinstalling Python"
categories:
  - programming
tags:
  - python
  - brew
  - numpy
  - scipy
excerpt: The basic commands to get the SciPy stack up and running
#categories: programming python OSX
---
Often I find myself lost on everything I need to reinstall when using a fresh OSX installation. Assuming a preference for [homebrew](https://brew.sh/) over [anaconda](https://anaconda.org/) this should be a rigorous list
```bash
$ python3 -m pip install --upgrade pip
$ brew install numpy --with-python3
$ brew install scipy --with-python3
$ python3 -m pip install jupyter pandas matplotlib h5py
```

**Note:** If you don't have admin write access then use `install --user` instead.
{: .notice--warning}

**Python Version:** swap `python3` for `python` to the system's default version
{: .notice}
