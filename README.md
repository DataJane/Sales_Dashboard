# Sales Dashboard
Sales Dashboard Excel Project

## Under Construction 
**1 Dashboard recording**

## Skills Used  
- Exploratory Data Analysis  
- Formulas and Functions  
- Pivot Tables  
- Statistics  
- Creating Dashboards  

## Dashboard  
The final dashboard can be found here: 

## The data:
I downloaded this dataset from Kaggle from: [Sales Dataset](https://www.kaggle.com/datasets/sahilislam007/sales-dataset/data)  
The dataset is a sales dataset for a store, consisting of 1000 rows, giving information on   
- gender,   
- age,   
- product category,   
- quantity bought,   
- price per unit and   
- total sale amount.  

## Exploratory Data Analysis
I loaded the csv file into Excel and conducted EDA, using statistical analysis and Pivot charts.  
- There are 1000 customers.  
- The average transaction value is £456  
- I calculated the average age for customers.  
- The statistical average is 41.3, being slightly lower for females.   
- The Median is 42 for both males and females in the dataset.  

** 2 Average Age Calculation  **

### Analysis by Quantity and Value
- Splitting the sales into product categories, clothing drove the biggest volume of sales followed by Electronics then Beauty.  
- Analysing by Value of sales, Electronics has the highest value by a small margin, followed by clothing, Beauty is the lowest value sales.  

** 3 Screenshot 2 charts Sales by Volume and Sales by Value **

### Analysis by Age Groups
I split the data into age bins by decades and analysed their spending.  
- The 40-49 and 50-59 age groups are the largest groups.  
- In terms of spending the 50-59 age group spend the most.  
- Despite being the smallest group, the 10-19 age group spend the most per capita. This dataset seems to have some rather well off 18 & 19 year olds!  

** 4 Screenshot 3 charts – no of customers, total spent, spend per capita **

### Analysis by Product Category and Gender

This shows clear distinctions with females spending more on clothing and beauty and males spending more on electronics.  

** 5 Screenshot sales by product category & gender **

### Timeline Analysis 
- The highest sales were in May and October, the lowest were in March and September. 
- There are only two records in the dataset for January 2024.  

** 6 Screenshot Total Sales graph ** 

## Dashboard
- Each of the above analyses are plotted as a graph and placed on the dashboard for the owner of the business to use. 
- I added slicers for Gender, Age group and Product category.  
- These interact with the graphs as appropriate. 

** 7 Screenshot of dashboard **

### Key Cards
Using array multiplication, I calculated values for median spend per transaction, number of items purchased, and price per unit. 
These are linked to the item showing on each of the three slicers.

For example, for the median spend:
```
=IFERROR(MEDIAN(IF((
(Sales[Product Category]=Category_Pv)*
(Sales[Gender]=GenderPv)*
(Sales[Age Bin]=Age_Gp_Pv)
),Sales[Total Amount],FALSE)),"Not Available")
```
8 Key Card

- If multiple items are selected on the slicers, the key cards display Not Available. 
- A message pops up on the dashboard indicating to the user to choose single values on the slicers, then the key cards will display values.


##Alternatives
- I executed a version of the dashboard utilising data validation inputs for the key cards and slicers for the charts.  
- However this version is cleaner and means the data is unified between charts and key cards.

##Conclusion
- In this analysis, clothing had the biggest volume of sales, whereas electronics led on value.   
- Overall females spent more than males.   
- Females were more likely to spend on beauty and males on electronics.  
- I’ve provided an interactive dashboard to provide insights into the data underlying the model.  
- This has been a helpful learning tool in developing interactivity between keycards and slicers and in - consolidating learning from other courses so far.  
- I’m looking forward to stretching my skills further.
