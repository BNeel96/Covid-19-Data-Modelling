# Covid-19-Data-Modelling

#### -- Project Status: [Completed]

## Project Intro/Objective
The purpose of this project is to conduct Data Analysis with JHU Covid-19 Dataset. The primary objective is to answer Analytical Questions around Vaccination effectivesness and Policy Making around Mask usage. We discuss the potential impact of Vaccination on the count of Confirmed Covid-19 Cases in the states of Virginia, Maryland and Massachussets. Followed by this we take a look at how mask policy affected the Covid-19 spread, by comparing New York and Texas confirmed cases after 15th April, 2020. The aim of the project is to come up with data-driven insights for better policy making and governance

### Partner
* Neel Barge, Janet Zhuang, Yuxin Zhang, Zaurez Hamid, Ranchen Huang, Ming Tang and Zhangtao Ying


### Methods Used
* Relational Database
* Data Visualization

### Technologies
* Python
* PostGres, MySql
* Pandas, jupyter
* Amazon EC2

## Project Description

**Data Source**
* JHU Datasets: https://coronavirus.jhu.edu/about/how-to-use-our-data
* Cases: https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports_us
* Deaths: https://github.com/govex/COVID-19/blob/master/data_tables/vaccine_data/us_data/time_series/vaccine_data_us_timeline.csv & https://raw.githubusercontent.com/govex/COVID-
* Vaccine: https://github.com/govex/COVID-19/blob/master/data_tables/vaccine_data/us_data/time_series/vaccine_data_us_timeline.csv
* People Vaccinated: https://raw.githubusercontent.com/govex/COVID-19/master/data_tables/vaccine_data/us_data/time_series/people_vaccinated_us_timeline.csv
* Testing: https://raw.githubusercontent.com/govex/COVID-19/master/data_tables/testing_data/time_series_covid19_US.csv 
* Dictionary files of above data:
https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/README.md
https://github.com/govex/COVID-19/blob/master/data_tables/vaccine_data/us_data/data_dictionary.csv
https://github.com/govex/COVID-19/blob/master/data_tables/testing_data/data_dictionary.csv

**Star Schema**
   ![StarSchema](https://user-images.githubusercontent.com/89561764/188337616-c62dfac1-d61c-439f-b16f-89816779172f.jpg)
   |:--:|
   
**Analytical Queations**
* **How does government regulation effect spread of covid 19?**
   <img width="732" alt="NY" src="https://user-images.githubusercontent.com/89561764/188339610-5c75ba8f-deb6-46d2-a6ec-a1b6c6a6cd7c.png">
   <img width="731" alt="FL" src="https://user-images.githubusercontent.com/89561764/188339620-9a7d2775-e944-4ef5-8cb6-8c4ee494e7ce.png">

On comparing the percentage change of Confirmed Cases between New York(NY) and Florida(FL), NY has substantially lower confirmed cases after NY government ordered shutdown and reopened step by step meeting the phase requirement, before the vaccine came out. Government of FL did not take strict actions to slow the spread of COVID-19. Therefore, people had more chance of getting exposed to Virus which led to increase in Confirmed case percent change. So, government regulation has made some contribution to slow the spread of COVID-19. This also lead to an intuiative result of increased death percent change in FL than NY.

* **What is the effectiveness of vaccine**
   <img width="710" alt="Effectiveness" src="https://user-images.githubusercontent.com/89561764/188337916-1dd8992c-95c5-4b5b-b60f-cbc97ae0ed85.png">

The data is between 01-02-2021 and 11-16-2021, as it is around this time people started to get vaccinated.
In the first graph, the x-axis is months and y-axis is confirmed cases, while the second graph has months on x-axis and count of fully vaccinated people on y-axis. In the Second graph, we can see that from January to June, the growth rate of people getting vaccinated concaves up. After June, the growth rate gradually reduces. This is mainly caused by the fact that majority of people have been vaccinated. For the first graph, we can see, thanks to the vaccine, the growth rate of confirmed case is concaving down. Meaning even though there are more people getting covid, the spread has been gradually controlled.
However, we can see from August to November, the growth rate shoots, meaning the spread is accelarating. As you may remember, that is around this time  Delta Variant was discovered, a variant that is much more destructive. Also, since majority of people have been vaccinated, people start being less protective of themseleves, giving more exposure to the new variant. Based on this analysis, vaccine is the best way to fight virus. Given the current accelrated spread of virus, it would be a better choice to have a booster shot and wear masks.

* **During thanksgiving holidays and Christmas holiday 2020, did cases/ death increase significantly?**

We observe that the COVID-19 Death rates for the Holiday period totalling to 40 days, from Thanksgiving to New Years has increased by 117, from 677 on 11-26-2020 to 794 on 01-04-2021.
On comparing similar time period for 40 days before the holidays we see 32 death cases, while after the holidays there was a drastic increase in death cases accounting to a total of 179.

* **Explore how the mask policy affected the covid-19 spread by comparing NY and TX confirmed cases after 4/15/2020 NY started to mandate mask outdoor**

   <img width="760" alt="MaskPolicy" src="https://user-images.githubusercontent.com/89561764/188338464-dea08089-57b2-498d-8813-062052bc1533.png">
   <img width="573" alt="ConfirmedCases" src="https://user-images.githubusercontent.com/89561764/188338505-51a39b3b-f8fc-43ef-ad7e-4300d922c926.png">

With these three plots, we can see how the outdoor mask mandate policy affects the New York state covid spread, after 04-15-2020. New York has a higher population density than Texas, but the increasing trend of new confirmed cases is lower compared to Texas. Since Texas does not have any mask mandate until 03-10-2021.


## Needs of this project

- Bulk Loading
- Data processing/cleaning
- Data exploration/Descriptive statistics
- writeup/reporting
