# Kickstarting with Excel

## Overview of Project

The purpose of our analysis was to look at aggregated fundraising data across a multitude of countries and entertainment categories. We utilize various features of excel (such as filtering, pivot tables and charts), in order to present the data in a way that makes pertinant trends easier to identify. 

### Purpose

Our purpose is to help a client, Louise, with a fundraising campaign for her play, Fever. In order to help Louise, we will use excel to better understand a large set of data with information regarding various entertainment kickstarter funding campaigns. We will perform various analyses and visualizations of the data so Louis can determine an informed strategy for her fundraising campaign.

## Analysis and Challenges

To begin our analysis for Louise, we started by getting to know the data by looking at basic information, such as: how many data points there are, what types of data are there, what kind of categories and the overall format of the data. We then took the step of converting data into different formats when needed, for example, by converting the timestamp into a date that would make sense to the average person (Fig 1). We also made some changes to the data so it was better presented, for instance we split apart the parent and subcategory column into two columns. We worked on making sense of the data by applying visual ques to the cells, such as shading a cell based on the magnitude of its value. This proved to be insightful as it exposed the fact that there are some serious outlieres in the set (Fig1).

![alt text](https://github.com/aamotz001/Kickstarter-Analysis/blob/main/Fig1.png)
**Figure 1: Time-stamp converted column and shading by percentage funded.**  

We then decided to help Louise set up her incentives by looking at the average donation amount. This involved averaging and looking at rounded data as percentage funded, and using error control to keep the results sane (for example setting values equal to zero when there was a zero in the denominator of the average). Using pivot tables to summarize data, and produce plots from that. Using search and filters to simplify data sets. Using vlookup to hone in on a specific subset. Looking at success versus type of input. Analyzed some measures of central tendancies.


### Analysis of Outcomes Based on Launch Date

One particulary important analysis which was performed, involves looking at the outcomes of various theater kickstarters by the time of year in which the campaign was launched. To do this, a pivot table was constructed using a filter over the parent category (so that the theater category could be considered on its own). The pivot table summarized data based on the total number of plays launched during a particular month (summing over all years) and looked at the three outcomes (successful, failed or canceled). Below are images showing the pivot table (Fig 2) as well as the chart produced from the pivot table (Fig 3). 

https://github.com/aamotz001/Kickstarter-Analysis/blob/main/Fig2.png
**Figure 2: Pivot Table.**

https://github.com/aamotz001/Kickstarter-Analysis/blob/main/Theater_Outcomes_VS_Launch.png
**Figure 3: Theater Outcomes VS Launch date.**

### Analysis of Outcomes Based on Goals

Another important analysis performed was based upon looking at the outcome of campaigns based on the goal amount. In order to do so, we had to use a special function, COUNTIFS, that would count the number of data points which mactched a particular criterion. This was an important thing to learn as it allows us to parse down large amounts of data into categories that we define. In this case, we were interested in seeing how the magnitude of the goal affected the success. Based on the results we gleamed using the COUNTIFS function, a line chart was produced as shown below (Fig 4).

https://github.com/aamotz001/Kickstarter-Analysis/blob/main/Outcomes_VS_Goals.png
**Figure 4: Outcomes VS Goals.** 

### Challenges and Difficulties Encountered

Challenges during this analysis involved understanding how the interplay between various filters worked. At first, I was not sure how "stacking," multiple filters worked. I thought that by selecting a filter, it automatically removed any other filters but now I know this is not the case. The biggest concepual challenge was understanding how to create the pivot tables, specifically, choosing the best options for the row, column and value sections of the table in order to present the data in a way that is natural and sensical. The way that this challenge was overcome was simply by brute force - I had to mess around with several pivot tables in order to develop an intuition about how to summarize large sets of data in a way that becomes easy to understand and present 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

Two conclusions to be drawn from the Outcomes VS Launch date chart are that (a) the number of succcsessful campaigns significantly increases at the beginning of summer (May). It should be considered that the largest amount of campain donations comes from the united states (Fig 5), so it may be because the end of the school year in the US coincides with May, and is far away from holiday spending. 

https://github.com/aamotz001/Kickstarter-Analysis/blob/main/Total%20Funding%20by%20Country.png
**Figure 5: Total donation by country.

Another conclusion is that the number of failed and canceled campaigns are relatively constant throughout the year - meaning that a high-risk vs low-risk campaign can take place any time of the year.

- What can you conclude about the Outcomes based on Goals?

The obvious conclusion from the outcomes based on goals is that it is significanctly better strategy to set lower donation goals ... but another thing to notice is that after a larger amount (about $15k) the percentage failed vs successful rates are about equal. So if larger goals are asked for, there is likely a 50/50 shot of being successful. 

- What are some limitations of this dataset?

One big limitation is that.... it's big. There are several erronious data points and it is so vast in terms of each parameter.  For example having a large number of countries my wash away important regional trends, or . Another limitation is that there is a bit of redundancy in the types of information that are being represented. 

- What are some other possible tables and/or graphs that we could create?

Some other types of pivot tables could include looking at the length of the campain (by subtracting the launch date from the date it was ended) and looking at how the amount of time affects the average donation by and success/failure/cancelled status. Another plot may be bar chart showing the total donation by category, and the success/failure/cancelled status by category as well. 
