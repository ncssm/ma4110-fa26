# Lab 06 - Grading Guide

## Total points: 11

## Points Summary
| Question   | Points |
| ---------  | ------ |
| Autograder | 8 |
| Q 1.1      | 1 |
| Q 1.4      | 1 |
| Q 1.11     | 1 |

## Solutions

### Q 1.1

#### Solution
Emily's model is that the TT practitioners have a 50% chance of choosing the correct hand —
equivalent to flipping a fair coin. The alternative model is that the practitioners choose
the correct hand with some chance **other than** 50%.

#### Rubric
+1: States the null model as a 50% (chance / fair-coin) rate of choosing the correct hand,
**and** states an alternative that is "some rate other than 50%".

+0.5: States the null model correctly but gives no alternative, or gives a one-sided
alternative ("better than guessing") without justification.

+0.5: States a correct alternative but describes the null model imprecisely.

+0: Describes the models backwards, or gives no model.

+0: No response.

### Q 1.4

#### Solution
The statistic is the **absolute** difference between the expected percent correct and the
actual percent correct. The absolute value is what matters: the alternative model in
Question 1.1 says practitioners are *not* guessing at random, not that they are *better*
than random. A deviation in either direction is evidence against Emily's model.

#### Rubric
+1: Explains that the absolute difference is used because the alternative is two-sided —
deviation in either direction counts — and ties this back to the models from Q1.1.

+0.5: Says the absolute difference is the right statistic but does not connect it to the
two-sided alternative.

+0.5: Connects to the models from Q1.1 but misstates why the absolute value is needed.

+0: Argues for a signed difference, or gives no reasoning.

+0: No response.

### Q 1.11

#### Solution
No. The proportion of simulated statistics at least as large as the observed statistic is
greater than 0.05, so there is not enough evidence to reject Emily's model. The data are
consistent with practitioners guessing at random.

#### Rubric
+1: Concludes there is **not** sufficient evidence to reject Emily's model, **and** justifies
it by comparing the proportion from Q1.10 against the 5% cutoff.

+0.5: Correct conclusion but no reference to the 5% cutoff or the value from Q1.10.

+0.5: Compares against the cutoff correctly but states the conclusion backwards.

+0: Claims the model is rejected, or treats "failing to reject" as proof the model is true.

+0: No response.

**Note:** watch for students who write that the result "proves" the practitioners were
guessing. Failing to reject is not proof of the null model — this is worth a comment even
when the rest of the answer earns full credit.
