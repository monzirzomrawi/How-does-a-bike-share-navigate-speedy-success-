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
  
- I used Power Query’ s add column feature to add a new column "day_of_week" from "started_at" column.

  ![Screenshot (34)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/aeb73209-9591-497c-8acf-5344619b695c)
  
- I found that each ride_id is unique.
  
- I added another column "month" to show the month of the year for each ride.

  ![Screenshot (35)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/e2d0795f-ccce-4a4d-be5a-ff16e3acc3e2)
  
- some columns like "start_station_name" and "end_station_name" have blank values.
  
- I replaced each blank value with "Not Available" because deleting the rows that have blank values in some columns will reduce the amount of my data.
  
- I used Power Query’ s add column feature to add  a custom column "duration_of_ride_length".

  ![Screenshot (36)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/edd41de8-096d-4214-824b-5540f640c1db)
  
- From the "duration_of_ride_length" column, I added two new columns "minutes" and "seconds".
  
- I added another new column "ride_length_by_minutes" to determine the length of the bike ride in minutes

  ![Screenshot (37)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/5a3788a2-2635-46ad-9d5a-cad8ac2bbf0f)

- I closed Power Query, and loaded the data. I view my data as a connection because Excel table can’t show 5 million rows data

  ![Screenshot (38)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/d41eb7f7-ee00-4692-846e-dac9e7c47587)



# Analyzing and Visualizing the Data


- Each time I created a chart, I will insert a pivot table and a recommended chart = screen 20

  ![Screenshot (39)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/ad49d6c4-edb1-43da-bc51-8404582793a1)
  
- I computed the total number of rides for casual and member riders= screen 24.

![Screenshot (40)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/5de4d426-9361-4538-acc0-d8f7327ddb19)

   In 2022, member riders use bikes more frequently than casual riders.
  
- I computed the average ride length for casual and member riders.

![Screenshot (41)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/70892a81-cde5-4617-a57b-c211d91e8964)

    In 2022, casual riders use bikes for longer period of time than member riders.
  
- I computed the total number of rides for casual and member riders by day.

![Screenshot (42)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/8af5a466-d0fd-4dab-bf7e-10d6b6266d25)

 On Saturday , casual riders use bikes more frequently followed by Sunday.
  
- I computed the sum of ride length for casual and member riders by day.

![Screenshot (43)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/2210d306-db54-4e55-ac11-1bca942626ad)

  On Saturday , casual riders use bikes for longer period of time followed by Sunday while member riders have the most on Thursday.
  
- I computed the total number of rides for casual and member riders by month of the year.

![Screenshot (44)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/ae3bfcd6-d7f1-44e6-9943-1eef07f61407)

  In July casual riders use bikes more frequently followed by June while member riders have August the most.
  
  - I computed the sum of ride length for casual and member riders by month
  
  ![Screenshot (45)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/ad413da5-c42b-4ded-ab82-989a7630a28c)
  
    In july, casual riders use bikes for longer period of time followed by June. Member riders have the most in July too
    
- Total Number of Rides by Bike Type for Casual and Member.

![Screenshot (46)](https://github.com/monzirzomrawi/How-does-a-bike-share-navigate-speedy-success-/assets/172976501/83395ca9-ecfb-4bb3-acea-93f4ebe6d3f3)

  Casual riders use electric bike more frequently while member use classic bike the most.

# My recommendations based on my analysis
- Increasing the number of electric bike because casual riders use it the most.

- Since casual riders use bikes more frequently and for longer period of time on Saturday and Sunday, encouraging casual riders to become members on these two days is a good idea .


- Since casual riders use bikes more frequently and for longer period of time in July and June, 
encouraging casual riders to become members in these two months is a good idea.


 
Thank you for taking time to review my first capstone project! I learned a lot from it because I used real-world data and business questions. I completed the entire project using only Excel.

  
