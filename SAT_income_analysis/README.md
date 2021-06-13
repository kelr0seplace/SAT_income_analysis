### Project 1: SAT & ACT Analysis Overview



### Problem Statement

The fairness of the SAT (Scholastic Aptitude Test) has been called into question by some in recent years due to its potential  bias toward wealthier students. 'On average, students in 2014 in every income bracket outscored students in a lower bracket on every section of the test, according to calculations from the National Center for Fair & Open Testing.'¹ This purpose of this analysis is to see if statewide median household income and per pupil spending have any notable positive correlation to total SAT scores from 2017 and 2018.


### Executive Summary

This notebook begins by importing and cleaning the 2017 and 2018 data files for both the SAT. Once cleaned, I then imported and cleaned data files for annual household income and per pupil spending amounts for the corresponding years and perform some exploratory data analysis to uncover potential trends in the participation rates and scores for the SAT in 2017-2018. There was a slight positive correlation between participation and per pupil spending amounts, as well as between median household income and per pupil spending amounts. From there I explored these parameters with more granularity, isolating the top scoring and lowest scoring states to look for trends.

### Datasets using

| Dataset| Description| Year |
|--------|-----------|-------|
| SAT Scores by State | Breakdown of scores by state, participation rate, section | 2017 |
| SAT Scores by State | Breakdown of scores by state, participation rate, section | 2018 |

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|SAT 2017/2018|each state within the 50 contiguous US| 
| **us_state_abbrev** | *object* | SAT 2017/2018 | abbreviation of each state used in choropleth maps
|**sat_2017_participation**|*float*|SAT 2017|percentage of high school students (freshman through senior) in the state that took the SAT in 2017| 
|**evidence_based_reading_and_writing_2017**|*int*|SAT 2017|score between 200-800 (inclusive) measuring verbal reasoning, averaged over all test takers in state in 2017| 
|**math_2017**|*int*|SAT 2017| score between 200-800 measuring mathematical reasoning, averaged over all test takers per state in 2017| 
|**total_2017**|*int*|SAT 2017|sum of reading/writing and math score, averaged over all test takers per state in 2017| 
|**total_funding_2017**|*int*|SAT 2017| money spent by public schools per pupil in the year 2018,  may include teacher and administrator salaries, supplies, building maintenance, field trips, etc|
|**income_2017**|*int*|SAT 2017|median household income reported in 2017|
|**participation_2018**|*float*|SAT 2018|scaled score between 1-36 (inclusive) measuring mathematical reasoning, averaged over all test takers in a state in 2017|
|**evidence_based_reading_and_writing_2018**|*int*|SAT 2018|scaled score between 1-36 (inclusive) measuring reading comprehension, averaged over all test takers in a state in 2017|
|**math_2018**|*int*|SAT 2018|score between 200-800 measuring mathematical reasoning, averaged over all test takers per state in 2018|
|**total_2018**|*int*|SAT 2018| sum of reading/writing and math score, averaged over all test takers per state in 2017|
|**total_funding_2018**|*int*|SAT 2018|money spent by public schools per pupil in the year 2018,  may include teacher and administrator salaries, supplies, building maintenance, field trips, etc| 
|**income_2018**|*int*|SAT 2018|median household income reported in 2017| 


### Conclusions and Recommendations
Although we can see a slight correlation between total score and per pupil spending, further study is needed to support the claim that income has any definitive impact on total SAT score. It would appear that per pupil spending and median household income more greatly impact participation rates than SAT scores, and even then the relationship is subtle.

Given the multitudes of income disparities present in any particular state as a whole, it would be more telling to look at individual states and segment by county. A single average score per state does not tell the whole story of what is going on in different school districts where there are different curricula, private schools, public schools, etc. My recommendation would be to isolate states in different regions of the US and from there compare average scores of multiple districts within that state, increasing the number of samples and taking into consideration the diversity of the landscape. 

In looking at the data from 2017 to 2018, overall median scores DECREASED from 1107 to 1098, while per pupil spending and income both increased slightly by ~$400 and ~$2,653 respectively. In conclusion, if anything this analysis disproved the notion that income plays a part in SAT scores on a national scale, but it would be worth it to perform similar analyses on a more granular scale.




### Sources Used

Data:
¹https://www.wsj.com/articles/BL-REB-28270
https://www.census.gov/programs-surveys/school-finances.html
https://data.world/garyhoov/household-income-by-state
https://reports.collegeboard.org/pdf/2017-maryland-sat-suite-assessments-annual-report.pdf
https://www.census.gov/data/tables/2019/demo/income-poverty/p60-266.html
https://www.sde.idaho.gov/assessment/college/
https://collegereadiness.collegeboard.org/sat
https://collegereadiness.collegeboard.org/sat

Code:
https://plotly.com/python/choropleth-maps/
https://www.kite.com/python/answers/how-to-plot-a-line-of-best-fit-in-python
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.dtypes.html

