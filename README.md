# Code Sample: Data Cleaning with R

This repository, a demonstration of my data cleaning skills, contains some work that I did as a research assistant at Columbia Business School. The code here prepares data from the [University of Michigan's Panel Study of Entrepreneurs II (PSED)](https://www.icpsr.umich.edu/web/ICPSR/studies/37202), a longitudinal survey of entrepreneurs from 2005-2011, for analysis.

## Contents
- `cdbk.pdf` is the PSED codebook.
- `psedii_scrn_ABCDEF.sav` is the PSED data.
- To load and clean data, run `run.R`: this performs initialization, sources `read.R`, `extract.R`, `recode.R`, `construct.R`, and `convert.R`, then writes data (in wide and long panel formats) to "all_waves_wide.csv" and "all_waves_long.csv".
    - `read.R` reads the data from `psedii_scrn_ABCDEF.sav`.
    - `extract.R` subsets the raw data of around 8000 variables into a subset of around 100 useful variables, and maps PSED variable codes to meaningful variable names.
    - `recode.R` maps variable values to meaningful codes (i.e., if "No" was coded as "2", it becomes "N").
    - `construct.R` removes observations that don't fit our study criteria to create the `all_waves` sample.
    - `convert.R` converts the panel from wide format to long format.