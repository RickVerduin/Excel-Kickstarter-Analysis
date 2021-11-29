# Kickstarting with Excel

## Overview of Project
Up-and-coming playwright Louise is planning to launch a fundraising campaign to fund the production of a play she wrote. To provide her with useful information, data for similar projects between 2009 and 2017 has been analyzed, and charts have been created to compare the outcomes of campaigns to their respective fundraising goals and the date the campaign was launched. Based on this analysis, conclusions about general trends will be given.

### Purpose
The purpose of this analysis is to provide Louise with insights on the performance of past Kickstarter fundraising campaigns within the Theater category. The analysis focuses on the relationship between fundraiser success and the date the fundraising campaign was launched, as well as the relationship between fundraiser success and the fundraising goal in US dollars.

## Analysis and Challenges
Outcomes of fundraising campaigns fall into one of three categories:
- Successful - The campaign reached its fundraising goals
- Failed - The campaign did not reach its fundraising goals
- Canceled - The fundraising campaign was stopped before the due date

In order to look at outcomes based on the date the campaign was launched, the following steps were taken.
- To only account for campaigns in the "Theater" category, data in the "Category and Subcategory" column was converted into two columns: "Parent Category" and "Subcategory".
- Data in the "Date Created" column was converted from Unix timestamps to Human dates, and a new column was added with the Date Created Conversion.
- A pivot table was created with Outcomes in columns, and Date Created Conversion in rows, with Count of Outcomes as the value. A filter was added to filter by Parent Category, and the Parent Category Theater was selected.
- A line chart was created using the pivot table.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/93882635/143691445-691d3807-af12-4124-9ac1-bd41687b8898.png)

In order to look at outcomes based on the fundraising goals, the following steps were taken:
- Dollar amounts for fundraising goals were divided into 12 categories: Less than 1000, 1000-4999, 5000-9999, 10000-14999, 15000-19999, 20000-24999, 25000-29999, 30000-34999, 35000-39999, 40000-44999, 45000-49999, Greater than 50000.
- A new sheet was created to calculate the percentage of Successful, Failed, and Canceled fundraisers within each of the Goal brackets.
- A line chart was created.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/93882635/143691501-7a4d21a1-038f-41a9-a920-5fe98f0fca5e.png)


## Results
1. Looking at outcomes by launch date, the months May and June have not only the highest number of campaigns launched, but also the highest success rate at respectively 67% and 65%. The data suggests that launching a fundraising campaign in either May or June may lead to an increased chance of meeting the fundraising goal.
2. Our data shows that the months August, October, December and January all have a below average success rate, and should be avoided as months to launch a fundraising campaign.
3. Our data shows a general tendency for the success rate to decline when the fundraising dollar goal increases. The chance of a campaign reaching its fundraising goal drops to less than 50% for dollar amounts over $20,000. To ensure that the campaign will be successful, the fundraising goal should be no bigger than strictly necessary.

### Limitations
The dataset used for this analysis is limited to Kickstarter data between 2009 and 2017 and therefore does not take the most recent trends into consideration.
Only the launch date and fundraising amount have been analyzed to provide insights into the chances for a campaign to be successful. Other factors, such as the topic of the play at hand, or the social-economical environment are ignored.

### Options for further analysis
The data sheet contains a colum titled "Spotlight"  that has been ignored during this analysis. It would be interesting to see whether spotlight fundraisers have a larger success rate.
The duration of the campaign can be included as a factor to see if campaigns that run for longer periods of time are more successful than shorter campaigns. This information can then be cross-referenced with both the Launch date of campaigns and the fundraising goal, to provide additional insights.
