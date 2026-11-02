# Perceived employability of senior executives

This project looks at how senior executives (aged 45 to 65) in France see their own employability. It uses their answers to a questionnaire that measures 12 dimensions of perceived employability.

## Questions

1. **What goes with professional self-efficacy?** Self-efficacy is a person's confidence that they could find another job. I study it with a linear regression.
2. **Who are the job seekers?** I compare job seekers with employed executives using a logistic regression, and I test how well the model predicts job status.

## Main results

- The data has 460 answers. Three pairs of rows were exact copies, so one row of each pair was removed, which leaves **457 respondents**.
- The linear regression explains about **45% of the differences in self-efficacy** (R² = 0.448).
- **Flexibility** and **awareness of one's own value** are the two scores most strongly linked to self-efficacy. Older executives and those earning less than 100k report lower confidence, other things being equal.
- Job seekers have **lower self-efficacy** and **higher training scores**. They also have **fewer dependent children** and are **more often without a business school degree**.
- The logistic regression **describes** the job seekers but **cannot find them**. Its test accuracy (85.9%) is the same as a baseline that always predicts "employed", and it finds only 2 of the 13 job seekers in the test set.
- These are associations in a single survey taken at one moment. They do not show cause and effect.

## Files

| File | What it is |
| --- | --- |
| `CAVUSOGLU_employability_report.pdf` | The written report (11 pages). Start here. |
| `CAVUSOGLU_employability_analysis.ipynb` | The Jupyter notebook with all the code, tables and charts. |
| `data/employability.csv` | The survey data (460 rows, 23 columns). |
| `data/codebook.csv` | A description of every column in the data. |
| `requirements.txt` | The Python packages and versions used. |

## How to run the notebook

1. Install Python. The notebook was run with Python 3.14.
2. Install the packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook:

   ```bash
   jupyter notebook CAVUSOGLU_employability_analysis.ipynb
   ```

4. Choose **Kernel > Restart & Run All**.

The notebook reads the data from the `data` folder using a relative path, so keep the folder structure as it is.

The report refers to notebook cells by their number (for example "cell 95"). These numbers are the `In [n]` numbers you see after **Restart & Run All**, and they go from 1 to 114.


## About the data

The data comes from a questionnaire that was e-mailed to 1,515 senior executives, of whom 500 answered (see Deacken & Jaotombo, 2019, in the report's references). The file does not contain names. Each respondent only has an arbitrary number.

The sample is not random. Most respondents come from one business school and earn more than 99k a year, so the results describe this group only.

## Author

Ali Ulas CAVUSOGLU
