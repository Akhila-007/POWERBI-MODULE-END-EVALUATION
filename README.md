# POWERBI-MODULE-END-EVALUATION
REPORT

Q1: 

Data Cleaning and Loading

1. Data Import
   
The CSV dataset was imported into Power BI and opened in Power Query Editor for cleaning and transformation.

3. Data Cleaning
   
•	Replaced missing text values with "Unknown". 
•	Converted OrderDate to Date format and handled missing dates. 
•	Removed duplicate rows. 
•	Imputed missing UnitPrice using the median 29,354. 
•	Calculated missing Sales using Quantity × UnitPrice. 
•	Replaced negative and missing Cost values using the median 75,435. 
•	Calculated missing Profit using Sales − Cost. 
•	Applied appropriate data types to all columns. 
The cleaned data was then loaded into Power BI.


Q2:

Visualizations and Insights

Three visualizations were created 

•	Pie Chart: Order Distribution by Region 
•	Column Chart: Top 5 Products by Number of Orders 
•	Line Chart: Profit Trend Over Time


Q3: DAX Calculations

a)	Calculated Table named EastRegionOrders created using the DAX:
EastRegionOrders = FILTER( SalesData,SalesData[Region] = "East")

b)	Calculated Column named ProfitCostDifference creating usind the DAX:
ProfitCostDifference = SalesData[Profit] - SalesData[Cost]

c)	Calculated Measure named TotalProfit created using the DAX:
TotalProfit = SUM(SalesData[Profit])


