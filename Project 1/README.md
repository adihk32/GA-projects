# Project 1: Analysis of SAT Compulsory Requirement with Its Scores for High School Graduation Criteria 

### Problem Statement:

- Since the new changes on SAT format from 2016, many states started to implement the SAT as their standardised test to graduate from high school. Thus, they offer complimentary SAT for their juniors or seniors. This project aims to check whether a compulsory SAT is the way to go for other states to implement as well or an optional but complimentary SAT is better for the states legislative to consider.
---

### Background:
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

Since 2016, SAT has been formatted to become 2 section only as per above with the maximum score of 1600, consists of maximum score of 800 from Evidence-Based Reading and Math respectively, the minimum score of each part is 200 ([*source*](https://blog.prepscholar.com/complete-guide-to-the-new-sat-in-2016#:~:text=Format%20Changes,still%20scored%20out%20of%20800.)). After the new formatting, many states legislative started to take SAT as the standardised test to graduate from high school, list of the states with compulsory SAT can be find below at Additional Information section. While some states started to provide free & optional SAT for students who wanted to participate.

In 2019, according to survey from Pew Research Centre ([*source*](https://eab.com/insights/daily-briefing/enrollment/75-of-teens-plan-to-attend-higher-ed-after-high-school/)), 59% of U.S teens intend to attend four year college, while the other 16% plan to attend other forms of higher ed studies, such as trade schools where most of them do not require SAT ([*source*](https://cetweb.edu/do-trade-schools-require-sat-scores/)). There is also 22% of teens still unsure of their plan. A

Meanwhile in another survey from Niche in 2021 ([*source*](https://www.niche.com/about/new-survey-75-of-high-school-juniors-believe-their-chances-of-acceptance-will-be-hurt-without-sat-act-scores/)), there is 75% of high school juniors believe that the university admission will be affected if they do not take SAT/ACT.

Therefore, we need to find out if compulsory SAT is necessary for state legislative to implement across the nation.


### Datasets Selected:
- sat_2017.csv
- sat_2018.csv
- sat_2019.csv
---

### Additional Information:
- Here are the states that implement compulsory SAT for their high school students:
1. [*Colorado*](https://testive.com/colorado-sat-change-2017/), since 2017 
2. [*Connecticut*](https://www.nytimes.com/2015/08/07/nyregion/connecticut-to-require-all-11th-graders-to-take-the-sat.html#:~:text=With%20approval%20from%20the%20United,the%202015%2D16%20school%20year.), since 2016 
3. [*Delaware*](https://whyy.org/articles/sat-to-replace-smarter-balanced-as-delawares-11th-grade-standardized-test/), since 2016 
4. [*Idaho*](https://www.kivitv.com/news/education/making-the-grade/idaho-could-drop-sat-requirement-waives-rule-for-2022-graduates#:~:text=THE%20SAT%20IN%20IDAHO,would%20have%20a%20postsecondary%20education.), since 2012 
5. [*Illinois*](https://www.chicagotribune.com/news/ct-illinois-chooses-sat-met-20160211-story.html), since 2017 
6. [*Maine*](https://legislature.maine.gov/testimony/resources/EDU20210303@OPLA132601326855083564.pdf), since 2006 
7. [*Michigan*](https://www.bridgemi.com/talent-education/what-michigans-switch-sat-means-high-school-students), since 2016 
8. [*New Hampshire*](https://www.education.nh.gov/who-we-are/division-of-learner-support/bureau-of-instructional-support/sat), since 2016    
9. [*Rhode Island*](https://www.providencejournal.com/news/20181025/with-sat-required-ri-sees-jump-in-participation-decline-in-scores#:~:text=In%202018%2C%20the%20SATs%20and,SAT%20to%20students%20for%20free.), since 2017 
10. [*West Virginia*](https://www.wsaz.com/content/news/All-WVa-high-school-juniors-to-begin-taking-SAT-exam-beginning-Spring-2018-444248263.html), since 2018

- Here are the states that offers free and optional SAT for their high school students ([*source*](https://prepmaven.com/blog/test-prep/states-require-sat-act/)):
1. District of Columbia
2. Oklahoma
3. South Carolina
4. Tennessee
5. Ohio
---

### Data Dictionary:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|sat_2017_to_2019.csv|The state where the high school graduate who take SAT test|
|**participation_2017**|*float*|sat_2017_to_2019.csv|The percentage of the high school graduate who took the SAT test in 2017|
|**evidence_based_read_and_write_2017**|*integer*|sat_2017_to_2019.csv|Average Evidence-Based Reading & Writing section test score (200-800) of high school graduates by states in 2017|
|**math_2017**|*integer*|sat_2017_to_2019.csv|Average Math section test score (200-800) of high school graduates by states in 2017|
|**total_2017**|*integer*|sat_2017_to_2019.csv|Average Total test score (max. 1600) of high school graduates by states in 2017|
|**participation_2018**|*float*|sat_2017_to_2019.csv|The percentage of the high school graduate who took the SAT test in 2018|
|**evidence_based_read_and_write_2018**|*integer*|sat_2017_to_2019.csv|Average Evidence-Based Reading & Writing section test score (200-800) of high school graduates by states in 2018|
|**math_2018**|*integer*|sat_2017_to_2019.csv|Average Math section test score (200-800) of high school graduates by states in 2018|
|**total_2018**|*integer*|sat_2017_to_2019.csv|Average Total test score (max. 1600) of high school graduates by states in 2018|
|**participation_2019**|*float*|sat_2017_to_2019.csv|The percentage of the high school graduate who took the SAT test in 2019|
|**evidence_based_read_and_write_2019**|*integer*|sat_2017_to_2019.csv|Average Evidence-Based Reading & Writing section test score (200-800) of high school graduates by states in 2019|
|**math_2019**|*integer*|sat_2017_to_2019.csv|Average Math section test score (200-800) of high school graduates by states in 2019|
|**total_2019**|*integer*|sat_2017_to_2019.csv|Average Total test score (max. 1600) of high school graduates by states in 2019|
|**total_mean**|*float*|sat_2017_to_2019.csv|Average of the mean total score from 2017 to 2019 by states|
|**participation_mean**|*float*|sat_2017_to_2019.csv|Average of the participation rate from 2017 to 2019 by states|
|**state_requirement**|*object*|sat_2017_to_2019.csv|The requirement of SAT at each state (compulsory, free & optional, NA)|

---

### Findings: 
- Michigan, Connecticut and Delaware has a 100% participation rate for these three years as they are a compulsary test to graduate high school
- Across the year 2017 to 2019, we can see that the state with higher participation rate has lower total score (below the 25% percentile) while the state with lower participation rate has higher total score (above the 75% percentile), meaning there is inverse relationship between the participation rate and mean total score
- Based on the highest average of total score mean, the top 5 state has a participation rate below 5%. As for the lowest average of total score mean, the top 5 state has at least 90% participation rate, except for West Virginia which only has 47% participation rate
- Colorado and Illinois participation rate grow around 90% after the new requirement to make SAT compulsory since 2017
- For Rhode Island, although the compulsory SAT regulation come to effect since 2017, but the participation rate before 2017 is considered quite high as well (71%)
- We also see a spike in participation rate at West Virginia after 2018, which came to about 70% increment
- District of Columbia participation rate remains high (>90%) throughout the year, eventhough participation is optional 
- Oklahoma, South Carolina and Tennessee, which optional free SAT, did see an increase in participation rate throughout the years
- From the total score average group by the state requirement, we can see that the SAT score mean is higher in the state where there is no requirement on SAT. Where as if we were to compare the compulsory and free & optional state, the states that provide free & optional SAT has a higher mean of the total score.
- The average participation rate at the states where SAT is free & optional is below 50%
---

### Conclusions/Recommendations:

**Conclusions :**
- Based on our findings above, we can imply that the state with the compulsory SAT requirement has no clear advantage over the one that offers free & optional SAT or none. This maybe caused due to the students' choice over the higher education that they wanted to attend since SAT is required only for most of the universities. Thus, those students does not prepare for the SAT
- As for the other states without any compulsory SAT requirement, the students voluntarily apply for the test itself, as a result they will be more prepared to score higher for their university admission. This can also be found in the relationship between SAT scores and participation rate above.

**Recommendations :**
- To provide free & optional SAT test instead of compulsory SAT. This will allow the students to have choice on what they want to pursue. 
- To provide better preparations for the student who choose to go for SAT so they will not have to take multiple attempts in order to save time.
- The remaining budget for the compulsory SAT can be allocated for other types of test that is more suited for the trade school or higher education study.
- To provide consultation/survey for students to get better idea of what is their plan or to advise them if they are doubtful 