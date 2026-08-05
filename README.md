# Pet Owners’ Knowledge, Attitudes, and Practices Towards Antimicrobial Resistance (AMR) and Antibiotic Use Study

## Overview

This repository contains the processed datasets and analysis resources used in the study:

> **Knowledge and practices regarding antimicrobial resistance and antibiotic use among companion animal owners in Hong Kong: a cross-sectional survey with descriptive attitude findings**
>
> *One Health Outlook*

The data support analyses of:

- Knowledge of antibiotic use and antimicrobial resistance (AMR) among Hong Kong companion animal owners
- Antibiotic-use practices among pet owners and for their pets
- Comparative analyses between owner and pet contexts using McNemar’s chi-square tests
- Factors associated with knowledge and practice outcomes using univariate and multivariable logistic regression
- Correlation analyses and reliability assessments of knowledge, attitude, and practice (KAP) measures
- Descriptive analyses of attitudes toward AMR

---

# Repository Contents

## 1. `data_petkapstudy.xlsx`
## 2. `data_petkapstudy.sav`

### Purpose

Primary analysis dataset used for:

- Descriptive analyses
- McNemar’s chi-square tests
- Univariate logistic regression
- Multivariable logistic regression
- Pearson correlation analyses
- Reliability analyses

### Dataset Structure

- **Format:** Long format
- **Unit of observation:** One row = one participant × one survey round

### Dataset Contents

The dataset contains:

- Demographic characteristics of pet owners
- Pet ownership information
- Antibiotic-use history and behaviors of owners
- Antibiotic-use history and behaviors for pets
- Knowledge, attitudes, and practices (KAP) regarding AMR and antibiotic use among owners
- Knowledge and practices regarding AMR and antibiotic use for pets
- Derived score variables
- Recoded analytical grouping variables

### Notes

- All variables required to reproduce published analyses are included in the dataset.
- No additional datasets are required.
- No data merging is necessary.
- Data have already been cleaned, recoded, and processed for analysis.

---

# Reproducing the Analyses

To reproduce the published results:

1. Load `data_petkapstudy.sav`
2. Apply the case-selection criteria described in the Methods section of the manuscript
3. Perform analyses as specified in the manuscript:
   - Descriptive statistics
   - Univariate logistic regression
   - Multivariable logistic regression
   - McNemar’s chi-square tests
   - Pearson correlation analyses
   - Reliability analyses

No raw survey datasets are required.

---

# Data Processing and Scope

These datasets are processed research datasets rather than raw survey exports.

Variables were cleaned, recoded, grouped, and derived prior to analysis.

## Demographic Characteristics of Pet Owners

### Gender

Original gender responses retained.

### Age

Age was consolidated from:

- `EndDate`
- `age_end_date`
- `age`

Age was subsequently categorized into:

- `agegp`

### Ethnicity

Free-text responses recorded in `Q3_8_TEXT` including:

- Chinese
- 香港人
- Hong Kong
- Hk

were recoded as:

```text
Q3 = 1 (Chinese)
```

### Marital Status

`Q4` recoded into:

```text
maritalgp
```

### Education

`Q5` categorized into:

```text
edu_3gp
```

### Employment Status

`Q6` recoded into:

```text
employgp
```

### Field of Study / Work

Free-text entries in `Q7_9_TEXT` were reviewed and recoded.

Examples include:

**Human-health related**

- 精神健康
- 診所
- 復康
- Physio
- 醫療
- nursing

**Animal-related**

- 寵物美容
- 獸醫
- 動物

Additional responses recoded include:

- Chef
- Pastry chef
- 倒垃圾
- Biomedical Engineering

Variables `Q7_1`–`Q7_8` were subsequently combined into grouped variables used for analysis.

### Household Size

`Q8` categorized into:

```text
livinggp
```

### Residential Area

Residential location variables retained and grouped as used in analysis.

---

## Pet Ownership Information

Includes:

- Pet type
- Number of pets
- Duration of ownership
- Presence of chronic illness in pets

### Derived Variables

| Variable | Description |
|-----------|-------------|
| `Petno` | Binary recode of number of pets (`Q19`) |

---

## Antibiotic-Use Variables: Owners

### History of Antibiotic Use

`Q10` recoded into:

```text
SelfAnti
```

### Most Recent Antibiotic Use

Retained in processed format.

### Antibiotic Medicine Bag Instructions

Recoded into:

```text
SelfMedbag
```

---

## Antibiotic-Use Variables: Pets

### History of Antibiotic Use

Recoded into:

```text
PetAnti
```

### Most Recent Antibiotic Use

Retained in processed format.

### Advice from Veterinary Sites

Recoded into:

```text
PetVet
```

---

# Knowledge, Attitudes and Practices (KAP) Variables

## Knowledge of Antibiotic Use Among Hong Kong People

### Item-Level Scoring

Variables:

- `Q14`
- `Q15_1`
- `Q15_2`

recoded into:

- `Q14_score`
- `Q15_1_score`
- `Q15_2_score`

### Derived Outcome

```text
SumKnowAbxHKers
```

Scoring:

- Total score = 3 → `1` (Not Poor)
- Total score < 3 → `0` (Poor)

---

## Knowledge of AMR Among Hong Kong People

### Item-Level Scoring

Variables:

- `Q16_1`–`Q16_8`

were recoded into corresponding score variables.

### Total Score

```text
SumKnowAMRHKers
```

### Pass Variable

```text
PassKnowAMRHKers
```

Cut-off: 75th percentile

- Score < 75th percentile → Poor (`0`)
- Score ≥ 75th percentile → Not Poor (`1`)

---

## Attitudes Towards AMR Among Hong Kong People

Variables:

- `Q17_1`–`Q17_6`

were categorized into:

```text
Q17_1_3 – Q17_6_3
```

Response categories:

| Value | Category |
|---------|----------|
| 1 | Disagree |
| 2 | Neither agree nor disagree |
| 3 | Agree |

---

## Antibiotic-Use Practices Among Hong Kong People

Variables:

- `Q13_1`–`Q13_7`

were recoded into score variables.

### Derived Variable

```text
SumPractiseHKers
```

Classification:

- Any inappropriate practice present → `1` (Inappropriate)
- No inappropriate practices → `0` (Appropriate)

---

## Knowledge of Antibiotic Use for Pets

Variables:

- `Q26`
- `Q27_10`
- `Q27_11`

were recoded as:

- `Score_Q26`
- `Score_Q27_10`
- `Score_Q27_11`

### Derived Variable

```text
SumKnowAbxPet
```

Classification:

- Total score = 3 → `1` (Not Poor)
- Total score < 3 → `0` (Poor)

---

## Knowledge of AMR for Pets

Variables:

- `Q28_1`–`Q28_9`

were recoded into score variables.

### Total Score

```text
SumKnowAMRPet
```

### Pass Variable

```text
PassKnowAMRPet
```

Cut-off: 75th percentile

- Score < 75th percentile → Poor (`0`)
- Score ≥ 75th percentile → Not Poor (`1`)

---

## Antibiotic-Use Practices for Pets

Variables:

- `Q25_1`–`Q25_7`

were recoded into score variables.

### Derived Variable

```text
SumPractisePet
```

Classification:

- Any inappropriate practice present → `1` (Inappropriate)
- No inappropriate practices → `0` (Appropriate)

---

# Ethical Approval and Data Access

- Data collection was conducted under institutional ethical approval.
- All shared datasets are fully anonymized.
- No personally identifiable information is included in the repository.

---

# Code Used to Generate Manuscript Tables

Analyses were performed using SPSS syntax contained in:

```text
syntax_petkapstudy
```

## Table 1

**Characteristics of companion pet cat/dog owners surveyed**

All code lines are located under the corresponding section in:

```text
syntax_petkapstudy
```

---

## Table 2

**Univariate and Multivariate Logistic Regression for Owners’ Knowledge of Pet Cats/Dogs’ Antibiotic Use**

### Multivariable Model

Outcome:

```text
SumKnowAbxPet
```

Predictors:

- edu_3gp
- Fieldgp
- Q1
- agegp
- Q18
- Petno

---

## Table 3

**Univariate and Multivariate Logistic Regression for Owners’ Knowledge of AMR for Their Pet Cats/Dogs**

Outcome:

```text
PassKnowAMRPet
```

Predictors:

- edu_3gp
- Fieldgp
- Q21
- Q1
- agegp
- Q18
- Petno

---

## Table 4

**Univariate and Multivariate Logistic Regression for Owners’ Practice of Pet Cats/Dogs’ Antibiotic Use**

Outcome:

```text
SumPractisePet
```

Predictors:

- SumKnowAbxPet
- Q1
- agegp
- Q18
- Q20
- SumKnowAbxHKers
- PassKnowAMRHKers
- Petno

---

## Table 5

**Correlation Matrix of Knowledge and Antibiotic-Use Practices**

Generated using Pearson correlation analyses contained in:

```text
syntax_petkapstudy
```

---

# Code Used to Generate Manuscript Figures

## Figure 1A

Comparison of antibiotic-use knowledge among respondents (n = 388)

Method:

- McNemar’s chi-square test

---

## Figure 1B

Comparison of AMR knowledge among respondents (n = 388)

Method:

- McNemar’s chi-square test

---

## Figure 1C

Comparison of inappropriate antibiotic-use practices among respondents with antibiotic-use history for both themselves and their pets (n = 280)

Method:

- McNemar’s chi-square test

---

## Figure 2

Pet antibiotic-use knowledge according to understanding of how antibiotics work among companion-animal owners (n = 388)

Method:

- Proportion of correct responses for Q27a-Q27i versus Q26, Q27j and Q27k

---

## Figure 3

Attitudes towards antimicrobial resistance among companion-animal owners in Hong Kong (n = 388)

Method:

- Descriptive proportions of agreement, disagreement, and neutral responses

---

# Supplementary Materials

## Supplementary Table ST1

**Reliability Analysis of KAP Statements on Pet Owners and Their Pets**

Generated using reliability analysis procedures contained within:

```text
syntax_petkapstudy
```

---

# Key Analysis Variables

| Variable | Description |
|-----------|-------------|
| EndDate | Survey completion date |
| age_end_date | Year of survey completion |
| Sum_Q14_Q15 | Total score of Q14_score, Q15_1_score, Q15_2_score |
| Sum_Q26_Q27 | Total score of Q26_score, Q27_10_score, Q27_11_score |
| SumKnowAbxHKers | Not-poor knowledge of antibiotic use among Hong Kong people |
| SumKnowAbxPet | Not-poor knowledge of antibiotic use for pets |
| SumKnowAMRHKers | Total AMR knowledge score among Hong Kong people |
| SumKnowAMRPet | Total AMR knowledge score for pets |
| PassKnowAMRHKers | AMR knowledge score ≥ 75th percentile among Hong Kong people |
| PassKnowAMRPet | AMR knowledge score ≥ 75th percentile for pets |
| Sumhkerpractise | Total inappropriate-practice score among Hong Kong people |
| Sumpetpractise | Total inappropriate-practice score for pets |
| SumPractiseHKers | Binary indicator of inappropriate antibiotic-use practice among Hong Kong people |
| SumPractisePet | Binary indicator of inappropriate antibiotic-use practice for pets |

---

# Citation

If you use these data, please cite:

> Kwok KO, et al. *Knowledge and practices regarding antimicrobial resistance and antibiotic use among companion animal owners in Hong Kong: a cross-sectional survey with descriptive attitude findings*. One Health Outlook.

---

# Contact

For questions regarding the dataset, analysis, or repository contents, please contact the corresponding author(s) listed in the associated publication.
