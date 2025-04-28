# MIST 4610 Group Project 2

## Group Members
##### Nabeel Sadiq [NabeelSadiq](https://www.github.com/Nabeel470)
##### Joshua Libatique [JoshuaLibatique](https://www.github.com/jiyuukane)
##### Anthony Lopez [AnthonyLopez](https://www.github.com/asl58391)
##### Ethan Payne [EthanPayne](https://github.com/EthanPayne27)
##### Claire Stockman [ClaireStockman](https://www.github.com/clairestockman)

## Dataset Description (Tony)

## Question One: Which counties have experienced the greatest change? (Joshua)
Analyzing which counties in California have experienced the greatest change in infectious disease rates is important because it allows us to explore how various factors can influence public health trends in disease transmission. From city and transportation infrastructure to location to population density, the top counties in California with the greatest increases and decreases in disease cases can reveal how each factor and other possible variables played a role in the disease rate changes observed in our dataset. This question focusing on counties is also directly relevant to the dataset we are using because it enables us to manipulate and analyze infectious disease data reflected across the entire state of California. By including every California county in the scope of our dataset in the context of this question, we can confidently assess which areas of the state experienced the greatest growth or decline in disease cases. The resulting data from this analysis can then support theories and explanations behind what characteristics of counties drive disease rate changes as well as the key differences between areas experiencing increases and decreases.

## Question Two: How Case and Population Growth Differed Across Urban, Suburban, and Rural Counties? (Ethan)
The second question we sought to answer was “How do case and population growth differ across urban, suburban, and rural counties?”.  There are several reasons why this question is interesting and important. These reasons include social, economic, and cultural. Socially, finding the differences in population growth and case growth can reveal disparities in healthcare access, living conditions, and the infrastructure of public health in differently populated areas. Economically, finding an increase or decrease in cases within a county can affect labor markets, housing markets, and the allocation of resources, specifically pharmaceuticals. Culturally, the analysis of this data may highlight the response hygienically to a global pandemic, even though the pandemic was caused by a virus. All of these realizations could aid policymakers, urban planners, and healthcare leaders to intervene more efficiently. On the other hand, these same leaders would have more data to support the investment into various developments within the state of California. This question is tied to the dataset because of its emphasis on the correlation between population and infectious diseases, which are both prominently recorded in the dataset.

## Data Manipulations (Tony)
Data Manipulations for Question 1
Map of California Counties
image
image image

Filtered Sex to "Total" (to avoid gender splits).

Created a calculated field: ➔ Overall % Change

Compared latest year cases vs earliest year cases using FIXED [County].

Formula used ABS() to stabilize the denominator.

Fixed mapping issues by creating a calculated field: ➔ County (Mapped) = [County] + " County"

Plotted using Latitude (generated) and Longitude (generated).

Colored counties by SUM(Overall % Change):

Red = case increases

Blue = case decreases

Excluded invalid or ambiguous rows (like “California” row if present).

Since the dataset didn’t include 'County' at the end of the county names, we created a calculated field called 'County (Mapped)' to format the names correctly so Tableau could match them to real map locations

Top 5 and Bottom 5 Counties (Bar Charts)
image imageimage

Filtered to Top 5 & Bottom 5 Counties which saw the greatest changes in disease cases over time:

Sorted by highest Overall % Change for Top 5 and lowest Overall % Change for Bottom 5

Built two separate horizontal bar charts

One for Top 5 Greatest Increase

One for Bottom 5 Greatest Decrease

County on Rows and SUM(Overall % Change) on Columns

Colored bars with a gradient to emphasize magnitude of change

## Analysis and Results for Question One (Nabeel)

## Analysis and Results for Question Two (Claire)
<img width="312" alt="Screenshot 2025-04-27 at 8 03 56 PM" src="https://github.com/user-attachments/assets/c91eb1bd-212a-4ada-ae14-2f8faddf12f5" />

Analysis: 
- After looking at the scatterplot and trend lines it was apparent that urban counties (the blue points and trendline) show the highest case growth relative to population growth.
- The rural counties (red points and line) had moderate case growth relative to population growth.The case growth increased more with population growth thatn suburban counties, but less than urban ones.
- Suburban counties (purple line and points) had the lowest case growth relative to population growth. They hade an even smaller increase in case numbers when population growth was higher. 

Potential Explanation:
- The congestion of urban infrastructure will significantly increase the flow of infectious disease cases and population. 
- Suburban density seems to allow a controlled growth environment for population while controlling the flow of diseases.
- Rural areas tend to show more data variance due to smaller populations and a higher sensitivity to localized outbreaks. 



