# Sales Dashboard
Sales Dashboard Excel Project

![Recording of Dashboard Functions: 1 Dashboard Recording](https://github.com/user-attachments/assets/7625125c-ba5d-4867-9802-bb8e1cd2ad70)

## Dashboard  
The final dashboard can be found here: [Sales Dashboard](https://github.com/DataJane/Sales_Dashboard/blob/main/Sales%20Dashboard.xlsx)


## Table of Contents
- [1. Skills Used](#1-skills-used)
- [2. The Data](#2-the-data)
- [3. Exploratory Data Analysis](#3-exploratory-data-analysis)
- [4. The Analysis](#4-the-analysis)
- [5. Dashboard Build](#5-dashboard-build)
- [6. Conclusion](#6-conclusion)


## 1. Skills Used  
- 📊 Exploratory Data Analysis  
- 🧮 Formulas and Functions  
- 📚 Pivot Tables  
- 📐 Statistics  
- 🎛️ Creating Dashboards  


## 2. The data:
I downloaded this dataset from Kaggle from: [Sales Dataset](https://www.kaggle.com/datasets/sahilislam007/sales-dataset/data)  
The dataset is a sales dataset for a store, consisting of 1000 rows, giving information on:  
- 🧑🏻‍🧑‍🧒 gender  
- 🔞 age  
- 🛒 product category   
- 📚 quantity bought   
- 💲 price per unit and   
- 💵 total sale amount.  


## 3. Exploratory Data Analysis
I loaded the csv file into Excel and conducted EDA, using statistical analysis and Pivot charts.  
- There are 1000 customers.  
- The average transaction value is £456  
- I calculated the average age for customers.  
- The statistical average age is 41.3, being slightly lower for females.   
- The Median age is 42 for both males and females in the dataset.  

![Screenshot of Average age calculation: 2 Average Age Calculation](https://github.com/user-attachments/assets/be45cb85-8cd3-48be-8ea0-85fbbbde63ba)
**Average Age Calculation**


## 4. The Analysis
### Analysis by Quantity and Value
- When the sales were divided into product categories, clothing drove the biggest volume of sales followed by Electronics, then Beauty.  
- Analysing by Value of sales, Electronics has the highest value by a small margin, followed by clothing, Beauty has the lowest value sales.  

![Charts showing Sales by Volume and Sales by Value: 3 Sales by Volume Sales by Value](https://github.com/user-attachments/assets/0300ca4b-6006-4990-b9a4-6bf164352907)
**Charts: Sales by Volume & Sales by Value**

### Analysis by Age Groups
I divided the data into age bins by decades and analysed their spending.  
- The 40-49 and 50-59 age groups are the largest groups.  
- In terms of spending the 50-59 age group spend the most.  
- Despite being the smallest group, the 10-19 age group spend the most per capita. This dataset has some rather well-off 18 & 19 year old's!  

![Three Charts, by age bins, Number of customers, total spent & spend per capita: 4 No_Customers-Total_Spent-Spend_Per_Capita](https://github.com/user-attachments/assets/52d016a1-47b3-4be8-a7ef-ee729bd29116)

**Charts: Number of Customers, Total Spent, Spend per Capita**

### Analysis by Product Category and Gender

This shows clear distinctions with females spending more on clothing and beauty, and males spending more on electronics.  

![Chart of Sales by Product Category & Gender: 5 Sales_by_Product_Cat_Gender](https://github.com/user-attachments/assets/7974235c-50f2-4674-b2df-734930eae49b)

**Chart: Sales by Product Category & Gender**

### Timeline Analysis 
- The highest sales were in May and October, the lowest were in March and September. 
- There are only two records in the dataset for January 2024.  

![Chart of Total Sales timeline; 6 Total_Sales_Time](https://github.com/user-attachments/assets/b3306923-86cf-4097-b1f9-52c39a49776b)

**Total Sales Timeline** 


## 5. Dashboard Build 
- Each of the above analyses was plotted as a graph and placed on the dashboard for the owner of the business to use. 
- I added slicers for Gender, Age group, and Product category.  
- These interact with the graphs as appropriate.
- Where slicers would eliminate most of the bars on a chart, they are not linked to that chart.

![Screenshot of Dashboard](https://github.com/user-attachments/assets/1aae557c-01a4-40d1-a3de-cae704d9a0a0)

**Dashboard**

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
![Screenshot of Key Card](https://github.com/user-attachments/assets/195afacb-c8ce-4f47-bd76-2b1ed60c75dd)
**Key Card**

- If multiple items are selected on the slicers, the key cards display Not Available. 
- A message pops up on the dashboard indicating to the user to choose single values on the slicers, then the key cards will display values.


### Alternatives
- I executed a version of the dashboard utilising data validation inputs for the key cards and slicers for the charts.  
- However, the final version is cleaner and means the data is unified between charts and key cards.


## 6. Conclusion
- In this analysis, clothing had the biggest volume of sales, whereas electronics led in value.   
- Overall, females spent more than males.   
- Females were more likely to spend on beauty and males on electronics.  
- I’ve provided an interactive dashboard to provide insights into the data underlying the model.  
- This has been a helpful learning tool in developing interactivity between keycards and slicers and in consolidating learning from other courses so far.  
- I’m looking forward to stretching my skills further.
