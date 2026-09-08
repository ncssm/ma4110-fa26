# Lab 04 - Grading Guide

## Total points: 17

## Points Summary
| Question   | Points |
| ---------  | ------ |
| Autograder | 15 |
| Q 3.6      | 1 |
| Q 4.1      | 1 |

## Solutions

### Q 3.6

#### Solution
```python
ceo_salary_percent.set_format('Salary (%)', PercentFormatter)
ceo_salary_percent
```

The `Salary (%)` column should display values such as `2.35%` rather than `0.0235`. The
underlying data is unchanged — `set_format` only changes how the column is displayed.

#### Rubric
+1: Uses `set_format` with `PercentFormatter` on the `'Salary (%)'` column, and the displayed
table shows percentages.

+0.5: Calls `set_format` but with the wrong formatter (e.g. `NumberFormatter`), or formats the
wrong column.

+0.5: Converts the values by multiplying by 100 instead of using a formatter. The display is
right but the method asked for was not used.

+0: Incorrect or no response.

### Q 4.1

#### Solution
```python
compensation.hist('Total Pay ($)', bins = np.arange(0, 25000000, 1000000), unit="Dollar")
```

There is no autograder check on this question, so the plot must be read directly.

#### Rubric
+1: A histogram of `Total Pay ($)` with bins running from 0 to 25,000,000 in steps of
1,000,000. The distribution is strongly right-skewed, with most CEOs in the first few bins.

+0.5: Histogram of the correct column but with default or otherwise incorrect bins.

+0.5: Correct bins but the wrong column plotted.

+0: No histogram, or a different chart type (bar chart, scatter plot).

+0: No response.

**Note:** students are warned in the prompt that the bar heights will be very small because
the bin widths are in dollars. Do not deduct for small y-axis values — that is expected.
