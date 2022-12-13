[![license](https://img.shields.io/github/license/DAVFoundation/captain-n3m0.svg?style=flat-square)](https://github.com/DAVFoundation/captain-n3m0/blob/master/LICENSE)
![contributors](https://img.shields.io/github/contributors/shubha8196/data-512-homework_1.svg) ![codesize](https://img.shields.io/github/languages/code-size/shubha8196/data-512-homework_1.svg)


# Impact Analysis of human mobility and government interventions effects on the spread of COVID-19
County Assigned: Jefferson County (Kentucky, US)


## Goal

The COVID-19 pandemic has greatly affected people’s lives, world economies, and the public health threat it represents is the most serious seen in a respiratory virus since the 1918 H1N1 influenza pandemic. In the absence of a vaccine or an effective treatment, the rapid spread of the disease elicited a wide range of responses from different governments across the globe to contain the spread of the pandemic. It is well known that the US government had also adopted several interventions apart from the mask mandate policy like travel restrictions, ban on large gatherings, stay-at-home orders, etc., to determine the set of restrictions that will effectively help remediate the spread of COVID-19 without excessively limiting the economic activity. However, these policies did have severe public repercussions. These non-traditional restrictions caused social belonging, quality of education, human needs of safety, and financial security to be threatened.  Hence, it's essential to understand which government policies which include pharmaceutical and non-pharmaceutical inventions, had a positive turnaround in containing the spread and were truly worth implementing. This analysis can help the policymakers get more insights on what measures can be quickly implemented/ adjusted in the future if a similar situation were to arise, so as to ensure that the general public is not subjected to restrictions that perhaps don't yield the intended results.

Human mobility also plays an important role in the dynamics of infectious disease spread. By analyzing social mobility data, one can evaluate if changing social mobility in outdoor or indoor settings along with masking policies influenced COVID-19 infection spread in real-time as well. One of the motivations for this exercise is to understand if tracking human mobility both inclusive and exclusive of periods where mask mandates policies were in effect, through publicly available data sources can be used as an effective measure in identifying patterns in the COVID-19 spread.

The Kentucky state government (like other state governments) has implemented several policies at different time periods to help reduce the spread. However, it can be possible that the population responds differently to government interventions and that these differences can cause different human mobility patterns which leads the epidemic development to change. Hence, human mobility is a good additional factor that can also be used to evaluate the effectiveness of pharmaceutical and non-pharmaceutical inventions when analyzing the spread of COVID-19.

The main motivation of this analysis is to truly understand the effects of government interventions and human mobility on the spread of COVID-19 and to identify how these interventions and human mobility, in general, had a significant impact in reducing the COVID-19 spread in Jefferson County, Kentucky, US.

## Research questions
Below are the set of Research questions and Hypothesis the study tries to answer. (All the questions listed before are pertaining to Jefferson County, KY)
1) How has mobility changed with the government restrictions and policies in place?
Hypothesis:
Null: The mean difference in the percentage change in mobility prior to and post-mask mandates is not different from 0.
Alternative: The mean difference in the percentage change in mobility prior to and post-mask mandates is different from 0.

2) Which of the different government responses/policies have influenced mobility the most?
Hypothesis: 
Mobility (of a particular type, say mobility to drug stores or pharmacies) reduced by X% post a varied combination of government policy implementation on the travel ban, masking regulations, and vaccination mandates

3) Which of the different government responses/policies have influenced the COVID-19 spread the most?
Hypothesis: 
COVID-19 cases reduced by X% post a varied combination of government policy implementation on the travel ban, masking regulations, and vaccination mandates

4) How have different mobility habits influenced the spread of the COVID-19 pandemic? Has reduction/increase in mobility had a significant impact on case reduction/increase?
Hypothesis: 
A time lag correlation between the different types of human mobility and the covid-19 cases, identifies the mobility contributions towards the spread.


## Data Utilized/ Input files

Data Source 1: [COVID-19 Data from John Hopkins University ](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv)

