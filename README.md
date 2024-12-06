# Data Visualization Project

## Data

The data I use in this project is *Sleep Efficiency Dataset*. Data source: https://www.kaggle.com/datasets/equilibriumm/sleep-efficiency, Vizhub: https://vizhub.com/YiwenLiebesleid/sleep_efficiency

### Description of the dataset

This dataset is about a study of sleep efficiency and sleep patterns, it contains information about a group of test subjects and their sleep patterns.

Each test subject is identified by a unique Subject ID and their age and gender are also recorded. The Bedtime and Wakeup time features indicate when each subject goes to bed and wakes up each day, and the Sleep duration feature records the total amount of time each subject slept in hours. The Sleep efficiency feature measures the proportion of time spent in bed that is spent asleep. The REM sleep percentage, Deep sleep percentage, and Light sleep percentage features indicate the time each subject spent in each stage of sleep. The Awakenings feature records the times each subject wakes up during the night. Additionally, the dataset includes information about each subject's caffeine consumption and alcohol consumption in the 24 hours before bedtime, their smoking status, and their exercise frequency.

### Attributes
- ID
- Age (ordered): (9, 69)
- Gender (categorical): 50% male and 50% female
- Bedtime
- Wakeup time
- Sleep duration (ordered): (5, 10)
- Sleep efficiency (ordered): (0.5, 0.99)
- REM sleep percentage (ordered): (15, 30)
- Deep sleep percentage (ordered): (18, 75)
- Light sleep percentage (ordered): (7, 63)
- Awakenings (ordered): (0, 4)
- Caffeine consumption (ordered): (0, 200)
- Alcohol consumption (ordered): (0, 5)
- Smoking status (categorical): (yes, no)
- Exercise frequency (ordered): (0, 5)

I mainly focus on age, gender, sleep duration, sleep efficiency, XXX sleep percentage, and lifestyle attributes (e.g. caffeine, alcohol, exercise).

---

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * How different age groups and genders vary in sleep patterns (XXX sleep percentage)?
 * How different age groups and genders vary in sleep duration and sleep efficiency?
 * Correlation between sleep efficiency and lifestyle attributes (caffeine consumption, alcohol consumption, exercise), and understand the distribution of lifestyle attributes in different sleep efficiency groups.

---

## Sketches

<p>
<img src=./doc/sketch1.jpg align="center" width=600 />
<img src=./doc/sketch2.jpg align="center" width=600 />
</p>
<!-- ![image](./doc/sketch1.jpg "sketch1")
![image](./doc/sketch2.jpg "sketch2") -->

The 1st sketch is related to Task 1, I consider using brushing in this viz, so when selecting one group then all the related plots are highlighted. It visualized the sleep pattern percentage of each age group or gender, and also the sleep patterns and efficiency of each age group or gender.

The 2nd sketch is related to Task 2 & 3. I'm thinking when selecting the efficiency group in task 3, all data related to this group should be highlighted in both Task 2 and 3. It visualized the correlation between each lifestyle and sleep efficiency, and also the distribution of these lifestyles in different sleep efficiency groups.

---

## Prototypes

I’ve created a proof of concept visualization of this data: 

- A pie chart showing the sleep pattern percentage distribution in age group 1 (9~19).
- A bar chart showing average sleep duration and efficiency in each age group.
- A scatter plot of the correlation(exercise, sleep efficiency).
- A bar chart for the caffeine consumption in each sleep efficiency group.

<p>
<img src=./doc/age_group1.png align="center" width=300 />
<img src=./doc/age_group1_distribution.png align="center" width=300 />
<img src=./doc/exercise.png align="center" width=300 />
<img src=./doc/caffine.png align="center" width=300 />
</p>

---

## Milestones

> Note: some of the following visualizations were updated during the process.


### Week 8: Pre-process Dataset
Link: https://vizhub.com/YiwenLiebesleid/processed_sleep_efficiency_dataset

