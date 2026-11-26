# Dataset audit summary

## Sources and coverage

The notebook compares Open-Meteo historical archive data with NASA POWER daily data. Open-Meteo is used as the main source; NASA POWER is used for a rainfall comparison at Havelian. The notebook also describes the optional Open-Meteo Flood API/GloFAS river-discharge option.

The recorded main weather download covers 1960-01-01 through 2024-12-31 for:
- Havelian
- Mingora/Swat
- Nowshera
- Muzaffarabad

The notebook reports 23,742 daily rows per location.

## Recorded raw-data quality checks

The notebook's audit output reports, for each of the four locations:
- 23,742 rows
- No missing values in the downloaded raw table
- No duplicate dates
- No missing calendar days
- No negative rainfall values

The recorded dry-day percentages and maximum daily rainfall differ by location. See the notebook's Dataset Audit section for the full output.

## Target definition

The default label is based on calculated surface runoff (NRCS Curve Number method, CN=75). A flood-risk day is defined using the 95th percentile of runoff calculated from the training period. It is therefore a derived heavy-runoff indicator, **not a verified flood event label**.

The notebook records class shares of approximately 5% in the training period, 3.97% in validation and 3.49% in the test period.

## Time split and leakage control

- Training: through 2018-12-31
- Validation: 2019-01-01 through 2020-12-31
- Test: 2021-01-01 through 2024-12-31

The notebook states that the split is chronological and the runoff threshold/scaler are fitted using training data only. Validation is used for model selection; the test period is held out for final evaluation.

## Licence and access note

The notebook uses public API endpoints. Before final submission, verify and cite the current applicable Open-Meteo and NASA POWER terms/licence and attribution guidance, and record the actual date you accessed each source. This file deliberately does not assert a licence that has not been independently verified.

## Privacy and limitations

The notebook states that only weather data is used and no personal or identifiable information is collected. Limitations include reanalysis rather than local gauge observations, coarse/variable historical resolution, only four locations, and a runoff-derived target rather than verified flood records.
