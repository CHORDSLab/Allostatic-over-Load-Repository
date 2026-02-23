# CHANGELOG
  
_Last updated: February 22, 2026_

## Overview
This changelog provides a chronological record of structural, documentation, and code-related changes made to this CHORDS Lab public repository to support transparency, version tracking, and reproducibility throughout the project lifecycle.

---

### [v2.0.0] – 2026-02-22  
**Weighted Threshold Implementation Update**

#### NHANES

- Added sampling weights and survey design variables (`WTINT`, `WTMEC`, `WTPH`, `SDMVSTRA`, `SDMVPSU`) to final dataset.
- Recalculated biomarker risk thresholds using survey-weighted quartiles.
- Identified and corrected logic error in `WHtR_risk_score` calculation.
- Added guidance section in `NHANES_dataset_construction.Rmd` on applying survey weights in analyses.
- Updated `NHANES_data_dictionary.xlsx` to document weight and design variables and revised derived variable definitions.
- Improved in-script documentation and explanatory comments for reproducibility.

#### HRS

- Added sampling weights and survey design variables (`WT_RESP`, `WT_PM`, `WT_BIO`, `WT_LBQ`, `STRATUM`, `SECU`) to final dataset.
- Recalculated biomarker risk thresholds using survey-weighted quartiles.
- Identified and corrected coding error in `pulse_clean` calculation function.
- Recoded HRS special missing values (e.g., 993, 998, 999) to `NA` and documented changes.
- Converted categorical variables (`sex`, `race`, `ethnicity`) to factors.
- Converted `biomarker_count` from double to integer.
- Retained biomarker risk threshold columns in final dataset for consistency with NHANES structure.
- Added guidance section in `HRS_dataset_construction.Rmd` on applying survey weights in analyses.
- Updated `HRS_data_dictionary.xlsx` to include weight and design variables and added HRS codebook URL references.
- Expanded in-script documentation and structural comments to improve clarity and reproducibility.

#### Documentation

- Updated repository README to reflect v2.0.0 release and weighted threshold implementation.
- Updated `NHANES` and `HRS` README files to reflect new weight handling and variable naming conventions.
- Updated `HRS_access_guide.md` to include Cross-Wave Tracker File instructions.  

---

### [2025-08-15]
- Added `NIH_All_of_Us_access_guide.md`, `NIH_All_of_Us_dataset_construction.ipynb`, and `NIH_All_of_Us_dataset_construction.pdf` to the `/NIH_All_of_Us` directory  
- Updated `README.md` in the `/NIH_All_of_Us` directory

---  

### [2025-07-31]
- Removed `/_TEMP_internal_docs` from `/docs` directory
- Archived pre-launch repository version; removed pre-launch notes from `CHANGELOG.md` and `TODO.md`
- Published public-facing version of the repository (changed visibility from private to public)

