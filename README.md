# Unit 18 Homework: Citi Bike Analytics

## Sheet Descriptions

**Data Source, ETL** - The information used in this project comes from [202206-citbike-tripdata.csv](/202206-citbike-tripdata.csv), representing the month of July in 2022. The csv was loaded into a Jupyter notebook ([citi_bike_etl.ipynb](/citi_bike_etl.ipynb)) in order to clean and group certain data points, especially in reference to statistics by station.

A sample of 10,000 rides was selected from the csv at random (using df.sample()) to make charting more manageable. The original file contains over a million rides, so a factor of at least 100 can be used.

**Population Density Map** - A png is provided with a population density heatmap as a reference to compare areas with bike rental stations. Please refer to [NYPopDensity.png](/NYPopDensity.png)
Going by the population density chart, we see the highest densities are around central park, North Manhattan, and on South Manhattan (before peninsula going to Brooklyn). 


**Member v Casual Map** - Starting off, this is a simple map to geoplot each trip from our sample and color the markers depending on whether the user was a member or casual user. 

It appears members are more likely to use bikes in North Manhattan, and the areas in across the river in Brooklyn. Casual users seem to generally be in the center of South Manhattan.

One possible explanation for this is that tourists are more likely to be the casuals and are more likely to be located in the heart of lower (South) Manhattan. The areas with heavy member rides look to be the more 'suburban' areas, such as Brooklyn and Astoria across the river, or Harlem in Upper Manhattan.

**Bike Type Treemap** - This Treemap is a useful snapshot to get a general sense for how "busy" each station is, along with the type of bikes used at each station. We can also get a sense of the distribition of "busy-ness" across all stations. At a glance, about 1/3 of all stations had over 20 rides (out of our sample, 20 x 100 would be a more accurate stat by month), and about a third are below 5 (x100) rides per month.

**Routes Detailed, filtered** - What would a Citi Bike presentation be without routes!? After consolidating the coordinates into start and end origins using Panda, we are able to chart routes. Only a few stations can be represented simultaneously and still be visible, so a filter is in place to only show a select few stations' routes.

Everything about mapping the routes looks to make sense. There are many short trips taken in high density areas, and longer trips that go from lower to higher density areas, resembling commutes. They are also highly popular everywhere around park areas such as Central Park.

**Total Miles per Station** - This orients stations and their "busy-ness" on a map. The largest clusters are naturally around lower Manhattan, with a noticeably higher density on the left coastline along the Hudson River. Looking at a google map view of NYC I see the presence of many piers and parks along the Hudson. I'm surprised we don't see larger clusters along the Eastern coastline given the size of East River Park. Several factors may be playing a role here, such as local ordinances.

**Mean Distance by Station** - A necessary follow-up to the previous map, this one differs in that the cluster size is based on the average distance biked by station. This seems to be pretty consistent across the board, with station averages ranging from less than 1 mile to 6+ miles. Lower Manhattan has mostly small clusters indicating short trips. Larger clusters are present cross the East River and North of Upper Manhattan, the likely starting location for people who commute to work towards Lower Manhattan.

**Rides per Station Bar Chart** - A good old fashion bar chart to visualize station ride counts. It is useful to see the spread of bike rentals across all stations, ranging from 1 to 40+ (x100).

**Bike Type Count + Average Distance** - This bar chart demonstrates bike types by number. It was interesting to note that about 1/4 of all bikes rented are electric, which makes sense as electric bikes have been rapidly soaring in popularity. The markers are also colored based on the distances traveled, revealing that average distance per electric bike (1.4mi) was more than for classic bikes (1.1mi), which absolutely makes sense.





## Before You Begin

* Save this assignment to your Tableau Public account rather than GitHub. 

* If you haven't already, make sure to create a Tableau Public [account] (https://public.tableau.com/s/).

* The free tier of Tableau only lets you save to their public server. So, each time you save your file, it will be uploaded to your Tableau Public profile. 

* You can load and continue working on the same workbook.

* When you finish your assignment, you will submit the URL to your Tableau Public workbook along with any additional files used in your analysis. 

## Background

![Citi-Bikes](Images/citi-bike-station-bikes.jpg)

