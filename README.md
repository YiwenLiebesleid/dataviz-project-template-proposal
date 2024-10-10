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

(insert one or more hand-drawn sketches of interactive visualizations that you imagine)
(describe each sketch - how is the data visualized, what are the interactions, and how do these relate to the questions/tasks)

---

## Prototypes

I’ve created a proof of concept visualization of this data. It's a ... and it shows ...

[![image](https://user-images.githubusercontent.com/68416/65240758-9ef6c980-daff-11e9-9ffa-e35fc62683d2.png)](https://vizhub.com/curran/eab039ad1765433cb51aad167d9deae4)

(please put a screenshot of one or more visualizations of this dataset you already made, for previous assignments, and link to them)

You can put images into here by pasting them into issues.

You can make images into links like this:

```
[![image](https://user-images.githubusercontent.com/68416/65240758-9ef6c980-daff-11e9-9ffa-e35fc62683d2.png)](https://vizhub.com/curran/eab039ad1765433cb51aad167d9deae4)
```


Also, you can study the [source](https://raw.githubusercontent.com/curran/dataviz-project-template-proposal/master/README.md) to figure out Markdown formatting. You can use the GitHub built-in editor to edit the document.

---

## Open Questions

(describe any fear, uncertainty, or doubt you’re having about the feasibility of implementing the sketched system. For example, “I’m not sure where to get the geographic shapes to build a map from this data” or “I don’t know how to resolve the codes to meaningful names” … Feel free to delete this section if you’re confident.)

---

## Milestones

(for each week, estimate what would be accomplised)
