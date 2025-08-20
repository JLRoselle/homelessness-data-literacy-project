# Homelessness Data Literacy Project




## Table of Contents
* [PowerBI Dashboard](#powerbi-dashboard)
* [Motivation](#motivation)
* [Questions](#questions)
* [Normalizing the Data](#normaling-the-data)
* [Problems and Hurdles](#problems-and-hurdles)
* [Technologies Used](#technologies-used)
* [Sources](#data-sources)
* [Conclusion](#conclusion)

## PowerBI Dashboard
https://app.powerbi.com/view?r=eyJrIjoiNGI1Yjg1ZWQtZGFjMi00YTVhLTg0NjgtN2Y2YTRhNmFhMjEwIiwidCI6IjEwMWRhNTg3LTE4NDMtNGY1Mi04YjhhLTE3YjA2OWM2NmQzMyIsImMiOjJ9

## Motivation:
My motivation for this project is two-fold. First, after 3.5 years with Louisville Metro Government’s Office of Housing, I am well aware of the issues plaguing unhoused families and individuals in the United States. From over-priced housing to under-funded community resources, homelessness continues to be a nearly inescapable burden. I was deeply impacted by my time spent working with vulnerable individuals in unstable living conditions and wanted to take this opportunity to shine a light on the inequity inherent in a system that views the right to shelter as a commodity. 
Second, in the fast-changing world of AI and technology, the spread of misinformation is running rampant. As someone who has been educated around best analysis practices, I feel tasked to be a responsible steward-to provide clear, accurate findings, to reduce communication barriers, and to increase awareness and education surrounding the portrayal of data in today’s landscape of sensationalized media. 


## Questions:
1) Do homeless communities have access to adequate shelter on the national, state, and local level?
2) How are income and housing prices related?
3) Can numbers lie?  What lessons can be taught about correctly interpreting data and learning to recognize manipulations in visualizations?


## Normalizing the Data
The data sets I found came from different sources and covered different time periods. My first task was to streamline all acronyms, narrow down time frames for comparison, and bring together data from unrelated sources. I originally intended to work with a larger time frame, as HUD provides extensive national data going all the way back to 2007, but it was harder to access local records that covered as much, so I had to narrow my focus for comparison’s sake.

## Problems and Hurdles
All pricing and vacancy statistics had to be web scraped and then transformed into usable data frames. 
Localized population data was easy enough to find, but localized homelessness data proved more difficult to track down and included reaching out to local organizations (Launchpad and Nashville’s Office of Homelessness, specifically) to request the use of data that they had used in reports published online. 
There is not a data dictionary provided with HUD’s reports on homeless population and shelter availability, so I had to track down meanings for all acronyms and industry language.
 All HUD reports exist individually by year, so I had to add year columns and combine multiple tables for analysis. 


## Technologies Used
1) Python: for web scraping, exploratory analysis, normalization and aggregation of data
2) Power BI: for exploratory analysis and visualization
3) Excel: to acquire, download, and transform HUD reports
4) Google Sites: For website building
5) Git: for version control

## Data Sources
To answer the above questions I used the following sources to collect datasets for my analysis

1) 2007-2024 Point in Time and Housing Inventory Count by state:
2024 AHAR: Part 1 - PIT Estimates of Homelessness in the U.S. | HUD USER
https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fwww.huduser.gov%2Fportal%2Fsites%2Fdefault%2Ffiles%2Fxls%2F2007-2024-PIT-Counts-by-State.xlsb&wdOrigin=BROWSELINK

    2024 AHAR: Part 1 - HIC Estimates of Homelessness in the U.S. | HUD USER
    https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fwww.huduser.gov%2Fportal%2Fsites%2Fdefault%2Ffiles%2Fxls%2F2007-2024-HIC-Counts-by-State.xlsx&wdOrigin=BROWSELINK


2) HUD definitions of terms and acronyms:
A Guide to Counting Sheltered Homeless People (Third Revision)
https://www.hudexchange.info/sites/onecpd/assets/File/A-Guide-to-Counting-Sheltered.pdf

3) Nashville rental market history/trends:
Residential Rent Statistics for Nashville Tennessee | Department of Numbers
https://www.deptofnumbers.com/rent/tennessee/nashville/


4) Tennessee and Davidson County specific Homeless Counts
https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fwww.huduser.gov%2Fportal%2Fsites%2Fdefault%2Ffiles%2Fxls%2F2007-2024-PIT-Counts-by-CoC.xlsb&wdOrigin=BROWSELINK

    Tennessee and Davidson County specific Shelter Bed counts
    https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fwww.huduser.gov%2Fportal%2Fsites%2Fdefault%2Ffiles%2Fxls%2F2007-2024-HIC-Counts-by-CoC.xlsx&wdOrigin=BROWSELINK

## Conclusion
My analysis shows that, overall, Nashville is sheltering its homeless community at a slightly higher rate than average. There is still a shortage of shelter beds available in most years, but there is a less significant shortage in Davidson County than we see on the state and national level. There was a significant drop in homeless population in 2021 at all levels-most likely due to Covid-19 eviction moratoriums. But in all cases, those numbers spiked again in 2022 and have either remained steady or have continued to increase. 

Additionally, while it is often stated that homelessness numbers are rising due to an imbalance in housing prices and income, Nashville's rent to income ratio had stayed consistently around 20% before Covid. Nashville's vacancy rates have been increasing much more steadily than any other factor, which is likely due to a construction boom between 2010 and 2020 that has outpaced population growth. 

Regarding data literacy lessons, I sought to create intentionally misleading graphs and to explain what makes a visualization "good" or "bad". 
Through this practice, I affirmed my existing notion that color and shape are two easily manipulated variables that can either drive clear, concise reporting or lead any viewer astray. 
I also found that certain types of visualizations are useless when applied to certain data structures. For instance, a scatterplot is a virtually meaningless graph when looking at changes over time but a perfect tool to show correlation between related factors. 
A line and column chart is much more effective when comparing different values (count vs percentage) than when comparing same values of wildly varying amounts (10k vs 10m). A line chart is often much easier to read than an area chart. 
Charts over time should always have a linear aspect that can be grouped by date or time-be that a line chart, ribbon chart, or bar chart. 
Checking axes measurements, color coding, scale, and titles, legends and labels are a foolproof way to avoid being manipulated by data visualizations.  

While data cannot lie exactly, it can certainly obfuscate, confuse, and deceive.