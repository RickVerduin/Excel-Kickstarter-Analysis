# Excel-Kickstarter-Analysis

## Overview
This analysis looks at Kickstarter fundraising data to provide playwrights with insights on the performance of previous fundraising capaigns. Using data for projects between 2009 and 2017, charts have been created compare the outcomes of campaigns to their respective fundraising goals and the date the campaign was launched.

Outcomes fall into one of three categories:
- Successful - The campaign reached its fundraising goals
- Failed - The campaign did not reach its fundraising goals
- Canceled - The fundraising campaign was stopped before the due date

## Analysis and Challenges
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