This dataset consists of the cumulative confirmed case counts were gathered from the Kaggle repository of the John Hopkins University; Raw United States confirmed COVID-19 cases dataset. 


Data Source 2: [U.S. State and Territorial Public Mask Mandate from April 10, 2020, through August 15, 2021, by County by Day](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) 

This dataset consists of the data for masking mandates was sourced from the CDC dataset of masking mandates by county. 
and  the mask-use-by-county.csv dataset is the New York Times [mask compliance survey](https://github.com/nytimes/covid-19-data/tree/master/mask-use) data.
 

Data Source 3: [COVID-19 Mobility dataset from Google](https://github.com/GoogleCloudPlatform/covid-19-open-data/blob/main/docs/tablemobility.Md)

The dataset shows how visits to places, such as grocery stores, public transport hubs, and parks, to name a few, have changed since Feb 2020 compared to a baseline. The baseline is the median value, for the corresponding day of the week, during the 5-week period Jan 3–Feb 6, 2020. 

Data Source 4: [Covid-19 Government Response dataset from the University of Oxford](https://github.com/GoogleCloudPlatform/covid-19-open-data/blob/main/docs/tablegovernment-response.md )

This dataset consists of the government's response to the pandemic through different policies like school closures, restrictions on travel/ internal movement, and workplace closures, to name a few, including a stringency index associated with each government response.



## Repository Distribution

```
data-512-project/
  |- README.md
  |- LICENSE
  |- data
    |- RAW_us_confirmed_cases.csv
    |- mask-use-by-county.csv
    |- U.S._State_and_Territorial_Public_Mask_Mandates_From_April_10__2020_through_August_15__2021_by_County_by_Day.zip
    |- US_KY_21111.zip
    |- oxford-government-response_ky.csv
  |- plots
    |- Common-Analysis-Visual.png
    |- mobility-cases-lag.png
    |- mulit-linear-reg-for-mobility.png
    |- var-model-summary.png
    |- multi-linear-reg-for-cases.png
  |- DATA 512- Project Report.pdf
  |- notebooks
    |- Part 1- Jupyter notebook.ipynb
    |- Part2- Extensive Analysis.ipynb

```

## Jupyter Notebooks

Part 1- Jupyter notebook.ipynb : Contains the code used for analysis and plotting of the visualization for common analysis

Part2- Extensive Analysis.ipynb: Contains the code used for analysis and plotting of the visualizations needed for the extensive analysis to access the impact Analysis of human mobility and government interventions effects on the spread of COVID-19


## Issues/ Special considerations
1) Moving average (over 7 days) of the daily cases counts data also incorporated in the analaysis and visualization approach to account for case counts not being updated for every single day in a week to help smooth out-trend information by creating a constantly updated average value in the visualization.
2) Apart from the CDC masking mandate data, Jefferson County's official website stating the masking policies have also been considered in the output visualization.
3) The COVID-19 Mobility dataset demonstrates how visits to sites like grocery shops and parks have altered (during the pandemic) from a pre-pandemic baseline value. The baseline is the median value on the relevant weekday from January 3 to February 6, 2020. As time passes and we move further away from the baseline period, Jefferson County populations might vary due to relocation or new regional and remote working options. Google’s understanding of categorized places might also have changed. For example, the same value today and in April 2020 might not indicate the same behavior or adherence; it might be that Google has updated information about shops and restaurants in the region or that fewer people live there now. These differences could shift the values up or down over long time periods. Here, I would like to highlight that this potential variation in the population over time which in turn affects the changes in the mobility change rates is not considered during my analysis due to a lack of information on new baselines at different periods during the pandemic.
4) Also note that the inclusion of Google data in the computation of mobility changes is dependent on user choices, connection and if it fulfills Google's privacy limits. As a result, when the data does not match Google's quality and privacy requirements, there may be empty entries for specific locations and dates. It's also worth noting that this data is based on users who have enabled Location History in their Google Accounts, thus it reflects a sample group of users from any given region. As with all samples, this may or may not accurately represent the behavior of a larger population. 