1. Implementation:
I processed each data example to have an "age_group", and an "efficiency_group" with Python. 
- The age group is mapped in this way: {1:9-19, 2:20-29, 3:30-39, 4:40-49, 5:50-59, 6:60-69}. 
- The efficiency group is split into quartiles, therefore 4 groups are formed, a larger group number means higher sleep efficiency.

I also processed the NaNs in the attributes into 0s.

Later I will use this processed dataset instead of the original one for visualization. 

<img src=./doc/task0_dataset.png align="center" width=600 />


### Week 9: Task 1 Pie Charts
Link: https://vizhub.com/YiwenLiebesleid/83bb0cc6abc648c4bd076ad9574cf7eb

1. Implementation:
I computed the average deep sleep, REM sleep, and light sleep percentages of each age group and gender, and translated them into pie charts that easily illustrate the sleep patterns (different sleep stage proportions) in each group. It shows how the sleep pattern varies in different age groups, and different genders.

<img src=./doc/task1_v2_pie1.png align="center" width=600 />

2. Interaction:
- Toolkit buttons: the left top of the page shows 2 buttons: "Age" and "Gender". If you press one of them, the corresponding group results will be displayed.
- Hover: moving the mouse over the legend rectangles (i.e. XXX sleep) will only display the corresponding part in each pie chart, so you can easily compare the percentage of that sleep type in each group.

<img src=./doc/task1_v2_pie2.png align="center" width=600 />

3. Analysis:
This viz shows how sleep patterns vary in different age groups and genders.
- For different age groups:
  + REM sleep is quite close in each group, about 22.5% on average, while for the youngest group (9~19) this ratio is only 19.2%.
  + Light sleep and Deep sleep have more diverse distributions, the youngest group (9~19) and oldest group (60~69) have much more light sleep and much less deep sleep, compared to other groups. People in the middle age group (30~39) seems to have the most deep sleep.
- For different genders:
  + REM sleep is quite close, which is similar to age results.
  + Male has more deep sleep than female in general.


### Week 10: Task 1 Bar Charts
Link: https://vizhub.com/YiwenLiebesleid/2c0712efb0ad4813aead97542e81f53c

1. Implementation:
I computed the average sleep duration and efficiency of each age group and gender, and translated them into bar charts. The yellow bars correspond to the left y-axis (duration), while the purple bars correspond to the right y-axis (efficiency).

<img src=./doc/task2_v2_bar1.png align="center" width=600 />

2. Interaction: 
- Toolkit buttons: the left top of the page shows 2 buttons: "Age" and "Gender". If you press one of them, the corresponding group results will be displayed.
- Hover:
  + When moving the mouse onto one bar, all bars in the same chart of the same attribute (duration/efficiency) will display numbers.
  + When moving the mouse onto the legends, the bar charts will only display the corresponding attribute (duration/efficiency) to better observe each attribute's trend.

<img src=./doc/task2_v2_bar2.png align="center" width=600 />

3. Analysis:
This viz shows how sleep duration and efficiency vary in different age groups and genders.
- For different age groups:
  + Sleep duration: the youngest group (9~19) has a notably longer duration (7.9 hours) than other groups (7.5 hours on average).
  + Sleep efficiency: 2 middle age groups (30~39, 40~49) share the highest sleep efficiency in all groups, and on the contrary, the youngest group (9~19) has the lowest sleep efficiency, which is as low as 0.68
- For different genders: gender shows very little change in this dimension. The average sleep duration and average sleep efficiency is quite close for male and female.


### Week 11: Task 2 Scatter Plots
> Note: the following description is for an older version of my implementation for this task.

Link: https://vizhub.com/YiwenLiebesleid/24a05d8f436d44f388af4fd2ca5aedf4

1. Implementation:
I choose to use the following 3 lifestyle attributes: caffeine consumption, alcohol consumption, and exercise. I plot scatter plots with their trendlines to show the correlation between each lifestyle attribute and sleep efficiency. I also set color with interpolateViridis to strengthen the display of sleep efficiency (darker color means higher efficiency). 

2. Interaction:
- It should be responsive to fit different screen sizes
- Hover:
  + If you move the mouse over the "Trendline" legend, it will highlight the 3 trendlines in the scatter plots, and display the equations.
  + If you move the mouse over any trendline in the scatter plot, (which should be with a low opacity in the natural state), it will highlight this trendline and display its equation.

