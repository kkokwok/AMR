Pet owners’ Knowledge, Attitudes, and Practices towards AMR and antibiotic-use Study
This repository contains the processed datasets used in the article:
[Knowledge and practices regarding antimicrobial resistance and antibiotic use among companion animal owners in Hong Kong: a cross-sectional survey with descriptive attitude findings]
[One Health Outlook]
The data support analyses of the prevalence of poor knowledge of antibiotic-use and antimicrobial resistance, and inappropriate antibiotic-use among Hong Kong pet owners using multivariable logistic regression to examine associated factors and compare these outcomes between self and pet contexts using McNemar’s chi-square test; attitudes were assessed as a secondary descriptive domain.

File in this repository
data_petkapstudy.xlsx/ data_petkapstudy.sav
Purpose
Primary analysis dataset used for descriptive analyses, paired self-pet comparisons using McNemar’s chi-square tests, logistic regression models, Pearson correlation coefficients and reliability analysis.
Structure
Long format (one row = one participant × one survey round)
Contents
The dataset includes:
Demographic characteristics of pet owners
Pet ownership information
Antibiotic-use questions on owners and for pets
KAP regarding antimicrobial resistance and antibiotic use on owners
Knowledge and practices regarding antimicrobial resistance and antibiotic use for pets
Derived score variables
Recoded grouping variables used in analysis
Notes
All variables required for the published univariate and multivariable logistic regression models, McNemar’s chi-square tests, Pearson correlation coefficients and reliability analysis are contained in this file.
No additional merging with other datasets is required for all statistical analysis.
Reproducing the analyses
To reproduce the published results:
Load data_petkapstudy.sav
Apply the case selection criteria described in the Methods section
Fit the univariate and multivariable logistic regression models, McNemar’s chi-square tests and Pearson correlation coefficients as specified in the article
No additional raw data files are required.

