# Student Job Board – Application & Recruitment Analysis

**Analysis Period:** July – September 2026

## Project Overview

This project analyses student job application data to evaluate recruitment funnel performance, acquisition channel effectiveness and employer responsiveness.

The analysis focuses on three key areas:

1. Identifying acquisition sources that generate the highest hiring rates.
2. Understanding the relationship between application completion and shortlisting.
3. Comparing employer response times across paid and unpaid opportunities.

**Dataset:** 1,206 application records  
**Final Dataset:** 1,200 unique applications

## Manager Summary

[View the Recruitment Performance Summary](report/manager_summary.md)

## 1. Acquisition Channel Performance

The objective is to identify which acquisition channels generate the highest number of hires relative to application volume.

### Overall Source Performance

| Source | Applications | Hires | Hires per 100 Applications |
|---|---:|---:|---:|
| Referral | 121 | 13 | **10.74** |
| Email | 160 | 13 | 8.12 |
| Search | 439 | 25 | 5.69 |
| College | 208 | 7 | 3.37 |
| Social | 257 | 6 | 2.33 |

Referral emerged as the strongest overall acquisition channel.

### Performance Across Role Categories

The leading acquisition source varies across different job categories:

| Role Category | Highest Performing Source |
|---|---|
| Data | Search |
| Design | Referral |
| Finance | Search |
| Marketing | Referral |
| Operations | College |
| Software | Email |

**Business Insight:** Acquisition performance is not uniform across job categories. Channel strategies should account for role-specific differences rather than relying exclusively on overall conversion performance. Rates for smaller groups should be interpreted cautiously.

## 2. Application Completion & Shortlisting

This analysis compares shortlisting outcomes between applicants who completed all four application steps and those who completed fewer steps.

| Completion Group | Applications | Shortlisted | Shortlist Rate |
|---|---:|---:|---:|
| Completed all 4 steps | 403 | 195 | **48.39%** |
| Completed fewer than 4 steps | 797 | 74 | **9.28%** |

**Key Findings:**
- Shortlist-rate difference: **39.10 percentage points**
- Relative shortlist-rate ratio: **5.21x**

**Business Insight:** Applicants completing all four steps demonstrate a substantially higher observed shortlisting rate. Improving application completion through progress indicators and timely reminders could be worth exploring.

This relationship is observational and does not establish causation.

## 3. Paid vs. Unpaid Employer Responsiveness

Applications were classified according to their monthly stipend:

- Paid opportunities: Monthly stipend greater than ₹0.
- Unpaid opportunities: Monthly stipend equal to ₹0.

### Response Performance

| Metric | Paid Roles | Unpaid Roles |
|---|---:|---:|
| Total Applications | 734 | 466 |
| Recorded Replies | 638 | 328 |
| Median First-Reply Time | **3 days** | **7 days** |
| Mean First-Reply Time | 3.22 days | 7.62 days |
| No Reply Recorded | 96 | 138 |
| No-Reply-Recorded Rate | **13.08%** | **29.61%** |

**Key Findings:**

- Applicants to unpaid opportunities wait longer for a recorded first response.
- The median response time is 7 days for unpaid roles, compared with 3 days for paid roles.
- The no-reply-recorded rate is 16.53 percentage points higher for unpaid opportunities.

**Business Insight:** The difference in employer responsiveness highlights an opportunity to improve communication, particularly for unpaid opportunities. Automated employer reminders could help reduce delays in application responses.

Response-time statistics include only applications with recorded replies. Missing reply times represent responses not recorded at the dataset snapshot.

## 4. Data Visualisation

### Employer Responsiveness: Paid vs. Unpaid Roles

![Paid vs. Unpaid Employer Responsiveness](outputs/question_3_paid_vs_unpaid.png)

The visualisation compares median first-reply times and no-reply-recorded rates across paid and unpaid opportunities.

## 5. Data Preparation & Quality Checks

The dataset was examined and prepared before conducting the analysis.

Key preparation steps included:

- Inspected dataset dimensions, data types, missing values and duplicate records.
- Identified six duplicated application IDs containing exact duplicate records.
- Removed duplicate records, retaining 1,200 unique applications.
- Standardised inconsistent work-mode values.
- Replaced 15 missing acquisition source values with `unknown`.
- Preserved missing response-time values without imputing them.
- Validated recruitment funnel consistency.

The 15 applications with unknown acquisition sources were excluded from source-specific comparisons.

No inconsistent recruitment funnel records were identified during validation.

## 6. Methodology

The analysis was conducted using Python and Pandas.

The following metrics were calculated:

| Metric | Calculation |
|---|---|
| Hires per 100 Applications | (Hires / Applications) × 100 |
| Shortlist Rate | (Shortlisted / Applications) × 100 |
| Shortlist-Rate Difference | Completed-4-Step Rate − Fewer-Step Rate |
| Median Response Time | Median of recorded first-reply days |
| No-Reply-Recorded Rate | (Missing Reply Records / Total Applications) × 100 |

The analysis also includes grouping, aggregation, data cleaning, missing-value assessment and comparative visualisation.

## 7. Limitations

- Missing acquisition sources limit channel attribution for 15 applications.
- Some role-category/source combinations have relatively small sample sizes.
- Missing reply times do not establish permanent non-response.
- The relationship between application completion and shortlisting does not establish causation.
- The analysis assumes that a stipend of ₹0 represents an unpaid opportunity.

## 8. Project Structure

```text
job-board-analysis/
│
├── README.md
├── requirements.txt
│
├── data/
│   └── job-board-applications.csv
│
├── notebooks/
│   └── analysis.ipynb
│
├── outputs/
│   └── question_3_paid_vs_unpaid.png
│
└── report/
    └── manager_summary.md
```

## 9. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## 10. Running the Analysis

Clone the repository:

```bash
git clone https://github.com/AKrishnaK05/job-board-analysis.git

cd job-board-analysis
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Open the Jupyter Notebook:

```bash
cd notebooks
jupyter notebook analysis.ipynb
```

Execute the notebook cells sequentially to perform the data preparation, analysis and visualisation.