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

## Data Manipulations (Tony)

### Data Manipulations for Question 1
#### Map of California Counties
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

#### Top 5 and Bottom 5 Counties (Bar Charts)
![image](https://github.com/user-attachments/assets/0f2ae972-8f12-4d56-adca-b8109f6d3d14)
![image](https://github.com/user-attachments/assets/087fe553-1eb5-4b58-a53f-4cf494d448cf)![image](https://github.com/user-attachments/assets/dbba78af-2003-4eef-8074-f49925bd6681)


Filtered to Top 5 & Bottom 5 Counties which saw the greatest changes in disease cases over time:

Sorted by highest Overall % Change for Top 5 and lowest Overall % Change for Bottom 5

Built two separate horizontal bar charts

One for Top 5 Greatest Increase

One for Bottom 5 Greatest Decrease

County on Rows and SUM(Overall % Change) on Columns

Colored bars with a gradient to emphasize magnitude of change


## Analysis and Results for Question One (Nabeel)
![image](https://github.com/user-attachments/assets/6f9d3322-66d5-4ac1-b2dd-52ad5bcf6793)
![image](https://github.com/user-attachments/assets/cd8cdff6-a7cd-466a-9f89-64d9c4642001)
![image](https://github.com/user-attachments/assets/fdb9d329-c774-4a1c-8e17-7f2bb3499802)
Across California, counties with the greatest increases in disease cases are often urban or highly connected areas. For example, Modoc County had the largest percent increase, even though it is rural and sparsely populated, showing that small communities can still experience sharp changes. The other counties in the top five, like Lake, Marin, Imperial, and Santa Cruz, are primarily urban or suburban, where larger populations and closer contact likely contributed to faster spread. On the other hand, the bottom five counties, including Sierra and Plumas, are smaller, rural areas where decreases were more common. Sierra County, notably, is one of the least populated counties in the state and showed the greatest overall decline.

Several factors help explain these patterns. In general, higher population density leads to faster disease transmission simply because people are in closer contact. Transportation networks like highways and airports can further accelerate exposure and movement of infections, especially in major hubs. Meanwhile, rural counties with fewer residents, greater physical distance between people, and difficult-to-travel terrain — similar to regions near the Rocky Mountains — tend to have lower exposure rates and slower spread over time. These differences highlight how location, density, and infrastructure all play important roles in public health trends.





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