## Human-Centered Considerations

All of the methodological methods discussed below are human-centered in nature. To begin, the proposed study design is oriented toward individuals. It uses human mobility behaviors to make decisions, which are subsequently utilized to promote policy health care, and government mandates improvements for the public. It employs data created by individuals for people. It also employs a participatory design in which data from users' inquiries is blended into the created answer in real-time. This immediate, quick, and low-cost feedback will help in the proactive updating of policy suggestions based on people's activities. Certain ethical issues are also included in this analytical process. It is based on data from Jefferson County inhabitants and is free of any other demographic biases. To protect people's privacy, no personal information or particular search searches are used in the study. The approach and analysis developed are also replicable and can be used for any data set containing people's mobility patterns and COVID-19 region responses.


## Summarized Key Findings


For Common Analysis

A time series plot has been created to visualize the variations in the COVID-19 daily infection rate in Jefferson County (state of Kentucky) during and beyond the periods when mask mandate policies were established in Jefferson County. The mask mandate policies data w.r.t Jefferson County is also incorporated into this visual. The changepoints (represented by the red dotted lines in the graph) indicating the abrupt variations in the rate of infections i.e., timestamps where the change in inflected cases is significant from the confirmed cases dataset made available for Jefferson County are calculated using Pruned Exact Linear Time (PELT) Test as mentioned in methodology.

![Alt](./plots/Common-Analysis-Visual.png)

Through this visual, we can see that the masks were made mandatory from mid-June 2020 to mid-July 2021 (7/10/2020 to 6/10/2021) in Jefferson County. It is interesting to see that before and during the start of the mask mandate, we see that cases per day spread was kind of controlled and during the central period (Oct 2020 to Feb 2021) of the mask mandate the spread seems to move towards an uncontrolled trend. However, the same cannot be said during the end of the mask mandate. We see a controlled spread during the beginning of the end of the mask mandate period (i.e., from Mar 2021 to June 2021). If we were to consider the masking mandate to be the sole reason for the trend period, one can say the effects of removing the mask mandate can be observed in a little over the next 30 days’ time period (i.e., from Aug 2021) were the cases per day are starting to spread uncontrolled again. The voluntary masking survey shows us that 60.2% of the people in this county always wore masks and 91.5% of people wore masks more than sometimes (including sometimes survey points). This timeframe (July 2 - July 14) was when CDC had nationwide guidelines for wearing masks. So, technically our assumption is people in the county were following CDC guidelines religiously when there was a state mandate. Hence, these non-uniform variations in the case rates during different mask mandate periods lead me to infer that perhaps the mask mandates are not the only factor impacting the case rate variations. Additionally, moving away from the impact of mask mandates, we see that there is a huge uncontrolled spike in the case rates for Jefferson County at the beginning of the year 2022. One explanation for this can be the rise of the Omicron variant detection in several counties of the United States at the beginning of 2022.


For research question: 1) How has mobility changed with the government restrictions and policies in place?

Results from the dependent t-test
1) Mobility Type - Visits to retail and recreation point; test statistic=-5.87, pvalue=7.1e-08; Hypothesis action- Reject null hypothesis
2) Mobility Type - Visits to grocery and pharmacy; test statistic=1.72, pvalue=0.088; Hypothesis action-  Don’t reject null hypothesis
3) Mobility Type - Visits to transit stations; test statistic=-2.17, pvalue=0.032; Hypothesis action- Reject null hypothesis
4) Mobility Type - Visits to workplace; test statistic=-8.12, pvalue=2.2e-012; Hypothesis action- Reject null hypothesis
5) Mobility Type - Visits to residential areas; test statistic=10.49, pvalue=2.69e-17; Hypothesis action- Reject null hypothesis

From the above results, we see that the p-value is less than the significance level of 0.05 for all mobility types except for mobility corresponding to visits to grocery and pharmacies. This indicated that there is a significant difference in the percentage change in mobility of most types of post-introduction of mask mandates. To look at how different the mobility changes are when other government restrictions are in place we look to the results of the multi-linear regression model next.