<img src=./doc/task2_correlation.png align="center" width=600 />

3. Analysis:
From the visualization here, we can observe that the correlation between caffeine consumption and efficiency is small, while alcohol consumption and exercise times do have some impact on sleep efficiency: higher alcohol - lower efficiency; higher exercise - higher efficiency.


### Week 12: Task 3 bar charts
Link (v1): https://vizhub.com/YiwenLiebesleid/2add5d94142440e8b86b4c46b5d02041

Link (v2): https://vizhub.com/YiwenLiebesleid/c71db0d850e84c6899d9b17af9b92acc

1. Implementation:
I computed the average caffeine and alcohol consumption and exercise times of each sleep efficiency group, and translated them into bar charts. 

<img src=./doc/task4_bar0.png align="center" width=600 />

2. Interaction:
(Version 1)
- Hover:
  + When moving the mouse onto one bar, all bars will display the number of caffeine/alcohol.
  + When moving the mouse onto the legends, the bar charts will only display the corresponding attribute.

<img src=./doc/task4_bar1.png align="center" width=600 />

(Version 2)
- Hover:
  + When moving the mouse onto one bar, all bars will display the value of caffeine/alcohol/exercise (y-axis).
  + When moving the mouse onto one bar, the selected bar will be highlighted.

<img src=./doc/task4_bar2.png align="center" width=600 />

3. Analysis:
This viz shows how the trend of lifestyle differs in different efficiency groups. For example:
- People in higher efficiency groups consume relatively more caffeine before sleep.
- People in higher efficiency groups consume significantly less alcohol.
- People in higher efficiency groups do more exercises on average.


### Week 13: Add Interactions 

1. Implementation:
This week I added interactions to Task 1 pie charts, and Task 1 bar charts. (already updated in previous figures)


### Week 14: Merge all works
Link: https://vizhub.com/YiwenLiebesleid/09f09799636447728beb6130a6246898

1. Implementation:
This week I combined the Task 3 and Task 4 visualizations together, so if you select one lifestyle attribute, it will show both the scatter plot and bar chart of that lifestyle and sleep efficiency.

<img src=./doc/new_task3_1.png align="center" width=600 />

<img src=./doc/new_task3_2.png align="center" width=600 />

2. Interaction:
- Toolkit buttons: the right of the page shows 3 buttons: "caffeine", "alcohol" and "exercise". If you press one of them, the corresponding scatter plot and bar chart will be displayed.
- Hover:
  + When moving the mouse onto the trendline in the scatter plot (which should be in light yellow in the natural state), the trendline will be highlighted in red color, and its equation will be shown next to the trendline.
  + When moving the mouse onto one bar, your selected bar will be highlighted, and all bars will display the corresponding numbers.

3. Analysis:
This visualization shows the correlation between each lifestyle attribute and sleep efficiency, and also the average lifestyle value in each sleep efficiency group. From low to high, 0 means lowest efficiency, and 4 means highest efficiency.

From the visualization here, we can observe that:
- caffeine consumption has a small positive impact on sleep efficiency, with no obvious trend in both charts.
- alcohol consumption has some negative impact on sleep efficiency, higher alcohol consumption may result in lower efficiency.
- exercise times has an obvious positive impact on sleep efficiency, higher exercise times may result in higher efficiency.


---
## Final Conclusions
All works are collected in this article: https://vizhub.com/YiwenLiebesleid/6ebb1b5f7e804a95b0d4fe25710466b7

1. Different age groups and genders do have different distributions of sleep patterns. (the percentage of deep, light, and REM sleep)
2. The sleep duration and sleep efficiency vary a lot in different age groups, while remaining similar in different genders.
3. Different lifestyle attributes show different impacts on sleep efficiency: caffeine has a small positive impact, alcohol has a negative impact, and exercise as an obvious positive impact. (so I can give simple suggestions like: to have better sleep efficiency, one should consume less alcohol before sleep, and exercise more each week)
