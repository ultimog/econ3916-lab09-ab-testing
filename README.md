# econ3916-lab09-ab-testing
Lab 09 submission
# A/B Testing — Designing the Data-Generating Process

## Objective
I estimated the causal effect of a job training program and of a mobile game design change using randomized experiments, and checked how much data each test needs to detect its effect.

## Methodology
- I loaded the LaLonde NSW job training experiment (445 people: 185 trainees and 260 controls) and computed the experimental ATE.
- I simulated an observational comparison group to show selection bias, and split the gap: Observational ATE = True ATE + Selection Bias.
- I ran a permutation test (9,999 shuffles) and a bootstrap BCa 95% confidence interval for the ATE.
- I ran a power analysis: the power of this study, and the sample size needed for three dollar effects.
- I applied the same tests to the Cookie Cats mobile game A/B test (90,189 players, gate at level 30 or 40, Day-1 retention).
- I wrote a sample-size function, n_needed(), checked it against the power analysis, and used it to size a rerun of Cookie Cats.

## Key Findings
- Trainees earned $1,794.34 more than controls (permutation p = 0.0046, 95% CI $575.18 to $3,262.37).
- The simulated comparison group gave an ATE of $-14,784.45: without random assignment, the program looked harmful.
- Cookie Cats: gate_30 retained players 0.59 pp better than gate_40 (p = 0.0752), not significant at 0.05.
- A rerun large enough to detect that difference would need 111,192 players per group.
