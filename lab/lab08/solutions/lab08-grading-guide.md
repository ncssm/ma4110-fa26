# Lab 08 - Grading Guide

## Total points: 12

## Points Summary
| Question   | Points |
| ---------  | ------ |
| Autograder | 6 |
| Q 1.1      | 1 |
| Q 2.2      | 1 |
| Q 2.3.a    | 1 |
| Q 2.3.b    | 1 |
| Q 2.5.a    | 1 |
| Q 2.5.b    | 1 |

## Solutions

### Q 1.1

#### Solution
```python
births = Table().read_table('baby.csv')
births.hist('Maternal Age')

# Do not change this line
plt.scatter(np.mean(births.column('Maternal Age')), -0.001, color = 'red', s = 50 , marker = "^");
```

The plot should be a histogram of `Maternal Age` with the red triangle sitting under the
centre of the distribution.

#### Rubric
+1: A histogram of the `Maternal Age` column, with the provided red-triangle line left
intact.

+0.5: Histogram of the wrong column, or a different chart type that still shows the
distribution.

+0.5: Correct histogram but the provided last line was modified or deleted.

+0: No plot, or a plot of something other than a distribution.

+0: No response.

### Q 2.2

#### Solution
```python
for i in np.arange(repetitions):
    new_sample_mean = one_sample_mean(table, label, sample_size)
    means = np.append(means, new_sample_mean)
```

Only the two lines inside the `for` loop should change; the rest of the function is provided.

#### Rubric
+1: Calls `one_sample_mean` with all four pieces of information passed through from the
function's arguments, **and** appends each mean back onto `means`.

+0.5: Computes the sample mean correctly but overwrites `means` instead of appending
(so only the last value survives).

+0.5: Appends correctly but hard-codes the table, label, or sample size instead of using the
function's arguments.

+0: Modifies the provided code below the loop, or does not produce an array of means.

+0: No response.

### Q 2.3.a

#### Solution
```python
simulate_sample_mean(salaries, 'salary', 400, 10000)
plt.xlim(50000, 100000);
```

Any sample size is acceptable as long as `repetitions` is held at 10,000. Students were
encouraged to try several.

#### Rubric
+1: Calls `simulate_sample_mean` on `salaries` / `'salary'` with `repetitions` fixed at
10,000 and a sample size of their choosing, and leaves the `plt.xlim` line in place.

+0.5: Correct call but the number of repetitions was varied instead of held fixed — that is
Question 2.5's investigation, not this one.

+0.5: Ran only one sample size when the prompt asked them to vary it. Full credit is fine if
Q2.3.b shows they actually compared several.

+0: Wrong table or column, or the function was not called.

+0: No response.

### Q 2.3.b

#### Solution
As the sample size increases, the SD of the sample means decreases. Every other reported
statistic stays about the same: all the histograms centre on the population mean, but they
get narrower as the sample size grows, because larger samples vary less.

#### Rubric
+1: States that larger samples produce a **smaller SD of sample means** and a narrower
histogram, **and** cites specific printed statistics or histogram features from their own
runs.

+0.5: Correct conclusion but no specific values or visual details, despite the prompt asking
for them.

+0.5: Cites the data well but concludes the spread grows, or that nothing changes.

+0: Claims the centre of the distribution shifts with sample size.

+0: No response.

### Q 2.5.a

#### Solution
```python
simulate_sample_mean(salaries, 'salary', 100, 500)
plt.xlim(50000, 100000);
```

Any number of repetitions is acceptable as long as `sample_size` is held at 100.

#### Rubric
+1: Calls `simulate_sample_mean` with the sample size fixed at 100 and a number of
repetitions of their choosing, leaving `plt.xlim` in place.

+0.5: Correct call but the sample size was varied instead of held fixed.

+0: Wrong table or column, or the function was not called.

+0: No response.

### Q 2.5.b

#### Solution
The histograms get smoother as the number of samples increases, but the spread does not
change — neither does the SD of the sample means or any other statistic. Only the sample
size affects the variability.

#### Rubric
+1: States that more repetitions produce a **smoother** histogram but leave the SD and centre
essentially unchanged, **and** cites specific statistics or histogram features.

+0.5: Correct conclusion without specific evidence.

+0.5: Cites evidence but claims more repetitions reduce the variability of the sample means.
This is the key misconception in this lab — it is the *sample size* that controls the
spread, not the number of samples. Worth a written comment.

+0: Incorrect or no response.