Congratulations on your new job! As the new lead analyst for the [New York Citi Bike](https://en.wikipedia.org/wiki/Citi_Bike) Program, you are now responsible for overseeing the largest bike-sharing program in the United States. In your new role, you will be expected to generate regular reports for city officials looking to publicize and improve the city program.

Since 2013, the Citi Bike Program has implemented a robust infrastructure for collecting data on the program's utilization. Each month, bike data is collected, organized, and made public on the [Citi Bike Data](https://www.citibikenyc.com/system-data) webpage.

However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have questions about the program, so your first task on the job is to build a set of data reports to provide the answers.

## Instructions

Your task in this assignment is to aggregate the data found in the Citi Bike Trip History Logs and find two unexpected phenomena.

1. Design 2–5 visualizations for each discovered phenomenon (4–10 total). You may work with a timespan of your choosing. Optionally, you can also merge multiple datasets from different periods.

The following are questions you may wish to answer. Do not limit yourself to these questions; they are suggestions for a starting point. Be creative!

* How many trips have been recorded in total during the chosen period?

* By what percentage has total ridership grown?

* How have the proportions of short-term customers and annual subscribers changed?

* What are the peak hours when bikes are used during the summer months?

* What are the peak hours when bikes are used during the winter months?

* Today, what are the top 10 stations in the city for starting a journey? Based on data, why do you hypothesize these are the top locations?

* Today, what are the top 10 stations in the city for ending a journey? Based on data, why?

* Today, what are the bottom 10 stations in the city for starting a journey? Based on data, why?

* Today, what are the bottom 10 stations in the city for ending a journey? Based on data, why?

* How does the average trip duration change by age?

* What is the average distance in miles for a bike trip?

* Which bikes (by ID) are most likely due for repair or inspection in the timespan?

* How variable is the utilization by bike ID?

2. Use your visualizations (not necessarily all of them) to design a dashboard for each phenomenon. The dashboards should be accompanied by an analysis explaining why the phenomenon may be occurring. 

3. Create one of the following visualizations for city officials:

* **Basic:** A static map that plots all bike stations with a visual indication of the most popular locations to start and end a journey, with zip code data overlaid on top.

* **Advanced:** A dynamic map that shows how each station's popularity changes over time (by month and year). Again, with zip code data overlaid on the map.

* The map you choose should also be accompanied by a write-up describing any trends that were noticed during your analysis.

4. Create your final presentation.

    * Create a Tableau story that brings together the visualizations, requested maps, and dashboards.

    * Ensure your presentation is professional, logical, and visually appealing. 

## Considerations

Remember, the people reading your analysis will NOT be data analysts. Your audience will be city officials, public administrators, and heads of New York City municipal departments. Your data and analysis need to be presented in a way that is focused, concise, easy to understand, and visually compelling. Your visualizations should be colorful enough to be included in press releases, and your analysis should be thoughtful enough to inform programmatic changes. 

## Submission 

Your final submission should include:

* A link to your Tableau Public workbook that includes the following:
  * 4–10 total "phenomenon" visualizations 
  * 2 dashboards
  * 1 city official map
  * 1 story 
  * A text or markdown file with your analysis of the phenomena you uncovered in the data.

## Sharing Your Work

To share your work, we are asking that you save your workbook as a `.twb`x file so your TAs can grade them.

To save your workbook as a .twbx file, select "Save As..." from the "File" drop-down. Then, select the .twbx option.

## Assessment

Your final product will be assessed on the following metrics:

* Analytic Rigor

* Readability

* Visual Appeal


## Hints

* You may need to get creative with how you combine each of the CSV files. Don't just assume Tableau is the right tool for the job. At this point, you have a wealth of technical skills and research abilities. Dig for an approach that works, and go with it.

* Don't assume that the CSV format hasn't changed since 2013. Subtle changes to the formats in any of your columns can interfere with your analysis. Ensure that your data is consistent and clean throughout your analysis. (Hint: Start and End Time change at some point in the history logs).

* Consider building your visualizations with small extracts of the data (like single files) before attempting to import the whole thing. What you will find is that importing all 20+ million records of data will create performance issues quickly. Welcome to "Big Data."

* While utilizing all of the data may seem like a nice power play, consider the time course in making your analysis. Is data from 2013 the most relevant for making bike replacement decisions today? Probably not. Don't let overwhelming data fool you. Ground your analysis in common sense.

* Remember, data alone doesn't answer anything. You will need to accompany your data visualizations with clear and directed answers and analysis.

* As is often the case, your clients are asking for a LOT of answers. Be considerate about their “need to know” and the importance of not "cramming in everything.” Of course, answer each question, but do so in a way that is organized and presentable.

* Since this is a project for the city, spend the appropriate time thinking through decisions on color schemes, fonts, and visual storytelling. The Citi Bike program has a clear visual style. As a suggestion, look for ways to have your data visualizations match their aesthetic.

* Pay attention to labels. What exactly is "time duration?” What's the value of "age of birth?” You will almost certainly need calculated fields to get what you need.

* Look for obvious outliers or false data. Not everyone who signs up for the program is answering honestly.

* In answering the question of "why" a phenomenon is occurring, consider adding other pieces of information, like socioeconomic or geographic data. Tableau has a map "layer" feature that you may find helpful.

* Don't be afraid to manipulate your data and play with settings in Tableau. Tableau is meant to be explored. We haven't covered everything that you’ll need &mdash; so keep an eye out for new tricks!

* Treat this as a serious endeavor! This is an opportunity to show future employers that you have what it takes to be a top-notch analyst. 


## Rubric

[Unit 18 Homework Rubric](https://docs.google.com/document/d/11hlhJnKmEJgRYL3mUxRcdrz4AIxBU5PXW5fYrRYvgW8/edit?usp=sharing)

- - -

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.

