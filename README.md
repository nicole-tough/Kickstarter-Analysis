# kickstarter-analysis
Performing analysis on kickstarter to uncover trends

# Kickstarting with Excel

## Overview of Project
In this project, I analyzed data from Kickstarter campaigns to help Louise launch a successful campaign for her play. To best achieve this goal, I analyzed how Kickstarter campaings similar to Louise's reached their Outcomes based on their Luanch Date and Goal. 
All of my analysis was completed in Excel using tables, pivot charts, and line charts. The result of this analysis showed that to have the best chance at success, Louise should launch her Kickstarter campaign in May or June and with a fundraising goal of less than $4000. 

### Purpose
This project is intended to help Louise find relevant information to get funding for her play. In this analysis, we will see how different Kickstarter campaigns fared in relation to their launch date and their funding goal. 

## Analysis and Challenges
To analyze Kickstarter campaigns similar to Louise's, I used Excel to create tables and charts to see the impacts of Kickstarters launch dates and their goals. 

### Analysis of Outcomes Based on Launch Date
To analyze the outcomes based on launch date, I first created a new table in the workbook to separate the 'year' from the launch dates. Once this was complete, I was able to create a new pivot table based on our Kickstarter data set. I set up my pivot table by filtering for year and parent category. To fulfill the purpose of the analysis, I put the launch date in the rows and the outcomes in the columns of the pivot table. Then, I filtered the outcomes column to show only successful, failed, or canceled outcomes. Because Louise is starting a play, I wanted to compare her Kickstarter to similar campaigns, so I filtered the Parent Category to theater. Finally, to better understand the relationship between the launch date and outcome, I created a line chart from this data, placing the outcome counts on the y-axis and the months of the luanch dates on the x-axis.
 
### Analysis of Outcomes Based on Goals
To analyze the outcomes of Kickstarters based on their goals, I first created a new workbook to pull the goals and outcome counts from the Kickstarter data. I first set up my Goal column to include the following dollar ranges:
![This is an image](C:\Users\NicoleTough\Desktop\DOBC\Crowdfunding Analysis\Resources)
I then used the *COUNTIFS* function to pull the "Number Successful," "Number Failed," and "Number cancelled" from our data set with the conditions of the goal ranges and "plays" from the subcategory range. I then used the *SUM* function to get the totals for each row and found percentages of successful, failed, or cancelled plays for each goal range. Ultimately, the table looked like this:
![This is an image](C:\Users\NicoleTough\Desktop\DOBC\Crowdfunding Analysis\Resources)
Once the table was complete, I created a line chart from the data to better understand the relationship between Kickstarter's outcomes and their goals.

### Challenges and Difficulties Encountered
One challenge I encountered was pulling the goal amounts using the *COUNTIFS* function. I was able to easily pull the data for the goals that were <1000 using this function: '=COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"successful",Kickstarter!$R:$R,"plays")'
At first, I was attempting to create upper and lower bounds by creating a range '=COUNTIFS(Kickstarter!$D:$D,"1000><4999")' but that was incorrect. 
I overcame this challenge by creating separate conditionals for the upper and lower boundaries of the range. Once this was complete, my function looked like this: '=COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<=4999",Kickstarter!$F:$F,"successful",Kickstarter!$R:$R,"plays")'

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
From our line graph, you can see the following two conclusions based on Kickstarter's Launch Date:
- Kickstarters for plays were more successful when they were launched in May and June.
- Kickstarters for plays launched in December were nearly as equally likely to succeed or fail. 
- What can you conclude about the Outcomes based on Goals?
Based on our line graph comparing the outcomes of plays based on their Goals, you can see that campaigns with a goal over $4000 is more likely to fail. 
- What are some limitations of this dataset?
One limitation on this dataset is that it does not include if campaigns were created in more urban or rural areas. Kickstarter campaigns for plays may be more likely to succeed in urban areas due to a higher population or higher interest.
The dataset also does not include methods that different campaigns used to fundraise. Some campaigns may have been more or less successful based on their fundraising strategies. 
- What are some other possible tables and/or graphs that we could create?
We could also create a box plot of the goals vs. outcome to see if there are any outliers that are skewing the data. 
Another line chart could also be created to track the timeline of successful campaigns to see how long it took them to achieve their fundraising goal. 