Data processing and scope
These datasets are processed research data, not raw survey exports
Variables were cleaned, recoded, and grouped before analysis.
The following steps were applied during data cleaning and processing:
Demographic characteristics of pet owners 
Gender
Age: Consolidated pet owners’ ages based on the study end date (EndDate, age_end_date, age) and categorised (age) into three groups (agegp)
Ethnicity: Converted free-text responses in Q3_8_TEXT, including “Chinese”, “香港人”, “Hong Kong”, and “Hk” to 1=Chinese in Q3
Marital status: Recoded Q4 into a binary variable (maritalgp)
Education: Categorised Q5 into three groups (edu_3gp)
Employment status: Recoded Q6 into a binary variable (employgp)
Field of study/work: Converted free-text responses in Q7_9_TEXT, including “精神健康”, “診所”, “復康”, “Physio”, “醫療”, “nursing” to 1=humanrelated in Q7_1, “寵物美容”, “獸醫”, “動物” to 1=humanrelated in Q7_2, “Chef”, “Pastry chef” to 1=humanrelated in Q7_5, “倒垃圾” to 1=humanrelated in Q7_6, “Biomedical Engineering” to 1=humanrelated in Q7_8 and Recoded (Q7_1, Q7_2, Q7_3, Q7_4, Q7_5, Q7_6, Q7_7, Q7_8) into a binary variable (employgp)
Household size: Categorised Q8 into three groups (livinggp)
Residential area
Pet ownership information 
Pet type
Number of pets: Recoded Q19 into a binary variable (Petno) 
Duration of pet ownership
Pet chronic illness
Antibiotic-use questions on owners 
History of antibiotic use in Hong Kong people: Recoded Q10 into a binary variable (SelfAnti)
Latest antibiotic use in Hong Kong people 
Personal hygiene instructions notice on antibiotics medicine bags: Recoded into a binary variable (SelfMedbag)
Antibiotic-use questions for pets
History of antibiotic use in pet cats/dogs: Recoded into a binary variable (PetAnti)
Latest antibiotic use in pet cats/dogs 
Advice from veterinary sites: Recoded into a binary variable (PetVet)
KAP regarding antimicrobial resistance and antibiotic use on owners
Knowledge of antibiotic use in Hong Kong people
Recoded (Q14, Q15_1, Q15_2) into a binary variable respectively (Q14_score, Q15_1_score, Q15_2_score)
Create (SumKnowAbxHKers) equal 1 if total score of (Q14_score, Q15_1_score, Q15_2_score) equals 3, else 0
(SumKnowAbxHKers) = 0 = poor
(SumKnowAbxHKers) = 1 = not poor
Knowledge of AMR in Hong Kong people
Recoded (Q16_1, Q16_2, Q16_3, Q16_4, Q16_5, Q16_6, Q16_7, Q16_8) into a binary variable respectively (Q16_1_score, Q16_2_score, Q16_3_score, Q16_4_score, Q16_5_score, Q16_6_score, Q16_7_score, Q16_8_score)
(SumKnowAbxHKers) = (Q16_1_score + Q16_2_score + Q16_3_score + Q16_4_score + Q16_5_score + Q16_6_score + Q16_7_score + Q16_8_score)
(PassKnowAMRHKers) was recoded from (SumKnowAbxHKers) using the 75th percentile as the cut-off.
(PassKnowAMRHKers) = 0 = score < 75th percentile = poor
(PassKnowAMRHKers) = 1 = score ≥ 75th percentile = not poor
Attitude towards AMR in Hong Kong people
Categorised (Q17_1, Q17_2, Q17_3, Q17_4, Q17_5, Q17_6) into three groups respectively (Q17_1_3, Q17_2_3, Q17_3_3, Q17_4_3, Q17_5_3, Q17_6_3)
1 = Disagree
2 = Neither agree nor disagree
3 = Agree
Use of antibiotic in Hong Kong people
Recoded (Q13_1, Q13_2, Q13_3, Q13_4, Q13_5, Q13_6, Q13_7) into a binary variable respectively (Q13_1_score, Q13_2_score, Q13_3_score, Q13_4_score, Q13_5_score, Q13_6_score, Q13_7_score)
(SumPractiseHKers) equals to 1, if any of (Q13_1_score, Q13_2_score, Q13_3_score, Q13_4_score, Q13_5_score, Q13_6_score, Q13_7_score) equals to 1
(SumPractiseHKers) = 0 = appropriate
(SumPractiseHKers) = 1 = inappropriate
Knowledge and practices regarding antimicrobial resistance and antibiotic use for pets
Knowledge of antibiotic use for pet cats/dogs
Recoded (Q26, Q27_10, Q27_11) into a binary variable respectively (Score_Q26, Score_Q27_10, Score_Q27_11)
Create (SumKnowAbxPet) equal 1 if total score of (Score_Q26, Score_Q27_10, Score_Q27_11) equals 3, else 0
(SumKnowAbxPet) = 0 = poor
(SumKnowAbxPet) = 1 = not poor
Knowledge of AMR for pet cats/dogs
Recoded (Q28_1, Q28_2, Q28_3, Q28_4, Q28_5, Q28_6, Q28_7, Q28_8, Q28_9) into a binary variable respectively (Q28_1_score, Q28_2_score, Q28_3_score, Q28_4_score, Q28_5_score, Q28_6_score, Q28_7_score, Q28_8_score, Q28_9_score)
(SumKnowAMRPet) = (Q28_1_score + Q28_2_score + Q28_3_score + Q28_4_score + Q28_5_score + Q28_6_score + Q28_7_score + Q28_8_score + Q28_9_score)
(PassKnowAMRPet) was recoded from (SumKnowAMRPet) using the 75th percentile as the cut-off.
(PassKnowAMRPet) = 0 = score < 75th percentile = poor
(PassKnowAMRPet) = 1 = score ≥ 75th percentile = not poor
Use of antibiotic in pet cats/dogs 
Recoded (Q25_1, Q25_2, Q25_3, Q25_4, Q25_5, Q25_6, Q25_7) into a binary variable respectively (Q25_1_score, Q25_2_score, Q25_3_score, Q25_4_score, Q25_5_score, Q25_6_score, Q25_7_score)
(SumPractisePet) equals to 1, if any of (Q25_1_score, Q25_2_score, Q25_3_score, Q25_4_score, Q25_5_score, Q25_6_score, Q25_7_score) equals to 1
(SumPractisePet) = 0 = appropriate
(SumPractisePet) = 1 = inappropriate

