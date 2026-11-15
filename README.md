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
- The median response time is 7