---
jupytext:
  cell_metadata_filter: -all
  formats: ipynb,md:myst
  main_language: python
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.1
kernelspec:
  display_name: islp_test
  language: python
  name: islp_test
---

# Weekly S&P Stock Market Data

Weekly percentage returns for the S&P 500 stock index between 1990
and 2010.

- `Year`: The year that the observation was recorded

- `Lag1`: Percentage return for previous week

- `Lag2`: Percentage return for 2 weeks previous

- `Lag3`: Percentage return for 3 weeks previous

- `Lag4`: Percentage return for 4 weeks previous

- `Lag5`: Percentage return for 5 weeks previous

- `Volume`: Volume of shares traded (average number of daily shares
 traded in billions)

- `Today`: Percentage return for this week

- `Direction`: A factor with levels 'Down' and 'Up' indicating
 whether the market had a positive or negative return on a
 given week.

## Source

Raw values of the S&P 500 were obtained from Yahoo Finance and
then converted to percentages and lagged.

```{code-cell} ipython3
from ISLP import load_data
Weekly = load_data('Weekly')
Weekly.columns
```

```{code-cell} ipython3
Weekly.shape
```

```{code-cell} ipython3
Weekly.columns
```

```{code-cell} ipython3
Weekly.describe().iloc[:,:4]
```

```{code-cell} ipython3

```