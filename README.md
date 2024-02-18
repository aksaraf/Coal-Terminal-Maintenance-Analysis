# [Coal-Terminal-Utilization-Analysis](https://public.tableau.com/app/profile/akshay.saraf/viz/TableCalculations_16605871923360/Report)

## Project Overview
The project focuses on maintenance requirements for reclaimer-type machines within a coal terminal plant. Maintenance is deemed necessary when, during the preceding month, there has been at least one 8-hour period where the average idle capacity exceeded 10%.

Idle capacity = (Actual Capacity - Nominal Capacity) / Nominal Capacity

The objective of this project is to provide insights and recommendations regarding the identification of any of the 5 machines that have surpassed this threshold.

## Data Source
The main dataset utilized for this analysis is a CSV file comprising 5 sheets, each containing information specific to one of the machines.

## Data Cleaning/Preparation
In the initial data preparation phase, I performed the following tasks:

- Data loading and inspection
  - The five sheets in the CSV file are linked together through a left join in Tableau.
    ![Data Connection](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Data%20Connection.jpg
)
    
- Handling missing values
- Data cleaning and formatting
  - A new datetime sheet was created to facilitate the connection between the five sheets.
    
    ![Timeline Sheet](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Timeline%20Sheet.jpg)

  - A pivot table was generated to streamline the number of columns.
    
    Before
    
    ![Unpivot table](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Unpivot%20table.jpg)

    After
    
    ![Pivot table](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Pivot%20Table.jpg)

## Exploratory Data Analysis and Recommendations
### 1. RECLAIMER 1 (RL1)
Throughout the month, RL1 exceeded the allowable threshold on multiple occasions:

- On September 9th, the rolling average peaked at 14%.

- On September 14th, the rolling average peaked at 12%.

- On September 21st, the rolling average peaked at 15%.

Additionally, the trend line indicates an upward trend. Therefore, if the machine continues operating with all other factors unchanged, the 8-hour moving average idle capacity is projected to increase by approximately 0.05% in the long run.

![RL1](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Reclaimer%201.jpg)


### 2. RECLAIMER 2 (RL2)

The machine RL2 did not exceed the idle capacity threshold of 10% throughout the specified timeframe. On September 10th, 2015, the machine was operating at full capacity, and upon further investigation, it appears that this was intentionally done by sacrificing the capacity of SR6 (discussed below).

Furthermore, the trend line indicates a downward trend for RL2. Therefore, it is unlikely that this machine will require maintenance in the near future.

![RL2](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Reclaimer%202.jpg)

### 3. STACKER - RECLAIMER 1 (SR1)
The machine has not exceeded the idle capacity threshold of 10%. This indicates that the machine is operational and does not require maintenance in the near future.

The gap in the chart between September 10th at 00:00 and September 16th at 23:00 (inclusive) is attributed to the machine functioning as a stacker rather than as a reclaimer. It's important to note that we are only focusing on the data related to reclaimers.

![SR1](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/SR1.jpg)

### 4. STACKER - RECLAIMER 4A (SR4A)
The machine has not surpassed the idle capacity threshold of 10%, indicating that it is currently operational and does not require immediate maintenance.

The gap in the chart between September 13th at 00:00 and September 16th at 23:00 (inclusive) is a result of the machine operating as a stacker rather than as a reclaimer. It's worth noting that our analysis solely focuses on data related to reclaimers.

Additionally, the trend line exhibits an upward trajectory. Therefore, if the machine continues to operate with all other factors unchanged, the 8-hour moving average idle capacity is projected to increase by approximately 0.12% per hour in the long run. It is advisable to monitor the performance of this machine closely in the upcoming weeks, as preventive maintenance may be necessary.

![SR4A](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/SR4A.jpg)

### 5. STACKER - RECLAIMER 6 (SR6)

The machine exceeded the idle capacity threshold of 10% on September 10th, 2015. However, during the same timeframe, machine RL2 was running at full capacity. Given that both machines are located on the same line in the stockyard, it can be inferred that the capacity of machine SR6 was sacrificed to prioritize machine RL2. In this scenario, it appears that machine SR6 does not require maintenance as it did not exceed the idle capacity threshold at any other point in time.

![SR6](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/SR6.jpg)

## Summary
![Summary](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Summary.jpg
)

## Reference
[Tableau Advanced: Master Tableau in Data Science](https://www.udemy.com/course/tableau10-advanced/)
