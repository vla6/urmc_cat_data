# Synthetic Dataset Creation for URMC Course Assignment

Synthetic dataset representing costs of an inpatient stay, with significant contributions from ICD10 diagnosis codes.

## Data Sources

### DX Code Frequencies

This project uses inpatient frequency data from the [HEALTHCARE COST & UTILIZATION PROJECT](https://hcup-us.ahrq.gov/nisoverview.jsp).  Because of license and data use / privacy concerns, the full inpatient dataset is not used.  Instead, public high-level summaries are used to seed creation of a synthetic dataset.   

The seed information is a summary Excel file [HCUP_NIS2016_2023_DXandPRfreqs.xlsx](https://hcup-us.ahrq.gov/db/nation/nis/HCUP_NIS2016_2023_DXandPRfreqs.xlsx).  The sheet called "T.2_By_DX_Code" was converted to CSV and placed in this repository at **data/dx_freq.csv**.

### Summary statistics

Additional dataset features are based on summary statistics from AHRQ.

Patient / visit related summary stats for 2023 are from [SumStats NIS 2023 Core File, unweighted](https://hcup-us.ahrq.gov/db/nation/nis/tools/stats/MaskedStats_NIS_2023_Core.PDF).  Extracts from these stats are placed in **data/sum_stats_*.csv**

Similarly, hospital stats are from [MaskedStats_NIS_2023_Core.PDF](https://hcup-us.ahrq.gov/db/nation/nis/tools/stats/MaskedStats_NIS_2023_Core.PDF).  Extracts from these stats are placed in **data/hosp_*.csv**

## Setup

Local paths and other constants are defined in **00_setup.py**.  Modify this file to point to a local directory for storing intermediate files.

## Python Environment & Packages

This project uses **Python 3.12**.  

I suggest creating and using a virtual environment as follows (from the project root folder):

```bash
python3 -m venv venv
source venv/bin/activate
```

Now, install needed packages and create a kernel for Jupyter to use this environment: 
```bash
pip install -r requirements.txt
python -m ipykernel install --user --name=urmc_cat_data --display-name="URMC Cat Dataset"
```

*Note*: As I am on a mac I had to do `brew install libomp` in my virtual environment