# Airbnb Listing Data Analysis 

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Observations](#observations)
- [Recommendations](#recommendations)
- [Closing Remarks](#closing-remarks)

  
## Project Overview

Welcome to the fascinating world of Airbnb listings, where data speaks volumes about host preferences, price trends, popular neighborhoods, and guest satisfaction. In this data analysis project, we delve into the diverse and dynamic realm of short-term rentals, uncovering insights that illuminate the patterns and preferences that shape the Airbnb landscape.

### Data Sources

Airbnb Listing Data: This dataset was obtained from kaggle and it was obtained in a csv format, containing detailed information about host,prices, neigbourhoods and guest influences like review and ratings. 

### Tools Used

- Excel: used for data cleaning and visualization
- SQL: Data Analysis

### Data Cleaning

- I used Excel Function to identify and remove rows with null values in key columns.
- I utilized Excel filters and sorting functionalities to identify and eliminate brows with blank entries.
- I Employed Excel's find and replace functionality to remove special characters from relevant columns.
- I utilized Excel functions and visualization tools to identify and exclude outliers.

### Exploratory Data Analysis

Exploratory data analysis involved the Airbnb data to answer questions, such as:


- Which Top 5 Neighbourhood have the highest average prices?
- What are the average prices of each room type?
- Which Neighbourhood are most popular based on their average number of review?
- Which room type is most popular?
- What are host preference on Instantly Bookable
- What are host preference on Cancellation Policy
- Which Room type is the most popular among the guest based on their average ratings
- Which Room type is the most popular among the guest based on their number of reviews

### Data Analysis

Include some interesting query from our sql analysis

```sql
SELECT TOP(5) neighbourhood, AVG(price) AS Average_price
FROM Project.dbo.Airbnbdata
GROUP BY neighbourhood
ORDER BY Average_price DESC
```
```sql
SELECT [room type], AVG(price) AS Average_price
FROM Project.dbo.Airbnbdata
GROUP BY [room type]
```
```sql
 SELECT TOP(6) neighbourhood, AVG([number of reviews]) AS Average_number_of_review
FROM Project.dbo.Airbnbdata
GROUP BY neighbourhood
ORDER BY Average_number_of_review DESC
```
```sql
SELECT [room type], COUNT(*) AS [Popular room type]
FROM Project.dbo.Airbnbdata
GROUP BY [room type]
ORDER BY [Popular room type] DESC
```
```sql
SELECT TOP(5) [instant_bookable], COUNT([host id]) AS [Amount of instant bookings]
FROM Project.dbo.Airbnbdata
GROUP BY [instant_bookable]
ORDER BY [Amount of instant bookings] DESC
```
```sql
SELECT cancellation_policy, COUNT(*) AS [Numbers of cancellation policy]
FROM Project.dbo.Airbnbdata
GROUP BY cancellation_policy
ORDER BY cancellation_policy DESC
```
```sql
 SELECT [room type], AVG([review rate number]) AS Average_ratings
 FROM Project.dbo.Airbnbdata
 GROUP BY [room type]
 ORDER BY Average_ratings DESC
```
```sql
 SELECT [room type], AVG([number of reviews]) AS Average_number_of_review
 FROM Project.dbo.Airbnbdata
 GROUP BY [room type]
 ORDER BY Average_number_of_review DESC
```
### Results

- The result shows that New Dorp, Chelsea, Staten Island, New Dorp Beach, Arden Heights and Eltingville are the top six neighbourhood with most average prices, This analysis may influence guests' booking decisions for guests seeking a more luxurious accommodation.
- In analyzing the average prices across different room types, a clear hierarchy emerges, with hotels commanding the highest average price of $657, followed closely by private rooms at $627. Entire homes or apartments maintain a competitive average price of $624, while shared rooms follow closely at $623.
- The analysis of the highest top six neighborhoods based on their average numbers of reviews reveals Huguenot, Richmondtown, Silver Lake, DUMBO, eltingvile and East Elmhurst. This indicates high guest engagement and satisfaction in these neighborhoods.
- The analysis demonstrates a clear hierarchy in room type popularity, with "Entire home/apt" and "Private room" being the top choices. This insight is valuable for hosts in optimizing their listings to align with guest preferences
- This breakdown indicates that a significant number of hosts (24,154) do not have the instant bookable feature enabled, while a slightly lower number (23,990) have this feature enabled.The analysis highlights a split in host preferences regarding the instant bookable feature. While a considerable number of hosts prefer a more manual booking process, a significant portion is open to instant bookings.
- The analysis reveals a balanced distribution of host preferences for cancellation policies, indicating that hosts on the platform have varied preferences when it comes to managing booking cancellations.
- Hotel rooms tend to receive higher average ratings, suggesting that guests generally have a more positive perception of hotel accommodations.
- Hotel rooms also attract a higher average number of reviews, indicating a higher level of engagement and feedback from guests.

### Observations

- Room Type Preferences: The analysis revealed diverse preferences among guests, with "Entire home/apt" and "Private room" being the most popular choices. Hosts can optimize their listings based on these preferences.
- Host Preferences: Host preferences vary, as seen in factors like instant bookability and cancellation policies. Airbnb can provide educational resources to assist hosts in making informed decisions aligned with guest expectations.
- Neighborhood Popularity: Certain neighborhoods stand out as popular choices among guests, influencing pricing dynamics. Hosts can leverage this information to tailor their strategies and amenities.
- Guest Satisfaction: Average ratings and number of reviews indicate a positive perception of hotel rooms, emphasizing the importance of quality assurance for hosts in other room types.

### Recommendations

- Continuous Education for Hosts: Airbnb can continue offering educational resources to hosts, covering topics like cancellation policies, instant bookability, and effective communication strategies.

- Dynamic Pricing Strategies: Hosts can implement dynamic pricing strategies based on neighborhood popularity and room type preferences to stay competitive and maximize revenue.

- Quality Assurance Initiatives: Implementing quality assurance initiatives for hosts, especially in room types other than hotel rooms, can enhance overall guest satisfaction and contribute to positive reviews.

- Flexibility in Policies: Offering flexibility in cancellation policies and minimum stay requirements can attract a broader range of guests and improve overall listing performance.

### Closing Remarks

The Airbnb listing data analysis has provided valuable insights into the factors influencing guest decisions and host behaviors. By leveraging these insights, hosts and Airbnb administrators can create a more responsive and guest-centric platform, contributing to a positive experience for both hosts and guests.




