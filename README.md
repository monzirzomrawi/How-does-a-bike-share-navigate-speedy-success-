# How-does-a-bike-share-navigate-speedy-success-


## Introduction
Welcome to my first project as a junior data analyst for the Google Data Analytics Professional Certificate.
After completing 8 courses in this professional track and acquiring a wealth of knowledge and skills,
I am eager to apply what I have learned to a real-world challenge.
This case study marks the final step in completing the professional certificate, 
allowing me to showcase my ability to analyse and extract insights from complex data. 
In this project, I will be working with a large dataset using Excel to demonstrate my proficiency in data analysis. 

## About the company
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geo tracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.
Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic. 
## Scenario
I am a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, my team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, my team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve my recommendations, so they must be backed up with compelling data insights and professional data visualizations.

## Ask questions and define the problem.
Asking the proper questions is the first step in the data analysis process. As a data analyst, it is important for me to understand why I am doing the analysis and what I am attempting to accomplish. Understanding the stakeholders' expectations and keeping the lines of communication open help me characterize the issue. To guarantee that I have a thorough comprehension of the situation, I take the big picture into account when describing the issue.

## Ask the right questions.
 The following three questions will guide the future marketing program:
 
1. How do annual members and casual riders use Cyclistic bikes differently?

2. Why would casual riders buy Cyclistic annual memberships?
 
3. How can Cyclistic use digital media to influence casual riders to become members?
   
In this case study, I’m going to answer the first question.

## Identify the business task.

The goal is to design marketing strategies aimed at converting casual riders into annual members. In order to do that, we need to better understand how annual members and casual riders differ. This can be done by analyzing the Cyclistic historical bike trip data to identify trends.

## Identify key stakeholders.
-	The director of marketing: who is responsible for the development of campaigns and initiatives to promote the bike-share program.

-	The Cyclistic executive team: who is notoriously detail-oriented and will decide whether to approve the recommended marketing program.
  
-	The Cyclistic marketing analytics team: which is a team of data analysts who are responsible for collecting, analysing, and reporting data that helps guide marketing strategies.

# Prepare the data by collecting and storing data.


## Data Location

