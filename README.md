# [Coal-Terminal-Utilization-Analysis](https://public.tableau.com/app/profile/akshay.saraf/viz/TableCalculations_16605871923360/Report)

## Project Overview
This project finds out which of the 5 coal terminal machines is running above 10% idle capacity over the 
In a coal terminal plant, the reclaimer type machine require maintenance when within the previous month there was atleast one 8-hour period when the average idle capacity was over 10 %.
Idle capacity = (Actual Capacity - Nominal Capacity) / Nominal Capacity

## Data Source
The primary dataset used for this analysis is the csv file, which contains financial and overview information sheet about 1000 startups.

## Data Cleaning/Preparation
In the initial data preparation phase, I performed the following tasks:

- Data loading and inspection
  - The two sheets in the csv file, Financials and Overview, are connected to each other using an inner join in the tableau.
    ![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/Inner%20Join.jpg)
- Handling missing values.
  - No missing data
- Data cleaning and formatting
  - Duplicate columns ID and name removed.
  - Created folders to group the 2013–2014 and 2015 columns together.
    
    ![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/Folders.jpg)

## Exploratory Data Analysis
### 1. Number Of Companies Founded Each Year
The following bar chart shows the number of companies founded in each year from 1999 to 2014.
![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/No.%20of%20companies%20founded%20each%20year.jpg)

We can group a few of the previous years data (1999–2009) together using the group function in the tableau.
![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/No.%20of%20companies%20founded%20each%20other%20(group).jpg)

### 2. Average Number Of Employees In Each Industry
![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/Avg%20no.%20of%20employees%20in%20each%20industry.jpg)

### 3. Top 10 Startups By Growth %
![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/top%2010%20startups%20by%20growth%20%25.jpg)

### 4. 2015 Revenue vs. 2015 Expenses
Scatterplot

![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/2015%20Revenue%20vs.%202015%20Expenses%20Scatterplot.jpg)

Highlighted companies having higher revenue (>$9 million).

![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/2015%20Revenue%20vs.%202015%20Expenses%20Scatterplot(High%20Revenue).jpg)

Highlighted companies having lower expenses (<$5 million).

![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/2015%20Revenue%20vs.%202015%20Expenses%20Scatterplot(Lower%20Expenses).jpg)

Highlighted companies having higher revenue (>$9 million) and lower expenses (<$5 million). The Y-axis is reversed so that the quadrant is on the right-top side.

![](https://github.com/aksaraf/1000-Startups/blob/97ac005c8d4353cf94221d1e4ab2dc027493daa4/Images/2015%20Revenue%20vs.%202015%20Expenses%20Scatterplot(High%20Revenue%20%26%20Low%20Expenses).jpg)

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
