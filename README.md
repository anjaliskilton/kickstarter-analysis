# Kickstarting with Excel

## Overview of Project
**This project focused on the use of Pivot Tables and the COUNTIFS() function to categorize large sums of data.** All data for this project came from a pre-entered accounting sheet for fundraising campaigns specifying their id; name, blurb (project description), monetary goal (goal), money pledged (pledge), outcomes, country, currency, deadline and launch data(in duodecimals format), staff pick, number of backers  (backers count), category and subcategory, percentage funded, and average donation.

### Purpose
The first goal of this project was to create a chart and graph to demonstrate campaign outcomes based on launch date. The second goal of this project was to create a chart to demonstrate outcomes based on goals. 
![PivotTable_start](kickstarter-analysis/PivotTable_start.JPG)
## Analysis and Challenges
The first goal of the project is referred to as the Analysis of Outcomes Based on Launch Date and the second goal of the project is referred to as the Analysis of Outcomes Based on Goals. These goals will be discussed in the former order with PivotTables being the main focus of the first project and COUNTIFS() being the main focus of the second project.

### Analysis of Outcomes Based on Launch Date
Utilizing PivotTables one can create a sortable table and chart best on a selected excel sheet.
First the desired sheet was selected and highlighted (in this case it was our Kickstarter sheet). Then in the insert tab PivotChart was selected with the option PivotChart & PivotTable and placing the PivotTable in a new worksheet. 

A new sheet opened up with the PivotTable and options pop-up to the right hand of the screen called PivotTable Fields. In this area a list of column categories was shown at the top of the screen. Here the different categories were dragged and dropped into four sections filters, columns, rows, and values. It is important to note that values will create a count of whatever category is dragged and dropped into this section. 

The PivotTable was then filtered by theater in the parent category. Then by clicking the insert tab and the line graph icon (highlighted in red) a pop-up table with line graph options will appear. By selecting the option with points along the line graph, a graph with the data for the PivotTable appeared on the current sheet. 

This graph was then copy and pasted into paint and saved as a png. 

### Analysis of Outcomes Based on Goals
Creating an analysis of outcomes based on goal takes a slightly different approach than that of launch date. This called for a new sheet in the Excel workbook to be created titled Outcomes Based on Launch Date. In order to start the analysis 8 columns (shown in figure below) were added to the sheet.

In the goal column a set of numeric parameters were listed out to differentiate the certain type of goal. These rows were the basis for the rest of the analysis. 
In the following column (number successful) the COUNTIFS function was used to pull data within given parameters from our goals column from the Kickstarter worksheet. In the figure below you will see COUNTIFS, which tells Excel we want to use the COUNTIFS function. Then you will see Kickstarter!$D:$D, which denotes where we are pulling out information from (Kickstarter worksheet in column D). The <1000 tells Excel to count all values less than 1000 in the former specified column. Next, the Kickstarter!$F:$F,"Successful means the same as above except Excel is looking for the term Successful in column F of the Kickstarter worksheet. Thus, Excel is looking for all terms that say Successful in the Kickstarter worksheet in column F which correspond to a value under 1000 in the Kickstarter worksheet in column D.

A similar function is used for the mixed inequalities, except and extra term (in this case Kickstarter!$D:$D,"<=4999") is added to the end out the COUNTIFS function to set the exact range wanted. The same process and function was then applied to Number Successful, Number Failed, and Number Canceled rows. 
In the total project’s column, a simple sum function was used to add up all the successful, failed, and cancelled projects in the corresponding row. 

All percentages were also calculated by simple division and changing the cell type to a percentage. For instance, the number of successful was divided by total projects to give a decimal value, which then was converted into a percentage when cell type was changed from general to percentage. 

The derived percentages were then plotted in a line graph against the goal range to demonstrate the effectiveness of each range.


### Challenges and Difficulties Encountered
One of the biggest challenges with PivotTables is understanding what value goes where when creating a table is understanding what value goes where when creating a table (i.e. what value to put in the column, filter, or row section). The best practice to over come this is to write out the goal of the table and deduce what specific value is being targeted. Then it is easy to see exactly where each component goes. 

When it comes to COUNTIFS functions it can be challenging to track down exactly what column and sheet the data is being pulled from. To overcome this, the best practice is to write down in a word doc or a separate piece of paper where information is located so that it can be easily be inputted into the COUNTIFS sheet.
## Results
In conclusion it is found that the most successful theater campaigns are in May and the least successful are from May to July. It can also be seen that there is a large peak in success at the start of summer and a steady decline until fall with a sharp drop off at winter. This indicates that it would be best to start promoting these camping’s around start of spring to build anticipation for the more fruitful summer months.
It can also be seen that when a campaign has a lower goal it is much more likely to be successful. Thus, it would be advised to have more low goal campaigns throughout the summer in order to maintain success.
However, this data set focuses on theater and excludes other categories for the PivotTable, thus it is advised to create a PivotTable with all kick starters included to give a more accurate and holistic view of the data set. Another graph of goal versus pledge amount and pledge amount base on launch date would be beneficial to see when and what people are putting their money towards the most. 
