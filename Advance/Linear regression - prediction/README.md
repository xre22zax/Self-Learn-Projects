# Linear Regression Analysis of Website Usage Time

This repository contains Python code that explores factors influencing time spent on a website using linear regression.

## Key Findings

- Age and time spent on the website are positively correlated.
- Chrome users tend to spend longer on the website than Safari users.

## Files

- website.csv: Contains data on user age, browser type, and time spent on the website (in seconds).
- linear_regression.py: Python script for analysis, including:
    - Loading and exploring data
    - Building and fitting linear regression models
    - Visualizing results
    - Making predictions

## Dependencies

- pandas
- numpy
- matplotlib.pyplot
- statsmodels.api

## Usage

1. Install dependencies: `pip install pandas numpy matplotlib statsmodels`
2. Run the script: `python linear_regression.py`

## Key Code Snippets

```python
# Load data
website = pd.read_csv('website.csv')

# Model 1: Time vs. Age
model = sm.OLS.from_formula('time_seconds ~ age', website)
results = model.fit()

# Model 2: Time vs. Browser
model = sm.OLS.from_formula('time_seconds ~ browser', website)
results = model.fit()

# Prediction for 40-year-old
pred40 = results.params[0] + results.params[1]*40
```

## Contributing

Feel free to submit issues or pull requests for improvements or additions.

---

## Author

[Reza Sadeghi](https://github.com/xre22zax/)