# Project 1: Standardized Test Analysis
#### _Rohazeanti Mohamad Jenpire_

### Problem Statement
In 2019, 31 states in the United States provides high school students with free SAT or ACT tests. While all colleges and universities accept both SAT and ACT, and both tests share similarities in terms of subjects tested, participation rates and scores for each test differ across the country. 
As a consultant to the US Department of Education, I want to find out which region to target to improve participation rates and scores for SAT and ACT.

I aim to answer the following:
1.	Do students from states that provide free SAT/ACT score better than those that are not?
2.	Is there a preference for SAT or ACT for states with no free tests?
3.	Do students from higher household_incomes do better than lower-income?
4.  Do students from higher Per Pupil Current Spending states do better than lower Per Pupil Current Spending states?

### Executive Summary
This project explores the 2019 SAT & ACT data which contains the state-by-state participation rates and mean scores for students who took the SAT and ACT tests in the United States. I also take the opportunity to explore 2019 Household Income and 2019 Per Pupil Current Spending datasets which contains state-by-state household income and per pupil current spending of Pulic Elementary and Secondary in United States. 

Exploratory data analysis revealed a seemingly strong positive correlation between the ACT composite score and household income as well as per pupil current spending. Higher household income and high per pupil current spending is likely to increase ACT composite score. 

Exploratory data analysis also revealed that there is a strong negative correlation between participation rate of SAT/ACT and their composite score. It is probable that what we observe is due to selection bias which skew the data analysis. 

Based on the insights obtained through the data analysis, efforts to increase composite score and participation rate should be focused on the South region, with view a of increasing per pupil current spending.  

### Data Sources
For this project, these are the datasets used:

[2019 SAT Dataset](./data/sat_2019.csv)

[2019 ACT Dataset](./data/act_2019.csv)

[2019 Household Income Dataset](./data/HouseholdIncome.csv)

[2019 Per Pupil Current Spending Dataset](./data/per_pupil_current_spending.csv)

[US State Region Dataset](./data/states.csv)
 

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT/SAT|Name of state where ACT and SAT data is taken| 
|sat_rate_19|float|SAT 2019|SAT participation rate in 2019, in percentage| 
|act_rate_19|float|ACT 2019|ACT participation rate in 2019, in percentage| 
|sat_composite|float|SAT 2019|SAT average composite score| 
|act_composite|float|ACT 2019|ACT average composite score| 
|household_income|float|Household Income|2019 Average household income of all the states, in USD| 
|ppcs|float|Per Pupil Current Spending|2019 Per Pupil Current Spending of Public Elementary and Secondary, in USD | 
|state|object|US State Region|Names of States in United States| 
|state_code|object|US State Region|State code of States in United States| 
|region|object|US State Region|Names of Regions in United States| 

### Conclusions and Recommendations
1.	Do students from states that provide free SAT/ACT score better than those that are not?
States where do not provide SAT/ACT tests scored better than those that states that provides free tests. However, it is probable that what we observe is due to selection bias. There is a negative correlation between Participation Rate and Composite score. For states that has high participation rate, it could be due to mandatory requirement by the state for students to take either SAT or ACT, whicheve the state chooses. Due to this, students may not take the test seriously, which resulted in lower mean scores. Whereas for states with low participation rates, the students who took the tests may have done it at their own will, are high achievers, resulting in high mean scores. 

2.	Is there a preference for SAT or ACT for states with no free tests?
Yes. Students from states where tests are not state-sponsored prefer SAT over ACT. We have observed that the mean for SAT participation rate is higher than ACT which infer that states that does not provide free tests favour SAT over ACT.

3.	Do students from higher household_incomes do better than lower-income?
Household income does not seem to affect scores of students who took SAT test. However, household income affects the scores of students who took ACT.  

4.  Do students from higher Per Pupil Current Spending states do better than lower Per Pupil Current Spending states?
Similarly, PPCS does not affect the scores of student who take SAT, but it affects scores of students that take ACT. 

**Recommendations**
Efforts to increase composite score and participation rate should be focused on the South region. We have noted that household income and PPCS affects ACT score. Hence, we proposed that states in the South region to mandate ACT, which automatically pushes the participation rate to 100%. As participation rate inversely affects composite score, we propose that the states to increase Per Pupil Current Spending; state funds to be spent more on provision of quality tutors, extra ACT preparatory classes and tests, make practice resources more readily available such as online resources, school libraries and e-learning.  

**Future project consideration:**
Additional data that would be helpful: 
Number of students that participated in each exam for each state for the score to be adjusted
Average time spent on studies per day
Social-economic statistics like race and demographics which may have an effect on the scoring amongst states.
