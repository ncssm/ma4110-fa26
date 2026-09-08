# Lab 09 - Grading Guide

## Total points: 12

## Points Summary
| Question   | Points |
| ---------  | ------ |
| Autograder | 8 |
| Q 1.1      | 1 |
| Q 1.2      | 1 |
| Q 1.4      | 1 |
| Q 4.2      | 1 |

## Solutions

### Q 1.1

#### Solution
```python
faithful.scatter('duration')
```

`duration` on the horizontal axis, `wait` on the vertical axis.

#### Rubric
+1: A scatter plot with `duration` on the x-axis and `wait` on the y-axis.

+0.5: Scatter plot with the axes reversed. The prompt states the convention explicitly, so
this is worth a comment.

+0.5: Correct variables shown but with a different chart type (e.g. a line plot).

+0: No plot, or a plot of the wrong columns.

+0: No response.

### Q 1.2

#### Solution
Yes, roughly linearly related. The durations form two clusters — a group of short eruptions
and a group of longer ones — but within and across the clusters the points fall roughly along
a line. The association is **positive**: longer eruptions are followed by longer waits.

#### Rubric
+1: Says the relationship is roughly linear **and** positive, **and** describes a specific
feature of the scatter plot (the two clusters, or the upward trend).

+0.5: Identifies the relationship as positive and linear but describes no features of the
plot, despite the prompt asking them to be specific.

+0.5: Describes the plot well but characterises the direction or form incorrectly.

+0: Says there is no relationship, or gives no reasoning.

+0: No response.

Do not deduct for a student who notes the clustering and hedges on linearity, as long as
they explain why the clusters still permit a linear fit.

### Q 1.4

#### Solution
```python
faithful_standard.scatter(0)
```

#### Rubric
+1: Scatter plot of the standardised table, with the standardised duration on the x-axis.

+0.5: Plots the standardised data but with the axes reversed, or re-standardises by hand
rather than using `faithful_standard`.

+0.5: Re-plots the original (non-standardised) data. The shape looks identical, so check the
axis scales — standard units should run roughly from −2 to 2.

+0: No plot.

+0: No response.

### Q 4.2

#### Solution
* **2.5 minutes** — reliable. The dataset contains eruptions of about this length, so the
  prediction is an interpolation.
* **0 minutes** — not reliable. A zero-length eruption is physically impossible, so the
  prediction is meaningless.
* **60 minutes** — not reliable. It is far outside the observed range; an eruption that long
  would likely behave quite differently from anything in `faithful`.

#### Rubric
+1: Judges all three predictions correctly **and** grounds the reasoning in the range of the
observed data (extrapolation versus interpolation).

+0.5: Judges all three correctly but justifies only some of them, or reasons only from "the
number looks odd" without reference to the data range.

+0.5: Correct reasoning about extrapolation but misjudges one of the three cases.

+0: Treats all three predictions as equally reliable because the regression line produces a
number for each. This is the misconception the question targets.

+0: No response.
