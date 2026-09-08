# Lab 05 - Grading Guide

## Total points: 17

## Points Summary
| Question   | Points |
| ---------  | ------ |
| Autograder | 11 |
| Q 1.2      | 1 |
| Q 3.5      | 1 |
| Q 3.6.a    | 1 |
| Q 3.6.b    | 1 |
| Q 3.7.a    | 1 |
| Q 3.7.b    | 1 |

## Solutions

### Q 1.2

#### Solution
```python
if number_cheese < 5:
    say_please = 'More please'
else:
    say_please = 'Perfect'
say_please
```

#### Rubric
+1: A correct `if`/`else` that assigns `'More please'` when there are fewer than 5 cheese
nachos and `'Perfect'` otherwise.

+0.5: Correct logic but the comparison boundary is wrong (e.g. `<= 5` instead of `< 5`).

+0.5: Uses `if` without `else`, so `say_please` is undefined in one branch.

+0: Reassigns `say_please` directly instead of using a conditional — the prompt explicitly
rules this out.

+0: Incorrect or no response.

### Q 3.5

#### Solution
No, the convenience sample does not give an accurate picture of the salaries of the full
population. It is biased toward players younger than 22. Younger players are unproven, so
they do not command top salaries until they have established themselves.

#### Rubric
+1: Says the sample is **not** representative, **and** cites the histograms or summary
statistics, **and** gives a contextual reason (young players are unproven / early in their
contracts).

+0.5: Correct conclusion but supported only by intuition, with no reference to the
histograms or summary statistics.

+0.5: Cites the data correctly but draws the wrong conclusion.

+0: Claims the convenience sample is representative.

+0: No response.

### Q 3.6.a

#### Solution
```python
my_small_srswor_data = full_data.sample(44, with_replacement = False)
histograms(my_small_srswor_data)
my_small_stats = compute_statistics(my_small_srswor_data)
my_small_stats
```

#### Rubric
+1: Samples 44 rows **without** replacement, then calls both `histograms` and
`compute_statistics` on the sample.

+0.5: Samples with replacement, or uses the wrong sample size.

+0.5: Correct sample but only one of the two provided functions is called.

+0: Incorrect or no response.

### Q 3.6.b

#### Solution
The average age stays close to the population value from sample to sample, because NBA
players fall in a narrow age range. The average salary swings much more, because salaries
are far more variable.

#### Rubric
+1: Identifies that **age** is the more stable average and **salary** the more variable one,
**and** attributes this to the spread of the two variables.

+0.5: Identifies which average is more variable but does not explain why.

+0.5: Gives a reasonable explanation but names the wrong variable as more stable.

+0: Does not compare the two averages, or reports only a single sample without noting the
sample-to-sample variation the question asks about.

+0: No response.

### Q 3.7.a

#### Solution
```python
my_large_srswor_data = full_data.sample(100, with_replacement = False)
histograms(my_large_srswor_data)
my_large_stats = compute_statistics(my_large_srswor_data)
my_large_stats
```

#### Rubric
+1: Samples 100 rows without replacement and calls both provided functions.

+0.5: Samples with replacement, or uses the wrong sample size.

+0: Incorrect or no response.

### Q 3.7.b

#### Solution
Samples of 100 vary less from sample to sample and land closer to the population values,
which is what we expect from a larger sample. The age histogram and average in particular
track the population closely, because age is less variable than salary.

#### Rubric
+1: Says the larger sample approximates the population better, **and** compares the
histograms or summary statistics of the two sample sizes to support it.

+0.5: Correct conclusion with no comparison of the two sampling methods.

+0.5: Compares the two but concludes the smaller sample is as good or better.

+0: Incorrect or no response.
