## Project 1 - Supriya Sambhus

## Problem Statement

Lately standardised tests have been under the radar for being designed to favour richer students. We have been hired by the State of California to find out if there is indeed a correlation between SAT scores and poverty rates and participation rates in various school districts. This project seeks to analyse the participation rates and performance of all the school districts in California and report the findings and recommendations about remedial steps to the California State Board.

## Data Dictionary

**Data Set: df_perf_poverty** (Dataset containing SAT and ACT performance and participation data, merged with External Poverty Dataset)

|Feature|Type|Dataset|Description|
|:---|:---|:---|:---|
|cds|object|ACT & SAT|County/District/School code|
|c_code|object|ACT & SAT|County Code|
|c_d_code|object|ACT & SAT|County District Code|
|r_type|object|ACT & SAT|Record Type: C=County, D=District, S=School, X=State|
|d_name|object|ACT & SAT|District Name|
|c_name|object|ACT & SAT|County Name|
|sat_enroll12|float64|SAT|Enrollment of Grade 12 (Total number of students enrolled for Grade 12)|
|sat_num_tst_takr12|float64|SAT|Number of Test Takers for Grade 12 (For SAT)|
|sat_num_erw_benchmark12|float64|SAT|Number of test takers of grade 12 who got an ERW score above the Benchmark for Grade 12|
|sat_num_erw_benchmark12|float64|SAT|Percerntage of test takers out of total test takers for grade 12 who got an ERW score above the Benchmark for Grade 12|
|sat_num_math_benchmark12|float64|SAT|Number of test takers of grade 12 who got an Math score above the Benchmark for Grade 12|
|sat_pct_math_benchmark12|float64|SAT|Percerntage of test takers out of total test takers for grade 12 who got an Math score above the Benchmark for Grade 12|
|sat_tot_num_both_benchmark12|float64|SAT|Number of test takers of grade 12 who got both  Maths and ERW scores above the Benchmarks for Grade 12|
|sat_pct_both_benchmark12|float64|SAT|Percerntage of test takers out of total test takers for grade 12 who got both ERW and Math score above the Benchmarks for Grade 12|
|year|object|ACT & SAT|The Academic Year of the test|
|state_postal_code|object|Poverty Dataset|Two letter abbreviation for states using in Postal Codes of USA - CA for California|
|state_fips_code|int64|Poverty Dataset|Two-letter alphabetic codes defined in U.S. Federal Information Processing Standard Publication ("FIPS PUB") to identify U.S. states|
|district_id|int64|Poverty Dataset|District ID|
|name|object|Poverty Dataset|District Name|
|estimated_total_population|int64|Poverty Dataset|Estimated Total  Population of the district|
|estimated_population_5-17|int64|Poverty Dataset|Population of Children 5 to 17 years of Age|
|estimated_population_5-17_in_poverty|int64|Poverty Dataset|Estimated Number of Relevant Children 5 to 17 years old in Poverty Related to the Householder |
|act_enroll12|float64|ACT|Enrollment of Grade 12 (Total number of students enrolled for Grade 12)|
|act_num_tst_takr12|float64|ACT|Number of Test Takers for Grade 12 (For ACT)|
|num_act_benchmark12|float64|ACT|Number of test takers of grade 12 who got both  ACT scores above the Benchmarks|
|pct_act_benchmark12|float64|ACT|Percentage of test takers of grade 12 who got both  ACT scores above the Benchmarks|
|pct_5-17_in_poverty|float64|Poverty Dataset|Percentage of children 5 to 176 years old in poverty in the given district (estimated_population_5-17_in_poverty / estimated_population_5-17)|
|sat_participation|float64|SAT|Participation percentage for SAT Test for Grade 12 (sat_num_tst_takr12 / sat_enroll12)|
|act_participation|float64|ACT|Participation percentage for ACT Test for Grade 12 (act_num_tst_takr12 / act_enroll12)|

## Analysis Done

