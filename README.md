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
    ![Data Connection]()
    
- Handling missing values
- Data cleaning and formatting
  - Created a new datetime sheet so as to connect the 5 sheets together
    ![Timeline Sheet]()
  - Created a pivot table to reduce the number of columns
    ![Unpivot table]()
    ![Pivot table]()

## Exploratory Data Analysis
### 1. 

### 2. 

### 3.

### 4.

## Final Dashboard
The dashboard has a revenue cutoff, an expense cutoff, and a top startups by growth% slider so that venture capitalists can adjust the values according to individual requirements to select the top startups for investment.
![](https://github.com/aksaraf/1000-Startups/blob/0be6a3816a19bc48fa3962288339eba8e145a666/Images/Top%20Startups.png)


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
