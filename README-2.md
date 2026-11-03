# Nevis RIA Market Analysis

Isabella Vermaes's submission for the Nevis data analysis hometask. The notebook turns six SEC Registered Investment Adviser reports into a firm-level table, then answers the brief's market questions.

## Contents

- `nevis_ria_analysis.ipynb`: the executed notebook, with its outputs saved
- `requirements.txt`: the package versions it was tested on
- - `cross_check/`: my separate second build, used to check the main analysis
- `outputs/`: the output tables, without the full firm-year table

## Run it in Google Colab

1. Put exactly one file per year in `nevis_ria/data` in Google Drive, with names starting `Nov-21`, `Nov-22`, `Nov-23`, `Nov-24`, `Dec-25` and `Nov-26`.
2. Open the notebook in Colab and choose **Runtime → Run all**.
3. Allow access to Drive when asked.

The CSV outputs are saved to the `outputs` folder beside the data. No manual steps are needed.

The files come from the SEC's [Information About Registered Investment Advisers and Exempt Reporting Advisers](https://www.sec.gov/data-research/sec-markets-data/information-about-registered-investment-advisers-exempt-reporting-advisers) page. Use the registered adviser reports, not the exempt reporting adviser reports.

The October and November 2025 SEC reports contain no data because of the government shutdown, so `Dec-25` is used.

## Run it elsewhere

Tested on Python 3.13. Install the pinned versions with `pip install -r requirements.txt`. Put the six files in a `data` folder inside the project folder and run the notebook from there. Outside Colab, it reads from `./data` and saves to `./outputs`.

## Checks

The run stops if any of these fail:

- the 19 automatic checks on the final table
- the comparison of key firms with the source files
- the regression checks on the Q1 hold-out
- the check that the written executive summary still matches the data
