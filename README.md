# MIST 4610 Group Project 2

## Group Three Members
##### Nabeel Sadiq [NabeelSadiq](https://www.github.com/Nabeel470)
##### Joshua Libatique [JoshuaLibatique](https://www.github.com/jiyuukane)
##### Anthony Lopez [AnthonyLopez](https://www.github.com/asl58391)
##### Ethan Payne [EthanPayne](https://github.com/EthanPayne27)
##### Claire Stockman [ClaireStockman](https://www.github.com/clairestockman)

## Dataset Description 
Our dataset was found from the [data.gov](catalog.data.gov/dataset/infectious-diseases-by-disease-county-year-and-sex-6e856) catalog, and it analyzed infectious diseases by disease, country, year, and sex, while also providing populations for each country. The data provided one data point for each disaese in every county and year from the years of 2000 - 2020, giving us accurate and comprehensive information.

Our first question displayed a map of California, with each county ranging from a gradient of blue to red, with blue signifying a decrease in disease rate and red highlighting an increase. To achieve this map, we added the counties to details and selecting mapped, and added sun of overall % change to colors. The columns and rows were longitude and latitude respectfully, creating a gradient map of the state of California. 

We also wanted to highlight which conuties saw the greatest and lowest change in disease cases over time in hopes of discovering any similarities. To do so, our column was the sum of overall % change, while the rows were county. Afterwards, we filtered by the top and bottom five for overall % change, and created two horizantal bar charts; one for the top and one for the bottom five.

For our second question, we created a scatter plot of the rate of change for population and disease rate over the years 2000 - 2020. We had to use python in order to calculate the slope, as our version of tableau was unable to. After importing the new table created with python, we had the slope for population as our column, with the slope for diseease rate as our row. Afterwards, with a new table called urban classifcation created in excel, we used the classification to color code the data points, and created a trned line for each classification. After all the steps above, we had a scatter plot highlighting the population vs the disease rates, creating an outlook into how population growth can affect disease rate. 

## Question One: Which counties have experienced the greatest change? 
Analyzing which counties in California have experienced the greatest change in infectious disease rates is important because it allows us to explore how various factors can influence public health trends in disease transmission. From city and transportation infrastructure to location to population density, the top counties in California with the greatest increases and decreases in disease cases can reveal how each factor and other possible variables played a role in the disease rate changes observed in our dataset. This question focusing on counties is also directly relevant to the dataset we are using because it enables us to manipulate and analyze infectious disease data reflected across the entire state of California. By including every California county in the scope of our dataset in the context of this question, we can confidently assess which areas of the state experienced the greatest growth or decline in disease cases. The resulting data from this analysis can then support theories and explanations behind what characteristics of counties drive disease rate changes as well as the key differences between areas experiencing increases and decreases.

## Question Two: How Case and Population Growth Differed Across Urban, Suburban, and Rural Counties? 
The second question we sought to answer was “How do case and population growth differ across urban, suburban, and rural counties?”.  There are several reasons why this question is interesting and important. These reasons include social, economic, and cultural. Socially, finding the differences in population growth and case growth can reveal disparities in healthcare access, living conditions, and the infrastructure of public health in differently populated areas. Economically, finding an increase or decrease in cases within a county can affect labor markets, housing markets, and the allocation of resources, specifically pharmaceuticals. Culturally, the analysis of this data may highlight the response hygienically to a global pandemic, even though the pandemic was caused by a virus. All of these realizations could aid policymakers, urban planners, and healthcare leaders to intervene more efficiently. On the other hand, these same leaders would have more data to support the investment into various developments within the state of California. This question is tied to the dataset because of its emphasis on the correlation between population and infectious diseases, which are both prominently recorded in the dataset.

