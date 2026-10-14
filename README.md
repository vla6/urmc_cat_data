# Dataset creation for URMC course

Synthetic dataset representing costs of an inpatient stay, with significant contributions to diagnosis codes.

## Data Sources

### DX Code Frequencies

This project uses inpatient frequency data from the [HEALTHCARE COST & UTILIZATION PROJECT](https://hcup-us.ahrq.gov/nisoverview.jsp).  Because of license and data use / privacy concerns, the full inpatient dataset is not used.  Instead, public high-level summaries are used to seed creation of a synthetic dataset.   

The seed information is a summary Excel file [HCUP_NIS2016_2023_DXandPRfreqs.xlsx](https://hcup-us.ahrq.gov/db/nation/nis/HCUP_NIS2016_2023_DXandPRfreqs.xlsx).  The sheet called "T.2_By_DX_Code" was converted to CSV and placed in this repository at **data/dx_freq.csv**.

### Summary statistics

Additional dataset features are based on summary statistics from AHRQ.

Patient / visit related summary stats for 2023 are found in [SumStats NIS 2023 Core File, unweighted](https://hcup-us.ahrq.gov/db/nation/nis/tools/stats/MaskedStats_NIS_2023_Core.PDF).  Extracts from these stats are placed in **data/sum_stats_*.csv**

Similarly, hospital stats are 