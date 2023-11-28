
# Project Learnings
## Overview
This repository contains code and analysis for a project focused on understanding and improving sales and customer experience. The project involves data cleaning, manipulation, and exploratory data analysis (EDA) using Python libraries such as pandas, matplotlib, and seaborn. The primary goals are to identify potential customers across different demographics, improve customer experience, and enhance sales strategies.

## Getting Started

### Prerequisites
Make sure you have the following installed:

- Python
- Jupyter Notebook or any other Python environment

### Installation
#### 1. Clone the repository:
```
git clone https://github.com/tuseeqraza1/Python_Sales_Analysis.git
cd Python_Sales_Analysis
```
#### 2. Install required libraries:
```
pip install numpy pandas matplotlib seaborn
```
### Download the dataset:

[Sales Data.csv](https://github.com/tuseeqraza1/Python_Sales_Analysis/blob/main/Sales%20Data.csv)

## Code Structure
The code is structured as follows:

- <b>Import Libraries:</b> Import necessary Python libraries including numpy, pandas, matplotlib, and seaborn.
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
- <b>Load Data:</b> Load the sales data from the CSV file and perform initial data exploration.
```
df = pd.read_csv('Sales Data.csv', encoding='unicode_escape')
```
- <b>Data Cleaning:</b> Remove irrelevant columns and handle null values.
```
df.drop(['Status', 'unnamed1'], axis=1, inplace=True)
df.dropna(inplace=True)
df['Amount'] = df['Amount'].astype('int')
```
- <b>Exploratory Data Analysis (EDA):</b> Analyze data to gain insights into customer demographics and sales patterns.
```
# Example: Gender analysis
ax = sns.countplot(x='Gender', data=df, hue='Gender', palette=colors.values(), legend=False)
# ... (similar sections for Age, State, Marital Status, Occupation, Product Category)
```
## Exploratory Data Analysis (EDA)
The EDA section is divided into several sub-analyses:

1. <b>Gender Analysis:</b> Visualizes the distribution of buyers based on gender and their purchasing power.

2. <b>Age Analysis:</b> Examines the age groups of buyers and their purchasing behavior.

3. <b>State Analysis:</b> Identifies the top states contributing to the highest number of orders and total sales.

4. <b>Marital Status Analysis:</b> Explores the relationship between marital status, gender, and purchasing power.

5. <b>Occupation Analysis:</b> Analyzes the distribution of buyers across different occupations.

6. <b>Product Category Analysis:</b> Investigates the most popular product categories and their sales.

7. <b>Top Sold Products:</b> Highlights the top 10 most sold products.

## Conclusion
The project's findings indicate that married women aged 26-35 years, residing in Uttar Pradesh, Maharashtra, and Karnataka, working in IT, Healthcare, and Aviation sectors, are more likely to purchase products from Food, Clothing, and Electronics categories. These insights can inform targeted marketing strategies and inventory planning to enhance customer experience and increase sales.

Feel free to explore the Jupyter Notebook for a detailed walkthrough of the analysis.


