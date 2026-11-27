# Model Card: Credit Card Default Predictor

Model: Random Forest at threshold 0.35. See README for results and the report for full details.

## Intended Use
- Purpose: flag credit card customers who are likely to default on their next payment
- Intended users: bank credit staff, as a tool to decide who needs a credit review
- Out of scope: automatically refuse credit, setting interest rates, or use on data from other countries or time periods without retesting

## Subgroup Checks
- Sex: similar recall, but false positive rate 47% (men) vs 41.6% (women)
- Age: false positive rate ranges from 0.389 to 0.486 across age groups; the 51+ group is small (n = 470

## Known Failure
- Misses defaulters who look like good customers (paying on time recently, higher credit limits)

## Risks and Harms
- Good customers wrongly flagged could be refused credit or charged more
- Uses SEX and AGE as inputs, which may not be legal for credit decisions in some countries

## Human Oversight and Monitoring
- Every flag should be reviewed by a human before any decision
- Track the false positive rate for each group over time
- Retrain or review if the default rate or customer behaviour changes(data drift)

## Would Deployment Be Justified?
- Not as it is. It would only be suitable as a flagging tool with human review, after testing on recent data