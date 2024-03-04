
# Supply_Chain_Management_EDA



## Contents

- [Introduction](#Introduction)
- [Data Exploration](#Data-Dictionary)
- [Data Preprocessing](#Data-Processing)
- [Data Visualization](#Data-Visualization)
- [Suggestions](#Suggestions)

## Introduction


## Data Exploration


## Data Preprocessing
This project mainly focus on analyzing impact of features provided in the dataset on target variable product weight. 

### 1. Drop irrelevent columns
1. Unnamed: 0
2. Ware_house_ID
3. WH_Manager_ID
These three columns each contain entirely distinct values. In the context of this project, the uniqueness of these columns holds no relevance, as they are only analyzing product quantity. Therefore, these three columns have been removed.

### 2. Missing values
Among the 25 columns, null values are present in three columns. These columns correspond to the number of workers in the warehouse (workers_num), the year of warehouse establishment (wh_est_year), and the grade of government certificate approved for the warehouse (approved_wh_govt_certificate).

 **Plot of null values**
![](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/Null%20Values.png)

% of null values in eachg column:

workers_num(4.01 %)
wh_est_year(47.29 %)
approved_wh_govt_certificate(3.6 %)


**workers_num :**
 * numerical column
 * positively skewed
 Filled null values with median.

**wh_est_year :**

Since half of the values in the column wh_est_year are null, decided to drop it.

**approved_wh_govt_certificate:**
* categorical column
Filled null values with mode.

### 3. Duplicate values
No dupliocate values were present in the dataset.

### 4. Outliers

Outliers were present in some of the columns. plotted boxplot to locate outliers.
![1](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/Outliers%201.png)

![2](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/Outliers%202.png)


Determined the count of outliers in every column. Among them, the 'flood_proof' and 'flood_impacted' columns, each containing only two distinct values, exhibit significant disparities in their value distributions and lack correlation. one of the unique values is considered as outlier due to its significantly lower proportion. Consequently, both of these columns were removed from the dataset.

## Data Visualization
Relationship between other features and target variable Product weight

- **Warehouse location type & Owner Type**
![1](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-1.png)

- **Electric_supply & temp_reg_mach availability**
![2](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-2.png)

- **Storage issue reported in the last 3 months**
![3](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-3.png)


- **No. of warehouse breakdown in the last 3 months**
![4](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-4.png)

- **zone & Regional_zone**
![5](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-5.png)

- **Type of approval by government**
![6](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-6.png)

- **govt checking in last 3 months**
![7](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-7.png)

- **No. of workers**
![8](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-8.png)

-**Warehouse capacity size & Transport issue**
![9](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-9.png)

- **Competitor_in_mkt**
![10](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-10.png)


- **No. of Distributors**
![11](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-11.png)

- **No. of refill request in last 3 months**
![12](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-12.png)

- **Distance from hub**
![13](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-13.png)

![14](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-14.png)

- **Retail shop number**
![15](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-15.png)

- **Correlation Heatmap**
![16](https://github.com/Devika-K-M-15/Supply_Chain_Management_EDA/blob/main/Visuals/DA-16.png)


## Suggestions

- Focus on expanding warehouse operations in rural areas to capitalize on the higher average product weights and the larger share of total product weight, which can potentially lead to increased overall productivity and profitability.
- Prioritize investment in temperature regulating machines and enhancing electric supply availability for warehouses to improve product weight and overall warehouse performance.
- It is evident that, as production increases, storage issue increases. Hence, storage capacity must be upgraded to accomodate higher product weights. This highlights the importance of regularly assessing and expanding storage infrastructure in line with the production increments to ensure smooth warehouse operations and prevent bottlenecks.
- Implement proactive maintanance protocols. Invest in scalable solutions to accomodate higher production levels while minimizing the risk of operational disruptions caused by breakdowns. Conduct comprehensive analysis to identify root causes of braekdowns during periods of heightened production.
- Explore quality standards associated with different government approval grades. Identify opportunities to enhance product quality standards across all warehouse facilities.
- Workers number does not significantly affect production. Examine various factors such as technology adoption, training programs, and workflow optimization strategies to understand their collective impact on production efficiency.
