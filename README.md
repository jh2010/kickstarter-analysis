# Kickstarting with Excel

## Overview of Project

### Purpose
The purpose of this challenge is to help Luise understand how Kickstarter campaigns fared in relation to their launch dates and their funding goals.
---
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
From the excel workbook [Kickstarter_Challenge](https://github.com/jh2010/kickstarter-analysis/blob/master/Kickstarter_Challenge.xlsx), I created a new column named **Years**.  I then used the Excel function [YEAR()](https://support.microsoft.com/en-us/office/year-function-c64f017a-1354-490d-981f-578e8ec8d3b9) to extract the year from the **Date Created Conversion** column. Then, I created a pivot table that filters based on the **Parent Category** and the **Years**. After that I added the **outcomes** to the **Columns**. Next I added the **Date Created Conversion** to the **Rows** and added the **Count of outcomes** to the Values. I also adjusted the filter for the column labels to show **successful**, **failed**, and **canceled** After the pivot table was completed, I created a chart to visualize the Kickstarter theater outcomes based on launch date.

###### Outcomes Based on Launch Date Chart
![image_name](https://github.com/jh2010/kickstarter-analysis/blob/master/Outcomes%20Based%20on%20Launch%20Date.png)

### Analysis of Outcomes Based on Goals
From the excel workbook [Kickstarter_Challenge](https://github.com/jh2010/kickstarter-analysis/blob/master/Kickstarter_Challenge.xlsx), I created an Excel sheet named **Outcomes Based on Goals**. Then I created columns (Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed, Percentage Canceled) in the new sheet.

After that I added Goal ranges in from **Less than $1,000** to **Greater than $50,000**

Next I used the Excel function [COUNTFS()](https://support.microsoft.com/en-us/office/countifs-function-dda3dc6e-f74e-4aee-88bc-aa8c2a866842) to populate the **Number Successful**, **Number Failed** and **Number Canceled** columns.  First I added **outcomes** column "=COUNTIFS(**Kickstarter!F:F, "successful"**)", then I added the **goals** column (filtered by goal ranges) "=COUNTIFS(Kickstarter!F:F, "successful",**Kickstarter!D:D, "<1000"**)". Lastly I added the **subcategory** column "=COUNTIFS(Kickstarter!F:F, "successful",Kickstarter!D:D, "<1000", **Kickstarter!R:R, "plays"**)" and filtered by **plays**.

In the **Total Projects** I used the Excel function [SUM()](https://support.microsoft.com/en-us/office/sum-function-043e1c7d-7726-4e80-8f32-07b23e057f89) to add the **Number Successful**, **Number Failed** and **Number Canceled** columns together.

In the **Percentage Successful**, **Percentage Failed** and **Percentage Canceled** columns I used the [ROUND()](https://support.microsoft.com/en-us/office/round-function-c018c5d8-40fb-4053-90b1-b3e7f61a213c) to calculate the percentages of successful, failed and canceled projects.

After the excel sheet was completed, I created a chart to visualize the Kickstarter Outcomes vs Goals.

###### Outcomes vs Goals Chart
![image_name](https://github.com/jh2010/kickstarter-analysis/blob/master/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
I had slight difficulties creating the **Outcomes vs Goals** chart because it was challenging to format the percantages which I overcame it by researching the problem.

---

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Based on the analysis, it becomes obvious that in the month of May there were most 
successful outcomes for the theater based campaign in reaching their goal.
Another interesting conclusion is that the month of December shows least successful campaign.

- What can you conclude about the Outcomes based on Goals?
Successful campaigns happen when money collected fall between less than 1000 -9 999 and 35,000 to 45,000.
Based on the analysis, most of failed campaigns happen between 25,000-35,000 and between 45,000-  50,000> 

- What are some limitations of this dataset?
Some limitations for this dataset includes possible missing or inaccurate information from Kickstarter.

- What are some other possible tables and/or graphs that we could create?
To enhance this analysis, we can incorporate( include) another graph showing the number of backers and the average donation amount because they can give us another insight why campaigns might have been successful or failed.
