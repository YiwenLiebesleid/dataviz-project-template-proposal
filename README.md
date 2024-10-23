# Data Visualization Project

## Data

The data I propose to visualize for my project is *Sleep Efficiency Dataset*. Data source: https://www.kaggle.com/datasets/equilibriumm/sleep-efficiency, Vizhub: https://vizhub.com/YiwenLiebesleid/sleep_efficiency

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

I will mainly focus on age, gender, sleep duration, sleep efficiency, XXX sleep percentage, and lifestyle attributes.

---

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * How different age groups and genders vary in sleep patterns (XXX sleep percentage), sleep duration, and sleep efficiency.
 * Correlation between caffeine consumption, alcohol consumption, exercise frequency, and sleep efficiency. (i.e. correlation(caffeine, sleep efficiency), ...)
 * Understand the distribution of lifestyle attributes, and distribution of sleep patterns in different sleep efficiency groups.

---

## Sketches

<p>
<img src=./doc/sketch1.jpg align="center" width=600 />
<img src=./doc/sketch2.jpg align="center" width=600 />
</p>
<!-- ![image](./doc/sketch1.jpg "sketch1")
![image](./doc/sketch2.jpg "sketch2") -->

The 1st sketch is related to Task 1, I consider using brushing in this viz, so when selecting one group then all the related plots are highlighted. It visualized the sleep pattern percentage of each age group or gender, and also the sleep patterns and efficiency of each age group or gender.

The 2nd sketch is related to Task 2 & 3. I'm thinking when selecting the efficiency group in task 3, all data related to this group should be highlighted in both T  ask 2 and 3. It visualized the correlation between each lifestyle and sleep efficiency, and also the distribution of these lifestyles in different sleep efficiency groups.

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

## Open Questions

- I'm not sure if the correlation scatter plots will work, because from my current prototype, I find the correlation vague.
- Displaying the average sleep duration and average sleep efficiency in one chart may cause problem, should I split them into 2 charts?

---

## Milestones

- Week 8: pre-process datasets: https://vizhub.com/YiwenLiebesleid/processed_sleep_efficiency_dataset
- Week 9: Task 1 pie charts
- Week 10: Task 1 bar charts
- Week 11: Task 2 scatter plots
- Week 12: Task 3 bar charts
- Week 13: try to add interactions (brushing? clicking?)
- Week 15: merge all the works
