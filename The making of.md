# Individual Project

This is individual project as part of MSIS 2626: Dashboard, Scorecard, and Visualization class. The topic of interest is **City of Chicago’s Automated Speed Enforcement Program**.

There are 3 phases of this project:
* Data Exploration: The objective is to develop five distinct visualizations using Tableau that provide an effective overview of the data.
* First Version: The objective of this phase is to create a set of visualizations in an interesting, non-trivial, and somewhat unexpected
fashion intended for the Mayor of Chicago.
* Final Version: The objective of this phase is to further improvise our first version.

Reference: [Syllabus](https://github.com/mschermann/msis2629spring2019) & Professor comments.

## Data Exploration:

### Background:
As per [this](https://www.chicago.gov/city/en/depts/cdot/supp_info/children_s_safetyzoneporgramautomaticspeedenforcement.html) article: Chicago experiences roughly 3,000 crashes annually between motor vehicles and pedestrians, about 800 of which involve children. The Children’s Safety Zone Program protects children and other pedestrians by reminding motorists to slow down and obey speed laws – especially in school and park zones. Safety zones are designated as a 1/8th of a mile boundary around any Chicago parks or schools.

The City ordinance establishing the Children’s Safety Zone program substantially narrows the hours and locations of automated speed enforcement that are allowed under state law, and provides for the following:
* The enforcement hours will be limited from 7 a.m. to 7 p.m. in safety zones around schools on school days (Monday through Friday)
  * 7 a.m. to 4 p.m.: 20 miles per hour (mph) speed limit when children are present; and the posted speed limit when no children are present
  * 7 a.m. to 7 p.m.: The posted speed limit
* The enforcement hours around parks will be limited to only those hours parks are open (typically 6 a.m. to 11 p.m., 7 days a week) with a 30 mph speed limit
* Only warnings will be issued for the first 30 days after a cameras are newly-established in a safety zone
* The first time a vehicle owner is eligible to receive an actual ticket, they will instead receive a warning notice
* Fines for violations are $35 for vehicles traveling 6-10 mph over the posted speed limit while in a safety zone, and $100 for vehicles traveling 11 or more mph over the posted speed limit.  

Revenue from the program will be used for programs that enhance the safety of children, including afterschool, anti-violence and jobs programs; crossing guards and police officers around schools; and infrastructure improvements, such as signs, crosswalk markings and other traffic safety improvements.

### Data set information

[Dataset Source](https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4): The data reflects violations that occurred from July 1, 2014 until present, minus the most recent 14 days. 

### Exploration Results
Five distinct visualizations using Tableau that provide an effective overview of the data can be found [here](https://public.tableau.com/profile/bharati.malik#!/vizhome/Individual_Project_Visuals_1/SingleView).

## First Version:

In order to help Mayor of Chicago to make some informed decision based on the data, following are my findings.

* Finding 1:

Below is the visual from my data exploration phase. We can see here that there is a decreasing trend on the total number of violations per month. Also, June- September months were when the average number of violations were more! 
![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Phase1.JPG)

But this visual gives the overall picture of the total and average number of violations and does not take individual years or months or days into account. Thus, I graphed the same information at further granular level alongwith seasonal effects for better understanding.

![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Week.JPG)

As we can see, we have a decreasing trend of average number of violations with high and low spikes of average number of violations. Overall decrease in average number of violations would mean increased safety for the public of Chicago. But this would also mean a decrease in the revenue generated. As the revenue generated is further used for programs targetted for betterment of society, the fines should be increased which will help in increased revenue. 

![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Monthly.JPG)

I also wanted to check if there is a seasonality effect and I noticed the same seasonality effect as follows:
* Increases from Winter to Spring
* Increases from Spring to Summer
* Decreases from Summer to Fall
* Decreases from Fall to Winter

This visual tells us the seasonal effect and the trend of violations on an **average**.

* Finding 2:

From data exploration, we know that the enforcement hours are limited to certain hours during the weekday and school hours, which implies that the enforcement will not happen during summer. Does it mean that there is some kind of an error in capturing the number of violations? In order to further assess this, I explored camera id aspects for analysis. For this I calculated the **total** number of violations per unique camera and graphed it over time. I further added the seasonality effect to it. Again in summer, the number of violations captured were higher than other seasons. And winter has the least number of violations compared to other seasons. Does this mean the number of violations captured per camera are inflated due to technical glitch in cameras? 
Thus with this visual, Mayor of Chicago could increase the technical checks of the cameras to make sure if the violations captured were indeed correct.
 
* Finding 3:

