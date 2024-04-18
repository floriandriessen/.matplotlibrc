
# Overview

These settings can be called within a Python script to change the default matplotlib settings when generating a plot. Instead of customising within the user Python script, the default Python settings are overwritten when calling some style file(s).

The `matplotlibrc` file will always be active. It changes the default colour scheme in use by Python 3, and backend settings can be specified as well.

Figure settings will only change when a style sheet is called by the user the Python script. Several style sheets are included within the `stylelib` directory. The base style sheet is `science` and sets most options of interest. Any of these options can again be overwritten by calling yet another style sheet. Most included sheets are specific to astronomical journals to set proper figures sizes.

All possible customisation options can be found at the designated [matplotlib webpage](https://matplotlib.org/stable/users/explain/customizing.html).

# Usage

The defaults can be overwritten after importing the `matplotib` library. Add then the following in the header of the script, or anywhere else before plot calls appear.

## Basic

Call the base style.

```
plt.style.use(['science'])
```

## Jupyter notebook

Activate the notebook style together with no Latex rendering.

```
plt.style.use(['notebook', 'no-latex'])
%matplotlib inline
```