Ethical approval and data access
Data were collected with institutional ethical approval
All data are anonymized prior to sharing
Code used to generate manuscript tables
Demographic characteristics of pet owners reported in Table 1, univariate and multivariate logistic regression for owners’ knowledge and practice outcomes for their pet cats/dogs in Table 2-4, Pearson correlation matrix in Table 5 are generated in the SPSS Syntax.
Table 1. Characteristics of companion pet cat/dog owners surveyed
All code lines refer to file ‘syntax_petkapstudy’ with same heading.
Table 2. Univariate and Multivariate logistic regression for owners’ knowledge of pet cats/dogs’ antibiotic use
All code lines for univariate logistic regression refer to file ‘syntax_petkapstudy’ with same heading.
Key code lines for multivariate logistic regression:
LOGISTIC REGRESSION VARIABLES SumKnowAbxPet
  /METHOD=ENTER edu_3gp Fieldgp Q1 agegp Q18 Petno
  /CONTRAST (edu_3gp)=Indicator
  /CONTRAST (Fieldgp)=Indicator
  /CONTRAST (Q1)=Indicator(1)
  /CONTRAST (agegp)=Indicator(1)
  /CONTRAST (Q18)=Indicator(1)
  /CONTRAST (Petno)=Indicator(1)
  /PRINT=CI(95)
  /CRITERIA=PIN(0.05) POUT(0.10) ITERATE(20) CUT(0.5).
Table 3. Univariate and Multivariate logistic regression for owners’ knowledge of AMR for their pet cats/dogs 
All code lines for univariate logistic regression refer to file ‘syntax_petkapstudy’ with same heading.
Key code lines for multivariate logistic regression:
LOGISTIC REGRESSION VARIABLES PassKnowAMRPet
  /METHOD=ENTER edu_3gp Fieldgp Q21 Q1 agegp Q18 Petno
  /CONTRAST (edu_3gp)=Indicator
  /CONTRAST (Fieldgp)=Indicator
  /CONTRAST (Q21)=Indicator
  /CONTRAST (Q1)=Indicator(1)
  /CONTRAST (agegp)=Indicator(1)
  /CONTRAST (Q18)=Indicator(1)
  /CONTRAST (Petno)=Indicator(1)
  /PRINT=CI(95)
  /CRITERIA=PIN(0.05) POUT(0.10) ITERATE(20) CUT(0.5).
Table 4. Univariate and Multivariate logistic regression for owners’ practise of pet cats/dogs’ antibiotic use
All code lines for univariate logistic regression refer to file syntax_petkapstudy with same heading.
Key code lines for multivariate logistic regression:
LOGISTIC REGRESSION VARIABLES SumPractisePet
  /METHOD=ENTER SumKnowAbxPet Q1 agegp Q18 Q20 SumKnowAbxHKers PassKnowAMRHKers Petno 
  /CONTRAST (SumKnowAbxPet)=Indicator
  /CONTRAST (Q1)=Indicator(1)
  /CONTRAST (agegp)=Indicator(1)
  /CONTRAST (Q18)=Indicator(1)
  /CONTRAST (Q20)=Indicator
  /CONTRAST (SumKnowAbxHKers)=Indicator 
  /CONTRAST (PassKnowAMRHKers)=Indicator 
  /CONTRAST (Petno)=Indicator(1)
  /PRINT=CI(95)
  /CRITERIA=PIN(0.05) POUT(0.10) ITERATE(20) CUT(0.5).

