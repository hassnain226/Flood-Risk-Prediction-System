# Project log

This is a stage-based summary of work evidenced by the supplied notebook. Calendar dates are intentionally not invented.

| Stage | Work recorded in the notebook | Evidence |
|---|---|---|
| Problem definition | Defined a next-day flood-risk decision-support prototype for four locations in northern Pakistan and documented intended use and limitations. | Notebook Section 1 |
| Data acquisition | Retrieved historical weather data from Open-Meteo and compared rainfall with NASA POWER at Havelian. | Notebook Section 2 |
| Data validation and preparation | Added configuration/data validation, chronological splitting, feature engineering and training-only threshold/scaler fitting. | Notebook Sections 2-3 |
| Dataset audit | Reported row counts, date coverage, missing values, duplicate dates, calendar gaps, rainfall checks and a data dictionary. | Notebook Section 4 |
| Exploratory analysis | Produced and interpreted five EDA visualisations. | Notebook Section 5 |
| Model experiments | Compared Logistic Regression, Random Forest and Hist Gradient Boosting, including feature and imbalance-handling experiments and tuning. | Notebook Section 6 |
| Deep-learning extension | Compared FNN, CNN, LSTM and a CNN-LSTM-attention model on the same chronological split. | Notebook Section 7 |
| Evaluation | Evaluated on the held-out 2021-2024 period using classification and rare-event metrics. Both stated success criteria were not met. | Notebook Section 8 |
| Explainability and demonstration | Included 2022 analysis, feature importance, real-period replay and a clearly labelled what-if scenario. | Notebook Sections 9 and 11 |
| Testing | Recorded eight edge-case tests as passing. | Notebook Section 10 |
| Documentation and repository | Proposal, notebook and technical report are prepared; GitHub repository organisation and further genuine commits remain to be completed. | Project files and repository |

Update this log if further work is actually performed. Do not add invented dates or claim tasks that were not completed.
