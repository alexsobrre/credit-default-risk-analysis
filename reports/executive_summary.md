# Executive summary

The analysis tests prioritization of existing accounts for review using a 10% capacity constraint. Random forest was selected using training cross-validation. On the held-out test set it captured 31.7% of defaults at 70.2% precision, compared with 31.5% recall for a latest-repayment-code rule and 10% expected recall for random review.

Test ROC-AUC was 0.782, average precision 0.565, and Brier score 0.134. The notebook includes probability calibration, uncertainty, and subgroup checks. These estimates describe a held-out subset of a historical cohort, not future performance.

Financial scenarios vary review cost, LGD, and assumed effectiveness using latest positive balances as an exposure proxy. The dataset cannot establish realized savings or intervention effectiveness. Any economic recommendation depends on these assumptions and probability quality.

Recommendation: use this as a reproducible demonstration of ranking and decision analysis. Before operational use, obtain later-period validation, documented category/target definitions, actual loss data, additional fairness assessment, and a measured intervention pilot.

The random forest captured only three more defaults than the repayment rule among 600 reviewed test accounts (421 versus 418). Logistic regression captured 420. These small differences do not establish a meaningful operational advantage for the more complex model; prefer a simple policy unless further validation justifies complexity.
