# WellbeingStudy 
## IronHack Bootcamp Final Project 
### by [Isabel Jabs](https://github.com/IsabelJabs)
### May 2021

## Content

- [Project Outline](#project-outline)
- [The Data](#the-data)
- [Visualisation](#visualisation)
- [Machine Learning](#machine-learning)
- [Review and Outlook](#review-and-outlook)
- [Links](#links)

## Project Outline


We build a machine learning model for a real estate company to predict the selling prices of houses based on a variety of features on which the value of the house is evaluated. 
The senior management of the real estate company also wants us to explore the characteristics of the houses using some business intelligence tools. One of those parameters includes understanding which factors are responsible for higher property value - $650.000 and above.



## The Data

More tham 15000 survey results from a [Website about Happiness and Wellbeing](http://www.authentic-happiness.com) during a time frame from July 2015 to March 2021. 
The data contains information about age, gender, date of filling out the survey and 20 wellbeing features, which are answers to the survey questions. 
In order to analyse the 20 features best, 5 categories with each 4 features were identified and each scored low, medium or high: 
Body
Mind
Connection
Achievement 
Meaning

In detail: 
1. Body
* fruits_veggies: 0, 1, 2, 3, 4, 5 or more servings per day
* bmi_range: 1 (below 25) 2 (more than 25: overweight)
* daily_steps: 1.000 to 10.000 (in 1k steps) 
* sleep_hours per night: 1h to 10h (in 1h steps) 

2. Mind
* sufficient_income: (sufficient, not sufficient)
* daily_stress: scale 1 to 5 
* daily_shouting: passive or active aggressions per week
* weekly_meditation: times per week for time for yourself

3. Achievement
* personal_awards: No. of big recognitions in life (0-10)
* todo_completed: 0 to 10 how well you complete your to-do list
* achievement: No. of successes over the last 12 month 
* flow: hours per day 

4. Connection, assessing the strength of your network and your inclination to discover the world;
* core_circle: very close people 0 to 10 
* lost_vacation: days per year
* social_network: interactions on a typical day 0 to 10 
* places_visited: 0 to 10 new places 

5. Meaning, evaluating your compassion, generosity and how much 'you are living the life of your dream’.
* donation: times of financial donation or volunteering per year
* live_vision: clear for how many years, 0 to 10 
* supporting_others: how many people did your help the last 12 month, 0 to 10 
* time_for_passion: daily hours, 0 to 10

![Survey](http://www.authentic-happiness.com/your-life-satisfaction-score)
![Data set](https://www.kaggle.com/ydalat/lifestyle-and-wellbeing-data)
