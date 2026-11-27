# Reflective Changelog

- **Oct 2026: Project setup.** Chose the credit default dataset for a cost sensitive angle. Set up repo, venv and requirements.
- **M2: Data Audit** Found 35 duplicates and undocumented EDUCATION/MARRIAGE codes, dropped duplicates before splitting (to avoid data leakage), merged codes into catch all "others".
- **M2: Evaluation** Chose a 60/20/20 stratified split and a cost metric 5xFN + 1xFP as accuracy was misleading (baseline got 78% while catching 0 defaulters).
- **M3: Model comparison** At 0.5 the tree had the lowest cost but after threshold tuning the forest at 0.35 had the lowest (3318) , so I chose the forest.
- **M4: Final Evaluation** I tested it once on the test set: cost 3455 vs baseline 6630. Added fairness checks and found false positive rate gaps by age and sex.
- **M4: README fix** Fresh setup test showed the venv commands were hidden on GitHub, so I fixed them.