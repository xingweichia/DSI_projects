# DSI_Project 1: SAT & ACT Analysis

### Overview
----

The new format for the SAT was released in March 2016. By having the data of participation rates and scores for SAT & ACT test in both 2017/2018, analysis with outside research to identify likely factors that influences participation rate and scores in various states helps us to provide recommendations to College Board on where money is best spent to improve SAT participation rates.


### Data Dictionary
----

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|act/sat|State|
|participation_act2017|float|act2017|Statewide ACT 2017 participation rates|
|english_act2017|float|act2017|State average English score for ACT 2017|
|math_act2017|float|act2017|State average Math score for ACT 2017|
|reading_act2017|float|act2017|State average Reading score for ACT 2017|
|science_act2017|float|act2017|State average Science score for ACT 2017|
|composite_act2017|float|act2017|State average Composite score for ACT 2017|
|participation_sat2017|float|sat2017|Statewide SAT 2017 participation rates|
|erw_sat2017|int|sat2017|State average Evidence-Based English Reading and Writing score for SAT 2017|
|math_sat2017|int|sat2017|State average Math score for SAT 2017|
|total_sat2017|int|sat2017|State average Total score for SAT 2017|
|participation_act2018|float|act2018|Statewide ACT 2018 participation rates|
|english_act2018|float|act2018|State average English score for ACT 2018|
|math_act2018|float|act2018|State average Math score for ACT 2018|
|reading_act2018|float|act2018|State average Reading score for ACT 2018|
|science_act2018|float|act2018|State average Science score for ACT 2018|
|composite_act2018|float|act2018|State average Composite score for ACT 2018|
|participation_sat2018|float|sat2018|Statewide SAT 2018 participation rates|
|erw_sat2018|int|sat2018|State average Evidence-Based English Reading and Writing score for SAT 2018|
|math_sat2018|int|sat2018|State average Math score for SAT 2018|
|total_sat2018|int|sat2018|State average Total score for SAT 2018|

### Observations & Summary
---

Analysis was done with the data by comparing the state participation rate and scores of SAT and ACT in year 2017/2018. Average test scores does not have much influence on the participation rate. However, individual state graduate requirement is a main factor that influences the participation rate for both test.

As majority of the states have made ACT as the mandatory test, higher participation rate in ACT test observed in both years. A negative linear correlation was observed between participation rate of ACT and participation rate of SAT in both years. States that have high participation rate in ACT test will tend to have low participation rate in SAT test and vice versa. 

An interesting trend of participation rate has been observed in some states. Colorado and Illinois has a drastic decrease in participation rate (from 100% to 30% and from 93% to 43%) for ACT and the drastic increase of participation rate (from 11% to 100% and from 9% to 99%) for SAT observed in the same years. This is due to Colorado making SAT test mandatory start from year 2018 and in the same year, ACT has lost the contract for being the test provider in Illinois. Thus, one can see the importance of individual state graduate requirement affecting the participation rate of both SAT and ACT tests.



### Conclusion & Recommendation
---

A pattern of states with higher SAT total scores and lower participation rates has been observed in both years. This is likely due to statewide requirement for mandatory ACT test. Students will less likely take both tests even if there is an option for them unless they are confident that they will score well. 

Only considering the states that doesn't require mandatory ACT test, Minnesota has a higher total SAT score even though the participation rate is less than 5%, which one can assume that students in Minnesota has the potential to do well in SAT test.

Considering Minnesota is in quite some debt, SAT test is a cheaper alternative for the state to implement as a graduation exam. College Board could focus their efforts to Minnesota in order to be the only test provider in this state. Thus, improving the participation rate for SAT test.
