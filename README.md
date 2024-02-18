# [Coal-Terminal-Utilization-Analysis](https://public.tableau.com/app/profile/akshay.saraf/viz/TableCalculations_16605871923360/Report)

## Project Overview
In a coal terminal plant, the reclaimer type machine require maintenance when within the previous month there was atleast one 8-hour period when the average idle capacity was over 10 %.

Idle capacity = (Actual Capacity - Nominal Capacity) / Nominal Capacity

This project provides insights and recommendations about which of the 5 machines have exceeded this level.

## Data Source
The primary dataset used for this analysis is the csv file, which contains 5 sheets having information about each machine.

## Data Cleaning/Preparation
In the initial data preparation phase, I performed the following tasks:

- Data loading and inspection
  - The five sheets in the csv file are connected to each other using an left join in the tableau.
    ![Data Connection](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Data%20Connection.jpg
)
    
- Handling missing values
- Data cleaning and formatting
  - Created a new datetime sheet so as to connect the 5 sheets together
  - 
    ![Timeline Sheet](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Timeline%20Sheet.jpg
)
  - Created a pivot table to reduce the number of columns

    Before
    
    ![Unpivot table](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Unpivot%20table.jpg)

    After
    
    ![Pivot table](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Pivot%20Table.jpg)

## Exploratory Data Analysis and Recommendations
### 1. RECLAIMER 1 (RL1)
The image below illustrates the 8 hour moving avreage of Idle capacity for Reclaimer 1 (RL1) expressed as a % of nominal capacity
Throughout the month RL1 exceeded the allowable thresold multiple times

2/9 - rolling average peaked at 14%
14/9 - rolling average peaked at 12%
21/9 - rolling average peaked at 15%

Also, the trend line shows upward trend. So if the machine keeps working with all other fators unchanged, the 8 hours moving average idle capacity will approximately increase 0.05% in the long run.

![RL1](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Reclaimer%201.jpg)


### 2. RECLAIMER 2 (RL2)
The image above illustrates the 8 hour moving avreage of Idle capacity for Reclaimer 2 (RL2) expressed as a % of nominal capacity.

The machine RL2 has not crossed the idle capacity 10% once in the given timeframe. On the 10th Sept 2015, the machine was running on full capacity and on further investigation looks like it was done on purpose by sacrificing the capacity of SR6 (discussed in the coming slides).

Also, the trend line is showing downward trend so there machine won't require maintenance soon.

![RL2](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Reclaimer%202.jpg)

### 3. STACKER - RECLAIMERS 1 (SR1)
The image above illustrates the 8 hour moving avreage of Idle capacity for Stacker-Reclaimer 1 (SR2) expressed as a % of nominal capacity.

The machine has not crossed idle capacity thresold of 10%. This suggests that the machine is running and does not require maintenance soon.

The gap in the chart between 10th Sept 00:00 to 16th Sept 23:00(inclusive) is due to the machine working as a stacker and not as reclaimer (we are only concerned about reclaimers data).

![SR1](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/SR1.jpg)

### 4. STACKER - RECLAIMERS 4A (SR4A)
The image above illustrates the 8 hour moving avreage of Idle capacity for Stacker-Reclaimer 4A (SR4A) expressed as a % of nominal capacity.
The machine has not crossed idle capacity thresold of 10%. This suggests that the machine is running and does not require maintenance soon.
The gap in the chart between 13th Sept 00:00 to 16th Sept 23:00(inclusive) is due to the machine working as a stacker and not as reclaimer (we are only concerned about reclaimers data).
Also, the trend line shows upward trend. So if the machine keeps working with all other fators unchanged, the 8 hours moving average idle capacity will approximately increase 0.12% per hour in the long run. It is recommend to check performance of this machine in coming weeks as preventive maintenance may require.

![SR4A](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/SR4A.jpg)

### 5. STACKER - RECLAIMERS 6 (SR6)
The image above illustrates the 8 hour moving avreage of Idle capacity for Stacker-Reclaimer 6 (SR6) expressed as a % of nominal capacity.


The machine has  crossed idle capacity thresold of 10% on 10th Sept 2015 but at the same time the machine RL2 was running on full capacity and as both these machines are in the same line on the stockyard, we can say that capcity of machine SR6 was sacrificed to give priority to machine RL2. If that is the case then machine SR6 does not require maintenance as it has not crossed idle capacity at any other point of time.

![SR6](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/SR6.jpg)

## Summary
![Summary](https://github.com/aksaraf/Coal-Terminal-Utilization-Analysis/blob/51d4af07cda7596d6888091d1a685a8c4226a5d8/Images/Summary.jpg
)

## Tableau Learnings:
1. How to create groups
2. Groups vs. Sets
3. Static Sets
4. Dynamic Sets
5. Combining Sets
6. Controlling Sets with Parameters
7. Controlling Sets with Formulas

## Reference
[Tableau Advanced: Master Tableau in Data Science](https://www.udemy.com/course/tableau10-advanced/)