Exploratory Data Analysis: Summary of EDA is shared below:
**Performance vs Poverty Rates - SAT and ACT**<br>
Based on the Exploratory Data Analysis we find that the top 5 districts in terms of performance of students in SATs and ACTs have a much lower mean poverty rate in children between 5 to 17 years when compared to the bottom 5 districts. 

**Participation vs Poverty Rates - SAT**<br>
We find that the top 5 districts in terms of participation rates for SATs have slightly lower poverty rate in children between 5 to 17 years when compared to the districts with lowest participation rates. 

**Participation vs Poverty Rates - ACT**<br>
We also find that the top 5 districts in terms of participation rates for ACTs actually higher poverty rate in children between 5 to 17 years when compared to the districts with lowest participation rates. However when we extend the analysis to top 20 districts, the poverty rates are slightly lower than the districts with lowest participation rates. 

Visualisation: Some important analysis by visualisation is summarised below

**Heatmap**:
Based on the headmap we see a negative correlation of -0.69 between SAT participants above benchmarks vs poverty rates of children between 5 to 17 years by district. 

Based on the headmap we see a negative correlation of -0.71 between ACT students above benchmarks vs poverty rates of children between 5 to 17 years by district. 

Based on the headmap we see a negative correlation of -0.0.18 between ACT students above benchmarks vs poverty rates of children between 5 to 17 years by district. 

Based on the headmap we see a negative correlation of -0.0.11 between ACT students above benchmarks vs poverty rates of children between 5 to 17 years by district. 

**Histograms**:
The distribution of the SAT performance by districts is normal and centred around the mean (48.81) and the median (48.03).

The distribution of the ACT performance by districts is skewed slightly to the left. It has a mean of (56.41) and a median (59.55). 

The histogram of SAT participation is fairly normally distributed around the Mean (32.99) and the Median (31.16) with a slight righ skew due to the long right tail. 

The histogram of ACT participation is skewed to the right with a mean of 18.46 and a Median 15.4. 

**Scatter Plots**

We can see a strong negative correlation between the poverty rates and the SAT performance of students in the districts in California. At the highest poverty rate of around 42%, the % of students scoring above benchmark is around 17%. At the lowest poverty rate of around 2%, the % of students scoring above benchmark is around 79%.  

We can see a strong negative correlation between the poverty rates and the ACT performance of students in the districts in California. At the highest poverty rate of around 42%, the % of students scoring above benchmark is around 10%. At the lowest poverty rate of around 2%, the % of students scoring above benchmark is around 92%.  

We can see a weak negative correlation between the poverty rates and the SAT participation of students in the districts in California. At the highest poverty rate of around 42%, the SAT participation is around 30%. At the lowest poverty rate of around 2%, the SAT participation 38%. There are some outliers seen with participation rates abobe 60% irrespective of poverty rates.

We can see a weak negative correlation between the poverty rates and the ACT participation of students in the districts in California. At the highest poverty rate of around 42%, the ACT participation is around 38%. At the lowest poverty rate of around 2%, the ACT participation is around 50%. There are some outliers seen with participation rates abobe 40% irrespective of poverty rates.

## Conclusions and Recommendations

**Conclusion**

**There is a significant negative correlation between poverty rates in the districts of the state of California and the students performance in the SAT and ACT tests.** 

**There is a weak (alomost none) correlation between poverty rates in the districts of the state of California and participation of students in the SAT and ACT tests.** 

Further research shows that richer stuednts have an unfair advantage when taking the standardised tests due to access to better funded schools,private tutors and standardized test preparation classes, high costs of tests (source: www.cnbc.com/amp/2019/10/03/rich-students-get-better-sat-scores-heres-why.html). 

**Recommendation**

**The state of california should focus it's resources in trying to reduce the impact of poverty as a factor in standardised test performance.**

It can do so by:  
1. Provide funding to offer **test counselling and test preparation classes**
2. **Subsidies** to make re-taking the tests affordable
3. Allocate **funding for schools in poorer districts** to provide better support for studente
4. Encourage colleges to **reduce the relative weightage given to standardised test scores** for college admissions procedure