## Data Manipulations for Question 1
### Map of California Counties
###### ![image](https://github.com/user-attachments/assets/2297f705-17e0-40cd-90b3-7b4bd7163841)
![image](https://github.com/user-attachments/assets/94f08893-c1dc-48c2-82d8-69d82dfd1257)
![image](https://github.com/user-attachments/assets/688e6641-e531-42d6-9e1e-41c9bab7cd6a)

Filtered Sex to "Total" (to avoid gender splits).

Created a calculated field:
➔ Overall % Change

Compared latest year cases vs earliest year cases using FIXED [County].

Formula used ABS() to stabilize the denominator.

Fixed mapping issues by creating a calculated field:
➔ County (Mapped) = [County] + " County"

Plotted using Latitude (generated) and Longitude (generated).

Colored counties by SUM(Overall % Change):

Red = case increases

Blue = case decreases

Excluded invalid or ambiguous rows (like “California” row if present).

Since the dataset didn’t include 'County' at the end of the county names, we created a calculated field called 'County (Mapped)' to format the names correctly so Tableau could match them to real map locations

### Top 5 and Bottom 5 Counties (Bar Charts)
![image](https://github.com/user-attachments/assets/0f2ae972-8f12-4d56-adca-b8109f6d3d14)
![image](https://github.com/user-attachments/assets/087fe553-1eb5-4b58-a53f-4cf494d448cf)![image](https://github.com/user-attachments/assets/dbba78af-2003-4eef-8074-f49925bd6681)


Filtered to Top 5 & Bottom 5 Counties which saw the greatest changes in disease cases over time:

Sorted by highest Overall % Change for Top 5 and lowest Overall % Change for Bottom 5

Built two separate horizontal bar charts

One for Top 5 Greatest Increase

One for Bottom 5 Greatest Decrease

County on Rows and SUM(Overall % Change) on Columns

Colored bars with a gradient to emphasize magnitude of change

## Data Manipulations for Question 2
### Used Google Colab (Python) to calculate slopes for infectious disease rates and population rates from 2000-2020
Preview code [here](https://github.com/asl58391/MIST4610GroupProject2/blob/main/SlopeCalc.ipynb)

### Used Excel to Create Urban Classifications Table to Color Code by Rural, Urban, and Suburban
#### Urban Counties were those above a population of 750,000, Suburban Counties were those between 100,000 and 750,000, and Rural Counties were those below 100,000
Preview csv file [here](https://github.com/asl58391/MIST4610GroupProject2/blob/main/Slope%20Classification.csv)

### Filters, Marks, Columns, and Rows
#### Filtered out a single null value, and excluded California's information as it was in the dataset.
![image](https://github.com/asl58391/MIST4610GroupProject2/blob/main/Filters%20and%20Marks.png)
![image](https://github.com/asl58391/MIST4610GroupProject2/blob/main/Columns%20and%20Rows.png)




## Analysis and Results for Question One 
![image](https://github.com/user-attachments/assets/6f9d3322-66d5-4ac1-b2dd-52ad5bcf6793)
![image](https://github.com/user-attachments/assets/cd8cdff6-a7cd-466a-9f89-64d9c4642001)
![image](https://github.com/user-attachments/assets/fdb9d329-c774-4a1c-8e17-7f2bb3499802)
Across California, counties with the greatest increases in disease cases are often urban or highly connected areas. For example, Modoc County had the largest percent increase, even though it is rural and sparsely populated, showing that small communities can still experience sharp changes. The other counties in the top five, like Lake, Marin, Imperial, and Santa Cruz, are primarily urban or suburban, where larger populations and closer contact likely contributed to faster spread. On the other hand, the bottom five counties, including Sierra and Plumas, are smaller, rural areas where decreases were more common. Sierra County, notably, is one of the least populated counties in the state and showed the greatest overall decline.

Several factors help explain these patterns. In general, higher population density leads to faster disease transmission simply because people are in closer contact. Transportation networks like highways and airports can further accelerate exposure and movement of infections, especially in major hubs. Meanwhile, rural counties with fewer residents, greater physical distance between people, and difficult-to-travel terrain — similar to regions near the Rocky Mountains — tend to have lower exposure rates and slower spread over time. These differences highlight how location, density, and infrastructure all play important roles in public health trends.





## Analysis and Results for Question Two 
![image](https://github.com/asl58391/MIST4610GroupProject2/blob/main/table%2Blegend.png)
Analysis: 
- After looking at the scatterplot and trend lines it was apparent that urban counties (the blue points and trendline) show the highest case growth relative to population growth.
- The rural counties (red points and line) had moderate case growth relative to population growth.The case growth increased more with population growth thatn suburban counties, but less than urban ones.
- Suburban counties (purple line and points) had the lowest case growth relative to population growth. They hade an even smaller increase in case numbers when population growth was higher. 

Potential Explanation:
- The congestion of urban infrastructure will significantly increase the flow of infectious disease cases and population. 
- Suburban density seems to allow a controlled growth environment for population while controlling the flow of diseases.
- Rural areas tend to show more data variance due to smaller populations and a higher sensitivity to localized outbreaks. 

### Tableau Worksheets
[Question One](https://github.com/asl58391/MIST4610GroupProject2/blob/main/4610_TableauProj.twb)

[Question Two](https://github.com/asl58391/MIST4610GroupProject2/blob/main/Project2.twbx)



