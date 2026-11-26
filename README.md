# Flood-Risk Prediction Support System for Northern Pakistan

A classroom/research prototype that uses historical weather information and machine-learning models to estimate next-day **flood-risk conditions** for four locations in northern Pakistan: Havelian, Mingora/Swat, Nowshera and Muzaffarabad.

> **Important limitation:** The default target is derived from the top 5% of calculated runoff during the training period. It is not a record of verified river floods and this prototype must not be used as an official warning, evacuation or other high-stakes decision system.

## Project files

Place the supplied project files in this repository using the following structure:

```text
Flood-Risk-Prediction-System/
├── README.md
├── .gitignore
├── requirements.txt
├── PROJECT_LOG.md
├── TASK_RECORD.md
├── notebooks/
│   └── Flood_Risk_Prediction_Final.ipynb
├── reports/
│   ├── Project_Proposal.docx
│   └── Technical_Report.docx (or .pdf)
├── data/
│   └── data_dictionary.csv
├── docs/
│   ├── DATASET_AUDIT.md
│   └── DATA_DICTIONARY.md
└── outputs/
    ├── charts/
    └── model_results/
```

Only add files that actually exist. If the notebook creates its outputs during execution, you do not need to upload empty output folders.

## Data and method

- Main source: Open-Meteo Historical Weather API.
- Comparison source: NASA POWER daily weather data.
- Period in the notebook: 1960-01-01 to 2024-12-31.
- Locations: Havelian, Mingora/Swat, Nowshera and Muzaffarabad.
- Input features include daily rainfall, temperature, wind speed, evapotranspiration, estimated runoff, rolling rainfall/runoff summaries and day-of-year seasonality.
- Chronological split: training through 2018, validation 2019-2020, and test 2021-2024.
- Models include Logistic Regression, Random Forest and HistGradientBoosting; the notebook also contains a deep-learning extension using FNN, CNN, LSTM and an ensemble.

## Run the notebook

1. Use Python/Jupyter or Google Colab.
2. Install the packages listed in `requirements.txt`.
3. Open `notebooks/Flood_Risk_Prediction_Final.ipynb`.
4. Run the notebook cells in order. Internet access is required to retrieve weather data from the APIs.
5. The notebook creates `flood_data/` and `flood_outputs/` during execution.

The deep-learning extension can be skipped for a lighter run by setting the environment variable `RUN_DL=0` before running the notebook. The notebook also supports `QUICK_TEST=1` for a reduced test run; do not use quick-test results as the final reported experiment.

## Reported evaluation

The notebook's recorded test-period results for Hist Gradient Boosting are recall 68.6% and false-alarm rate 17.5%. The project's stated targets (recall at least 70%, false-alarm rate at most 15%) were **not met**. Report these results honestly.

## Safety and limitations

The model uses weather/reanalysis-derived inputs and a runoff-derived target, not verified flood-event labels. Coverage is limited to four locations. It is a classroom prototype for screening/research only, not an operational flood forecasting or public-warning service.

## Repository maintenance

Use meaningful commits that describe the actual changes made. Do not fabricate earlier dates, contributors, experiments or collaboration. The assignment guidance requires formal course-coordinator approval for an individual submission.
