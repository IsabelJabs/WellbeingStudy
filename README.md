# Wellbeing and Lifestyle Study 
## IronHack Bootcamp Final Project 
### by [Isabel Jabs](https://github.com/IsabelJabs)
### May 2021

## Content

- [Project Outline](#project-outline)
- [The Data](#the-data)
- [Visualisation](#visualisation)
- [Machine Learning](#machine-learning)
- [Review](#review)

## Project Outline

This study investigates how different factors of wellbeing and lifestyle of people influence each other. 
A machine learning model was built to predict high achieving people based on their body, mind, connection and meaning wellbeing situation.
The question, if a high meaning in life will result in high achievements has been visualised and evaluated. 
Furthermore the relationship between meaning and achievement for gender and different age groups has been analysed. 

[Presentation](https://github.com/IsabelJabs/WellbeingStudy/blob/main/Presentation/Wellbeing_Lifestyle_DA_Presentation.pdf)

## The Data

More than 15000 survey results from a [Website about Happiness and Wellbeing](http://www.authentic-happiness.com) during a time frame from July 2015 to March 2021. 
The data contains information about age, gender, date of filling out the survey and 20 wellbeing features as answers to the survey questions. 
The survey group is probably generally interested in the wellbeing topic as this survey is found to be a website about happiness and wellbeing. 

Gender: 62% Female (9858), 38% Male (6113)
4 Age Groups: under 21, 21-35, 36-50 and over 50

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

4. Connection
* core_circle: very close people 0 to 10 
* lost_vacation: days per year
* social_network: interactions on a typical day 0 to 10 
* places_visited: 0 to 10 new places 

5. Meaning
* donation: times of financial donation or volunteering per year
* live_vision: clear for how many years, 0 to 10 
* supporting_others: how many people did your help the last 12 month, 0 to 10 
* time_for_passion: daily hours, 0 to 10

[Survey](http://www.authentic-happiness.com/your-life-satisfaction-score)

[Data set](https://www.kaggle.com/ydalat/lifestyle-and-wellbeing-data)

## Visualisation

After the correlation of the categories achievement and meaning have been found to have the highest correlation (48%), they were investigated further and visualised in Tableau. 

The assumption of high achievers having high meaning in their life could not be seen in the data, as seen below. The combination high achievements & high meaning makes 8% of the total with 1313 people. 
The highest number of people have the combination low meaning & low achievement (3499 people or 22%) or medium meaning & medium achievement (4117 people or 26%). We can also see that very few people who have high meaning in their live will have low achievements (186 or 1%). 

![vis](https://github.com/IsabelJabs/WellbeingStudy/blob/main/Images/Arc_Meaning_Achievement.png)


Looking at the average achievement and meaning per age group and gender, there is a visible trend to people having more meaning and achievement when in older age groups, which is not surprising but logical. Interestingly women meaning in life increases even more than their achievements and for men it is the other way around. 

![avg](https://github.com/IsabelJabs/WellbeingStudy/blob/main/Images/Avg_age_gender.png)

[Tableau Visualisations](https://public.tableau.com/profile/isabeljabs#!/vizhome/Wellbeing_Lifestyle/Overview?publish=yes)

## Machine Learning 

The machine learning was conducted to predict the high achievers (Category: Achievement, Score: High). 
The high achievers are only 18% of the total, which leads to an imbalanced sample size. 
Therefore the Randon Forest Classifier Model resulted in a Precision score of 51%, Recall 33% and Accuracy Score of 57%. 
The Logistic Regression result was Precision 54%, Recall 31% and Accuracy score of 83%.
After oversampling the high achiever class with SMOTE the result of the Logistic Regression improved to Precision 70%, Recall 75% and Accuracy Score of 72%.

[JupyterNotebook: Machine Learning](https://github.com/IsabelJabs/WellbeingStudy/blob/main/MachineLearning/wellbeingML.ipynb)

## Review

The expectation of the study to show that people with high meaning in their life also have high achievements could not be seen.
The categorisation of features and visualisation has shown that people with low meaning in life often have low achievements (and/or the vice versa) and people with medium meaning in life often have medium achievements (and or vice versa). 

The average aggregated data devided by age groups and gender showed, that meaning in life and achievements increase from young to older age groups.
Furthermore meaning increases more in female older age groups, while achievements increase more in male older age groups.

The category that had the second highest correlations to others was the connection category to achievement and to meaning. 

Surprisingly the body and mind categories did not have significant correlations. 
A reason for these result could be found in the small sample size or in the features that describe the categories. 