Data is located [Here](https://divvy-tripdata.s3.amazonaws.com/index.html?trk=article-ssr-frontend-pulse_little-text-block), and it’s a public dataset. I'll use the data from 2022, which is made of 12 CSV files, each of which corresponds to a month of the year.

## Data Organization
The data is organized as zip files, each file has CSV data for a specific month  
## Data Credibility ROCC?
   This data is.
1.	Reliable: this data is accurate, complete, and unbiased.
	
2.	Original: this data is validated by the original source
   
3.	 Comprehensive: this data contains all the critical information to answer the questions
   
4.	Current: this data is useful with time pass
   
6.	Cited: this data is credible and citied from this source [Here](https://divvy-tripdata.s3.amazonaws.com/index.html?trk=article-ssr-frontend-pulse_little-text-block)

## Data License
1.	The data is maintained and made available by Motivate International Inc. under this [license](https://ride.divvybikes.com/data-license-agreement?trk=article-ssr-frontend-pulse_little-text-block)
   
2.	that data-privacy issues prohibit me from using riders’ personally identifiable information.
   
3.	I won’t be able to connect pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes.
## Download the data.
1.	I selected data files for the 12 months from January 2022 to December 2022.
	
3.	Every file was downloaded and saved as a CSV file 


## DATA PREPARATION PROCESS.

I used Power Query in Excel to merge 12 CSV files that correspond to the months of the year into one file. After merging, the dataset has 5,667,717 rows.

![Screenshot (33)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/8002e05c-be3a-4f49-9927-4d95f41d2c07)


Now, the data is ready for cleaning


# Data processing.
I used only Power query in EXCEL for data cleaning because normal EXCEL sheet can’t show this 5 million rows data.

- I deleted the column "Source_Name".
  
- I used Power Query’ s add column feature to add a new column "day_of_week" from "started_at" column. = screen 16
  
- I found that each ride_id is unique.
  
- I added another column "month" to show the month of the year for each ride. = screen 21
  
- some columns like "start_station_name" and "end_station_name" have blank values.
  
- I replaced each blank value with "Not Available" because deleting the rows that have blank values in some columns will reduce the amount of my data.
  
- I used Power Query’ s add column feature to add  a custom column "duration_of_ride_length". = screen 17
  
- From the "duration_of_ride_length" column, I added two new columns "minutes" and "seconds".
  
- I added another new column "ride_length" to determine the length of the bike ride in minutes = screen = screen 18

- I closed Power Query, and loaded the data. I view my data as a connection because Excel table can’t show 5 million rows data = screen 19



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Arrival Delay".
- Step 5 : For calculating average delay time, null values were not taken into account as only less than 1% values are null in this column(i.e column named "Arrival Delay") 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for four fields named "Class", "Customer Type", "Gate Location" & "Type of travel".
- Step 9 : Two card visuals were added to the canvas, one representing average departure delay in minutes & other representing average arrival delay in minutes.
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 10 : A bar chart was also added to the report design area representing the number of satisfied & neutral/unsatisfied customers. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of customers are also seggregated according the gender. 
- Step 11 : Ratings Visual was used to represent different ratings mentioned below,

  (a) Baggage Handling

  (b) Check-in Services
  
  (c) Cleanliness
  
  (d) Ease of online booking
  
  (e) Food & Drink
  
  (f) In-flight Entertainment

  (g) In-flight Service
  
  (h) In-flight wifi service
  
  (i) Leg Room service
  
  (j) On-board service
  
  (k) Online boarding
  
  (l) Seat comfort
  
  (m) Departure & arrival time convenience
  
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some customers.

All these values have been ignored while calculating average rating for each of the parameters mentioned above.

- Step 12 : In the report view, under the insert tab, two text boxes were added to the canvas, in one of them name of the airlines was mentioned & in the other one company's tagline was written.
- Step 13 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 
- Step 14 : Calculated column was created in which, customers were grouped into various age groups.

for creating new column following DAX expression was written;
       
        Age Group = 
        
        if(airline_passenger_satisfaction[Age]<=25, "0-25 (25 included)",
        
        if(airline_passenger_satisfaction[Age]<=50, "25-50 (50 included)",
        
        if(airline_passenger_satisfaction[Age]<=75, "50-75 (75 included)",
        
        "75-100 (100 included)")))
        
Snap of new calculated column ,

![Snap_1](https://user-images.githubusercontent.com/102996550/174089602-ab834a6b-62ce-4b62-8922-a1d241ec240e.jpg)

        
- Step 15 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(airline_passenger_satisfaction[ID])
        
A card visual was used to represent count of customers.

![Snap_Count](https://user-images.githubusercontent.com/102996550/174090154-424dc1a4-3ff7-41f8-9617-17a2fb205825.jpg)

        
 - Step 16 : New measure was created to find  % of customers,
 
 Following DAX expression was written to find % of customers,
 
         % Customers = (DIVIDE(airline_passenger_satisfaction[Count of Customers], 129880)*100)
 
 A card visual was used to represent this perecntage.
 
 Snap of % of customers who preferred business class
 
 ![Snap_Percentage](https://user-images.githubusercontent.com/102996550/174090653-da02feb4-4775-4a95-affb-a211ca985d07.jpg)

 
 - Step 17 : New measure was created to calculate total distance travelled by flights & a card visual was used to represent total distance.
 
 Following DAX expression was written to find total distance,
 
         Total Distance Travelled = SUM(airline_passenger_satisfaction[Flight Distance])
    
 A card visual was used to represent this total distance.
 
 
 ![Snap_3](https://user-images.githubusercontent.com/102996550/174091618-bf770d6c-34c6-44d4-9f5e-49583a6d5f68.jpg)
 
 - Step 18 : The report was then published to Power BI Service.
 
 
![Publish_Message](https://user-images.githubusercontent.com/102996550/174094520-3a845196-97e6-4d44-8760-34a64abc3e77.jpg)

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://user-images.githubusercontent.com/102996550/174096257-11f1aae5-203d-44fc-bfca-25d37faf3237.jpg)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://user-images.githubusercontent.com/102996550/174074051-4f08287a-0568-4fdf-8ac9-6762e0d8fa94.jpg)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.