For research question: 2) Which of the different government responses/policies have influenced mobility the most?

The multi-linear regression model has been fitted with the following variables data to analyze the impact of government policies on mobility.
Independent variables: 'mask_required',' facial_coverings ', school_closing’, workplace_closing ', 'cancel_public_restrictions_on_gatherings ’, 'public_transport’, ‘stay_at_home_requirements'

![Alt](./plots/mulit-linear-reg-for-mobility.png)

From the results of the model fitted for mobility type – visit to grocery and pharmacy we see that government restrictions (apart from mask mandates) like  stay at home requirements, canceling of public events and public transport close and restriction of gatherings have the most impact in reducing human mobility. For example, we see that when stay-at-home orders are in place, keeping all other variables constant, we see that there is an 8.8% decrease in mobility to grocery and pharmacy stores.

On fitting similar models to the rest of the mobility types we see that stay-at-home orders and the canceling of public events orders are the most common influential government restrictions for reducing the mobility of all types.


For research question: 3) Which of the different government responses/policies have influenced the COVID-19 spread the most?

To understand the impact of government policies on the spread of Covid-19 in Jefferson county we fit another multi-linear regression model with the following variables.
Independent variables: 'mask_required',' facial_coverings ', school_closing’, workplace_closing ', 'cancel_public_restrictions_on_gatherings ’, 'public_transport’, ‘stay_at_home_requirements
Response variable: daily cases count (moved 7-day averaged count)

![Alt](./plots/multi-linear-reg-for-cases.png)

The results of the fitted model indicate that most government restrictions have an impact on reducing daily case count. Predominantly, we see that when the stay-at-home restriction is mandated, holding all other variables constant we see a 6.2% reduction in daily case counts. Similarly, we see a 2.1% and 1.27% reduction in daily cases (holding all other variables constant) when the cancellation of public events and public transport closing mandates respectively are put in place. 

For research question: 4) How have different mobility habits influenced the spread of the COVID-19 pandemic? Has reduction/increase in mobility had a significant impact on case reduction/increase?

To access the mobility impact on the spread of COVID-19 in Jefferson County, we first plot the time series graphs of the percentage change in mobility (mobility of type- visits to grocery and pharmacy is displayed in the plot below) and change in daily case rate and their corresponding change points calculated through change point detection. The shaded red blocks in the graph show that there is a lag gap in the changes between mobility and the daily case rate. Note: Similar lags have been observed in other mobility types as well. Hence, we look to the results of the VAR model to infer how much of a lagged influence mobility change has on the COVID-19 spread.

![Alt](./plots/mobility-cases-lag.png)

Variables for the VAR models: percentage mobility change ( mobility of different types, such as visits to grocery and pharmacies, visits to retail and recreation stores, visits to workspaces, visits to residential areas, and visits to transit hubs)) and percent daily case rate change.

![Alt](./plots/var-model-summary.png)

The results of the fitted model indicate indicate that mobility to grocery and pharmacy places has a significant 7-day lagged impact on daily case rates. That is, reducing the mobility to grocery and pharmacy by 1% reduced the daily case rate by 4.5% after a duration of 7 days (holding all other variables constant)

We see similar results obtained when the VAR model is fitted with other types of mobility. For example, we see that mobility to transit stations also has a significant 7-day lagged impact on daily case rates. That is, reducing the mobility to transit stations by 1% reduced the daily case rate by 0.84% after a duration of 7 days (holding all other variables constant). Mobility to retail and recreation spots has a significant 10-day lagged impact on daily case rates. That is, reducing the mobility to retail and recreation spots by 1% reduced the daily case rate by 0.59% after a duration of 7 days (holding all other variables constant). Overall we see an average lag impact of 8.5 days on the case rates when all types of mobility are considered.



## Author
- [Shubha Changappa Palachanda](https://github.com/shubha8196)
