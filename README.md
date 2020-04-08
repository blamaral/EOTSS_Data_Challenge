### Executive Summary

#### Objective: Are there commonalities or trends among establishments that perform poorly?

**Preliminary information:** There were 72243 times establishments were graded within a 6 year span (2012-01 to 2018-06), however, only 7558 of those establishments were unique, meaning establishments are repeatedly graded throughout the years. Note that only half of the year of 2018 have records.


After looking through the dictionaries of the csv documents, I decided that any establishment with a result of *'HE_Fail', 'HE_FailExt', 'HE_Hearing', 'HE_OutBus', 'HE_TSOP'* at least once in a year was performing poorly. I did not include *HE_Filed* in this estimate because although the inspection did not pass, the inspector still deemed the results good enough not to require further re-inspection. While conducting analysis on the violations data, I noticed that there were additional results, and subsequently added *'HE_Closure', 'HE_Misc', 'HE_FAILNOR'* to this list.

I first approached the objective by taking all establishments that had those poor results. I noticed that the majority of establishments that perform poorly were graded C. This is to be expected as grades are determined by what/how many violations. While only making up 16.5% of the total establishments, they were 44.4% of the poorly performing establishments. However, the most frequent scores for poorly performing establishments were graded A and B as shown below:
* 90 with 1845 and frequency of 6.9257%
* 88 with 1650 and frequency of 6.1937%
* 98 with 1573 and frequency of 5.9047%
* 94 with 1267 and frequency of 4.7560%
* 86 with 1266 and frequency of 4.7523%

Although this was surprising at first, this indicates that there are far more varying scores that are in the grade C range. This aligns with the grading system as a grade of C is a larger range itself and is not limited whereas there is a maximum value a score can be is capped at 100.

There were a total of 467 establishments that recieved a score of 100, meaning they had no violations, but they still poorly performed. This seemed high so I dug future into this data. Almost all of these establishments were either out of business or temporarily shutdown by the health department.  

The most common violations that resulted in a poor performance were Non-Food Contact Surfaces Clean, Improper Maintenance of Walls/Ceilings, Non-Food Contact Surfaces, Improper Maintenance of Floors, and Food Protection. All of these categories are non-critical violations, but all resulted in a failed inspection. About 1/3 of all violations were non-critical that resulted in a failed inspection. It's also important to note that these categories were related to the license category of Eating and Drinking Establishment (FS) and Eating and Drinking Establishment with Take-Out Service (FT). This finding aligns with the initial exploratory data analysis I conducted since the vast majority of establishments were FS and FT, as shown below:
* FT - 37.9% 
* FS - 48.4% 
* RF (Retail Food Establishment) - 12.5% 
* MFW (Mobile Food Truck or Vendor) - 1.3%

The percentage of poor performing establishments are shown below:
* FT - 38.6%
* FS - 46%
* RF - 13.7%
* MFW - 1.7%

I then decided to look into how many establishments were repeatedly performing poorly within the same year. To do this, I needed to find all establishments that failed the inital inspection for a given year.

2012: 1484 repeat reoffenders of 5409 total establishments, 2591 of which failed initial inspection

2013: 1260 repeat reoffenders of 4073 total establishments, 2546 of which failed initial inspection

2014: 1330 repeat reoffenders of 3885 total establishments, 2650 of which failed initial inspection

2015: 1554 repeat reoffenders of 3900 total establishments, 2734 of which failed initial inspection

2016: 1689 repeat reoffenders of 4085 total establishments, 2864 of which failed initial inspection

2017: 1409 repeat reoffenders of 4072 total establishments, 2704 of which failed initial inspection

2018: 667 repeat reoffenders of 3009 total establishments, 2221 of which failed initial inspection

![Graph](https://raw.githubusercontent.com/blamaral/EOTSS_Data_Challenge/master/graphs/number-of-repeat-offenders.png)

From the data and graph, it looks like as the years progress, there are less establishments overall, whereas the number of establishments that perform poorly roughly remains the same. However, the number of establishments that repeatedly perform poorly within the year decreases.

The following are frequency graphs to show this trend in more detail.

![Graph](https://raw.githubusercontent.com/blamaral/EOTSS_Data_Challenge/master/graphs/initially-poorly-performing-establishments.png) 

This indicates that the majority of establishments perform poorly on their first inspection as time progresses.

![Graph](https://raw.githubusercontent.com/blamaral/EOTSS_Data_Challenge/master/graphs/repeatly-poorly-performing-establishments.png)

This conveys that the majority of establishments are not repeatedly performing poorly.

![Graph](https://raw.githubusercontent.com/blamaral/EOTSS_Data_Challenge/master/graphs/poorly-performing-establishments.png)

This shows that in recent years more poorly performing establishments are passing reinspections moreso than in years prior.

The last thing I looked at were the license categories for establishments that repeatedly perform poorly on a per year basis.

![Graph](https://raw.githubusercontent.com/blamaral/EOTSS_Data_Challenge/master/graphs/most-common-food-license-cats.png)

I also have data visualizations on Tableau to support the findings above here: 

https://prod-useast-a.online.tableau.com/#/site/brianna/workbooks/118180?:origin=card_share_link