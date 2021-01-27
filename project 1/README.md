# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

## Problem Statement
In this Project, I am keen to explore the probable causes of a change in participation rate in ACT and SAT from 2017 to 2018 and look at the probable causes for the shift in participation. 

## Executive Summary

Throughout this project, I will demonstrate the exploration and visualisation of data using the various libraries in python, such as seaborn, numpy, pandas and matplotlib. Ultimately, I will look to explore the for objective of this project.

### Contents:
- [2017 Data Import & Cleaning](#2017-Data-Import-and-Cleaning)
- [2018 Data Import and Cleaning](#2018-Data-Import-and-Cleaning)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Data Visualization](#Visualize-the-data)
- [Descriptive and Inferential Statistics](#Descriptive-and-Inferential-Statistics)
- [Outside Research](#Outside-Research)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)


## Datasets

For this project, I will be using the following datasets:

- [2017 SAT Scores](./data/sat_2017.csv)
- [2017 ACT Scores](./data/act_2017.csv)
- [2018 SAT Scores](./data/sat_2018.csv)
- [2018 ACT Scores](./data/act_2018_updated.csv)

These data give average SAT and ACT scores by state, as well as participation rates, for the graduating class of 2017.

You can see the source for the SAT data [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/), and the source for the ACT data [here](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows).

2018 state-by-state average results and participation for the SAT are available in PDF reports [here](https://reports.collegeboard.org/sat-suite-program-results/state-results). 2018 ACT state-by-state mean composite scores and participation rates are [here](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf) .

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|object|SAT/ACT| State which the exam took place.|
|**participation_2017sat**|float|SAT|Percentage off the population in the state that participated in the exam (unit 1 = 1%, meaning 61 = 61%|
|**evidence_based_reading_and_writing_2017sat**|float|SAT|Average score of evidence-based reading and writing test of the population by state|
|**math_2017sat**|float|SAT|Average score of math test of the population by state|
|**total_2017sat**|float|SAT|Population mean by state of total scores of all the exams in SAT|
|**participation_2018act**|float|SAT|Percentage off the population in the state that participated in the exam (unit 1 = 1%, meaning 61 = 61%|
|**evidence_based_reading_and_writing_2018sat**|float|SAT|Average score of evidence-based reading and writing test of the population by state|
|**math_2018sat**|float|SAT|Average score of math test of the population by state|
|**total_2018sat**|float|SAT|Population mean by state of total scores of all the exams in SAT|
|**participation_2017act**|float|ACT|Percentage off the population in the state that participated in the exam (unit 1 = 1%, meaning 61 = 61%|
|**english_2017act**|float|ACT|Average score of english test of the population by state|
|**math_2017act**|float|ACT|Average score of math test of the population by state|
|**reading_2017act**|float|ACT|Average score of reading test of the population by state|
|**science_2017act**|float|ACT|Average score of science test of the population by state|
|**composite_2017act**|float|ACT|Population mean by state of composite scores (composite score is the mean of score of all the scores in ACT)|
|**participation_2018act**|float|ACT|Percentage off the population in the state that participated in the exam (unit 1 = 1%, meaning 61 = 61%|
|**english_2018act**|float|ACT|Average score of english test of the population by state|
|**math_2018act**|float|ACT|Average score of math test of the population by state|
|**reading_2018act**|float|ACT|Average score of reading test of the population by state|
|**science_2017act**|float|ACT|Average score of science test of the population by state|
|**composite_2018act**|float|ACT|Population mean by state of composite scores (composite score is the mean of score of all the scores in ACT)|

## Conclusion and Recommendations

From the data that I have explored and trends that appeared by looking at the data, my conclusion is that participation rate is an influence of the state's policy. From making it mandatory or supporting the financial aspect and making it accessible to students, these policies have mada a positive impact on the participation rate.

I would also like to highlight Iowa from the dataframe. Iowa reflects the lowest total participation in 2017 (participation ACT 2017 + participation SAT 2017) and 2018 (participation ACT 2018 + participation SAT 2018) with a total participation rate of 69% and 71% respectively.

Simply basing my interpretation based on the 3 states i have mentioned before, my recommendations towards Iowa would be to also implement such a policy. Having a state level intervention, by either making it accessible or simply mandating it upon students will have the outcome desired, which is to boost the participation rate of the students in the standardised test such as SAT and ACT.

Although the recommendation would be straightforward, it is also interesting to note that some colleges are dropping [ACT and SAT requirements for admission during this coronavirus period](https://www.nytimes.com/article/sat-act-test-optional-colleges-coronavirus.html#:~:text=the%20main%20story-,More%20Colleges%20Are%20Waiving%20SAT%20and%20ACT%20Requirements,testing%20requirements%20for%202021%20applicants.&text=They%20are%20a%20rite%20of,students%3A%20the%20SAT%20and%20ACT.). The waiver might be temporary and for some, extended periods. As we navigate through the current coronavirus, it would be probable that the recommendation would cease to be relevant. Perhaps as schools try to achieve a better education for the students, a common ground can be found soon to be able to push students into colleges in the US.

