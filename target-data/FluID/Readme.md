# Target Data - FluID

This folder contains the ground truth information about ILI and ARI incidence in EU/EEA countries from [FluID]([https://erviss.org/](https://www.who.int/teams/global-influenza-programme/surveillance-and-monitoring/fluid)).

To access the latest data file, consider the [`latest-ILI_incidence.csv`]((https://github.com/european-modelling-hubs/RespiCast-SyndromicIndicators/blob/main/target-data/FluID/latest-ILI_incidence.csv)) and [`latest-ARI_incidence.csv`]((https://github.com/european-modelling-hubs/RespiCast-SyndromicIndicators/blob/main/target-data/FluID/latest-ARI_incidence.csv)). Alternatively, historical data files are stored in the folder [`snapshots`](https://github.com/european-modelling-hubs/RespiCast-SyndromicIndicators/tree/main/target-data/FluID/snapshots) and are named `YYYY-MM-DD-ILI_incidence.csv` and `YYYY-MM-DD-ARI_incidence.csv`, with `YYYY-MM-DD` representing the date of the last data update (which occurs every Friday). It's important to note that the latest files not only includes new data points but also the entire available history.

**Note**: To access additional datasets for informing your model, please visit the [Respiratory Viruses Weekly Data](https://github.com/EU-ECDC/Respiratory_viruses_weekly_data/tree/main) repository published by the ECDC.

Each ground truth CSV file contains the following columns:

| column | column type | description |
| -------- | -------- | ------- |
| `target` | string | The forecast target; one of: "ILI incidence", "ARI incidence" |
| `location` | string | **ISO-2** code identifying the country |
| `truth_date` | date | Date in format **YYYY-MM-DD**: the last day of the truth week (Sunday)|
| `year_week` | string | A string denoting the year and week to which the truth data corresponds |
| `value ` | decimal | ILI and ARI incidence per $100,000$ population (except for Finland, where it is reported per $100,000$ consultations)|


FluID covers the following countries: 

    ARI incidence: GB-ENG, GB-WLS, GB-NIR, GB-SCT
    ILI incidence: CH, GB-ENG, GB-WLS, GB-NIR, GB-SCT
