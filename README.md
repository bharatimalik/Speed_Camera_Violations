# 'The Making of' Individual Project

This is individual project as part of MSIS 2626: Dashboard, Scorecard, and Visualization class. The topic of interest is **City of Chicago’s Automated Speed Enforcement Program**.

There are 3 phases of this project:
* Data Exploration: The objective is to develop five distinct visualizations using Tableau that provide an effective overview of the data.
* First Version: The objective of this phase is to create a set of visualizations in an interesting, non-trivial, and somewhat unexpected
fashion intended for the Mayor of Chicago.
* Final Version: The objective of this phase is to further improvise our first version.

Reference: [Syllabus](https://github.com/mschermann/msis2629spring2019) & Professor comments.

## Data Exploration

### Background

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

Snapshot of the same is as follows: 
![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Phase1.JPG)

## First Version

In order to help Mayor of Chicago to make some informed decision based on the data, [here](https://public.tableau.com/profile/bharati.malik#!/vizhome/Individual_Project_Visuals_2/FindingsforMayorofChicago) is the first version of the analysis. Snapshots of the same are also attached for each finding below:

### Finding 1

* From my data exploration phase we noticed a decreasing trend on the total number of violations per month. Also, June- September months were when the average number of violations were more! It gave me an overall picture of the total and average number of violations and did not take individual years or months or days into account. Thus, I graphed the same information at further granular level for better understanding.
* First, I took into account the violations per week. As we can see below, we have a decreasing trend of average number of violations with high and low spikes of average number of violations. 
* Overall decrease in average number of violations would mean increased safety for the public of Chicago. But this would also mean a decrease in the revenue generated. 
* Thus with this visual, Mayor of Chicago could increase fines for overall revenue generation which in turn are used for programs targetted for betterment of society. 

![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Week.JPG)

* Second, I took into account per day violations across the years. For this I created a calculated field to extract day from violation date using [this](https://community.tableau.com/thread/147716) as a reference. 
* We can see that the average violations happen over the weekend rather than weekday. 
* Thus with this visual, Mayor of Chicago could keep the same enforcement hours in weekend as on weekdays. 

![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Day.JPG)

### Finding 2

* I then created a calculated field called Seasons using an if-condition. This helped me to capture seasonality effect across months. 

![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Monthly.JPG)

* We notice the same seasonality effect across months as follows:
 * Increases from Winter to Spring
 * Increases from Spring to Summer
 * Decreases from Summer to Fall
 * Decreases from Fall to Winter

* The seasonality effect seen here goes with our intuitive thinking that people, on an average, spend more time outside during summer compared to other seasons and thus the chances of violations happening during summer is higher compared to other seasons. 
* Thus with this visual, Mayor of Chicago could keep the same enforcement hours in summer as in other seasons. 

### Finding 3

![Image](https://github.com/bharatimalik/Speed_Camera_Violations/blob/master/Camera.JPG)

* I further incorporated camera id for further analysis of the data. I calculated the total number of violations per unique camera and graphed it over time with seasonal effects. The number of violations captured in summer were quite high compared to other seasons. And winter had the least number of violations compared to other seasons. 
* From data exploration, we know that the enforcement hours are limited to certain hours during the weekday and certain cameras operate only during school hours. Does that mean that the number of violations captured per camera in summer are inflated due to technical glitch? 
* Thus with this visual, Mayor of Chicago could increase the technical checks of the cameras to make sure if the violations captured were indeed correct.

## Conclusion

* Data exploration and first version has made me comfortable with Tableau. It also gave me an understanding about the topic at hand.
* I also found few other datasets such as [Crime dataset](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2), [Red Light Violations](https://data.cityofchicago.org/Transportation/Red-Light-Camera-Violations/spqx-js37) and [Ward dataset](https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Ward-Offices/htai-wnw4). But when I tried merging the datasets, there were lot of null values that were generated. It also meant losing some of the information from the original dataset based on the merging condition. 
* Thus, I didn't merge any new datasets found online in order to keep the original data integrity intact.

## Road-map

* For revised version, I could combine the insights gained during exploration and first version together and use more advanced and interactive features of Tableau to represent the same information. 
* I may also be able to find any new insights using further data wrangling.