Table 5. Correlation matrix of not poor knowledge of antibiotic use, AMR, and inappropriate antibiotic use
All code lines for correlation matrix refer to file ‘syntax_petkapstudy’ with same heading.

Code used to generate manuscript figures
McNemar’s chi-square test reported in Figure 1, number and proportion of respondents who correctly answered each pet antibiotic-use knowledge item in Figure 2, proportion of respondents who agreed, disagreed, or neither agreed nor disagreed with each attitude statement in Figure 3 are generated in the SPSS Syntax.
Figure 1(A). Comparison of antibiotic-use knowledge among all respondents (n = 388).
All code lines for McNemar’s chi-square test refer to file ‘syntax_petkapstudy’ with same heading.
Figure 1(B). Comparison of AMR knowledge among all respondents (n = 388).
All code lines for McNemar’s chi-square test refer to file ‘syntax_petkapstudy’ with same heading.
Figure 1(C). Comparison of inappropriate antibiotic-use practices among respondents with a history of antibiotic use for both themselves and their pets (n = 280).
All code lines for McNemar’s chi-square test refer to file ‘syntax_petkapstudy’ with same heading.
Figure 2. Pet antibiotic-use knowledge according to understanding of how antibiotics work among companion-animal owners (n=388).
All code lines for proportion of correct responses to Q27a–Q27i versus Q26, Q27j and Q27k refer to file ‘syntax_petkapstudy’ with same heading.
Figure 3. Attitudes towards antimicrobial resistance among companion-animal owners in Hong Kong (n=388).
All code lines for proportion of respondents who agreed, disagreed, or neither agreed nor disagreed with each attitude statement refer to file ‘syntax_petkapstudy’ with same heading.

Code used to generate supplementary table 
Reliability analysis of KAP statements reported in Supplementary Table ST1.
Supplementary Table ST1. Reliability analysis of KAP statements on pet cats/dogs’ owners and their pets
All code lines for reliability analysis refer to file ‘syntax_petkapstudy’ with same heading.	

Key variables used in univariate and multivariable logistic regression models, McNemar’s chi-square tests and Pearson correlation coefficients
Variable
Description
EndDate
Date of survey completion
age_end_date
Year of survey completion
Sum_Q14_Q15
Total score of Q14_score, Q15_1_score, Q15_2_score
Sum_Q26_Q27
Total score of Q26_score, Q27_10_score, Q27_11_score
SumKnowAbxHKers
If total score of Q14_score, Q15_1_score, Q15_2_score equals 3, this variable scores of 1 
SumKnowAbxPet
If total score of Q26_score, Q27_10_score, Q27_11_score equals 3, this variable scores of 1
SumKnowAMRHKers
Total score of Q16_1_score, Q16_2_score, Q16_3_score, Q16_4_score, Q16_5_score, Q16_6_score, Q16_7_score, Q16_8_score
SumKnowAMRPet
Total score of Q28_1_score, Q28_2_score, Q28_3_score, Q28_4_score, Q28_5_score, Q28_6_score, Q28_7_score, Q28_8_score, Q28_9_score
PassKnowAMRHKers
If score of SumKnowAMRHKers is 7 or above (75th percentile), this variable scores of 1
PassKnowAMRPet
If score of SumKnowAMRPet is 6 or above (75th percentile), this variable scores of 1
Sumhkerpractise
Total score of Q13_1_score, Q13_2_score, Q13_3_score, Q13_4_score, Q13_5_score, Q13_6_score, Q13_7_score
Sumpetpractise
Total score of Q25_1_score, Q25_2_score, Q25_3_score, Q25_4_score, Q25_5_score, Q25_6_score, Q25_7_score
SumPractiseHKers
If any of Q13_1_score, Q13_2_score, Q13_3_score, Q13_4_score, Q13_5_score, Q13_6_score, Q13_7_score equals 1 or above, this variable scores of 1
SumPractisePet
If any of Q25_1_score, Q25_2_score, Q25_3_score, Q25_4_score, Q25_5_score, Q25_6_score, Q25_7_score equals 1 or above, this variable scores of 1


