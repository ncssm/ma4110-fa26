# Lab 07 - Grading Guide

## Total points: 14

## Points Summary
| Question   | Points |
| ---------  | ------ |
| Autograder | 8 |
| Q 1.2      | 1 |
| Q 1.3      | 1 |
| Q 2.2      | 1 |
| Q 3.1      | 1 |
| Q 3.2      | 1 |
| Q 3.9      | 1 |

## Solutions

### Q 1.2

#### Solution
Zero. Under the null model there is no systematic difference between the two groups, so the
difference of the group means should be 0 on average.

#### Rubric
+1: Says 0 (or "no difference"), and ties it to the null hypothesis.

+0.5: Says 0 with no reasoning.

+0: Gives a non-zero value, or describes the alternative hypothesis instead.

+0: No response.

### Q 1.3

#### Solution
Shuffling the labels resamples the data under the assumption that the labels are unrelated
to the outcome — that is, under the null hypothesis. Repeating this many times builds the
distribution of the difference in means we would expect by chance, which is what lets us
judge whether the observed difference is unusual.

#### Rubric
+1: Explains that shuffling simulates the null hypothesis, **and** that the resulting
distribution is what the observed statistic is compared against.

+0.5: Says shuffling simulates the null model but does not explain what the distribution is
used for.

+0.5: Describes comparing to a distribution but does not connect shuffling to the null.

+0: Says shuffling makes the data random, or gives no reasoning.

+0: No response.

### Q 2.2

#### Solution
```python
my_bins = np.arange(2, 9.5, 0.5)
helicopters.hist('Time', bins=my_bins, group="Rotor")
```

#### Rubric
+1: An overlaid histogram of `Time` using the provided `my_bins` **and** `group="Rotor"`, so
both rotor lengths appear on the same axes.

+0.5: Correct column and bins but no `group` argument, so only one combined distribution is
shown.

+0.5: Uses `group` correctly but ignores the provided bins.

+0: Plots the wrong column, or produces two separate histograms instead of an overlay.

+0: No response.

### Q 3.1

#### Solution
An A/B test is appropriate because we are comparing two distributions of numerical data
split by a categorical label. The "A" (control) group is the full-length rotors; the "B"
(treatment) group is the shortened rotors.

#### Rubric
+1: Explains why an A/B test fits (comparing two groups' numerical distributions) **and**
correctly identifies which group is control and which is treatment.

+0.5: Identifies the groups but does not explain why an A/B test is appropriate.

+0.5: Explains the setup but assigns the groups backwards or leaves them unspecified.

+0: Incorrect or no response.

Accept the reverse group assignment if the student is consistent with it in Question 3.2.

### Q 3.2

#### Solution
The test statistic is the difference between the mean fall times of the two groups. Small
values support the null hypothesis; large values support the alternative that the
longer-rotor helicopters fall more slowly.

#### Rubric
+1: Names the difference of group means as the statistic **and** says which values support
the alternative.

+0.5: Names the statistic but does not say which values favour the alternative.

+0.5: Describes the direction correctly but proposes an unsuitable statistic.

+0: Proposes the absolute difference. The hypothesis here is one-sided ("longer for longer
rotors"), so the signed difference is what is wanted — but award +0.5 if the student
explicitly justifies a two-sided test.

+0: No response.

### Q 3.9

#### Solution
No. The data were not collected from a randomized controlled experiment, so a small p-value
shows association, not causation. Confounding factors, or the way helicopters were assigned
to groups, could explain the difference.

#### Rubric
+1: Says the result does **not** establish causation, **and** justifies it from the design of
the study (no randomized assignment), **and** notes what the A/B test does show
(association / an unlikely-by-chance difference).

+0.5: Correct conclusion citing only the study design, or only the meaning of the p-value.

+0.5: Discusses causation versus association sensibly but concludes causation is
established.

+0: Claims the small p-value proves causation.

+0: No response.
