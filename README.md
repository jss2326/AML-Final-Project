<div align="center">

# Predicting Blue-Chip Financial Health Trajectory  

### COMS 4995 – Applied Machine Learning: Final Project 
Group 24: Yu-Heng Chi, Param Sejpal, Jessica Villanueva, Yihan Yang, Zhiyi Zhang 

<br>

![stocklogo](https://github.com/user-attachments/assets/3fccb9f8-36b9-4098-b516-139212f2b59b)

</div>

## Objective

The focus of this project is to measure a company’s financial health and performance trajectory based on predicted financial metrics, such as *Market Cap* and *EBITDA Margins*. The companies we considered are Fortune1000 companies and the metrics are gathered from financial reports in 2024.

### Determining Company Financial Health Trajectory

“Is this company financial healthy” can be answered by several factors. We performed regression predict market capitalization ("Market Cap") and we classified companies as healthy or non-healthy based on their status as a growth or non-growth company. 

### I. Regression Objective
In this project, we use multiple regression models to predict a company's Market Cap using financial metrics including EBITDA, revenue, and other relevant features.

### II. Classification Objective
One measure of positive financial performance (described in Deliverable 1 as no bankruptcy or restructuring events, positive growth for certain financial metrics, and other factors) that tells us information about Market Cap is *profitability*. Therefore, we will classify these businesses as *Profitable* or *Non-Profitable* companies. 


## Installation

1. Clone this repo
2. Set up a virtual environment
3. `pip install -r requirements.txt`
4. (Optional) the dataset we use is included in this repo, but to see how we created the data, run the data creation script `generate.py` to create the dataset
5. Run the Jupyter notebook!



## Dataset
Many companies report EBITDA or earnings differently, which is why we created a dataset based on what we determined is the most consistent reflection of income statement and balance sheet data. **FinancialData.csv** is Financial data from Fortune1000 companies that was created using different sources of financial data. Income statement and balance sheet information was accessed from:
 
1. A [Kaggle dataset](https://www.kaggle.com/datasets/jeannicolasduval/2024-fortune-1000-companies/data) (k04dRunn3r on Kaggle).
2. Yahoo! Finance financials.
3. 10-K reports from the EDGAR archives on SEC.gov.



## Setup
This directory includes the following files.

1. **FinancialData.csv**: the final dataset we created and are using in this project.
2. `generate.py`: a quick script that can be run to see how the dataset was created.
    * Financial metrics that were added to the dataset come from Yahoo! Finance.
3. **KaggleData.csv**: The Kaggle dataset with basic company metrics (ticker, revenue, etc.) used in creating the dataset. 
4. **Past project deliverables**: this is added for reference and contains notes that we can refer to throughout the project.
5. `requirements.txt`: installation requirements.

 


## Brief Description of Metrics Used

1. **Rank**: company rank in the Fprtune1000 list.
2. **Ticker**: The stock symbol associated with a company.
3. **Sector**, **Industry**, **Type**: Economic categorization a company belongs to.
4. **Profitable**: (EBITDA Profitability) Profitability of a company, i.e., if total income outweighs expenses.
5. **Revenue**: Sales prior to any expenses.
6. **Market Cap**: Size of the equity portion of the business.
7. **Gross Profit**: Profit after deducting cost of goods sold.
8. **EBITDA**: Earnings before Interest Taxes Depreciation & Amortization - A non-GAAP, capital structure neutral, accrual accounting measure of profitability. EBITDA margins represents EBITDA as a percentage of total revenue.
9. **Profits Percent Change** and **Revenue Percent Change**: Growth percentage of current year's metric value from year before.
<br>

---

These metrics reflect how well the company is doing, potential sudden market events, and what investors think about a company's growth potential. More information on why these metrics were chosen and which machine learning techniques can be found under our Project Deliverable #1 and Project Deliverable #2 submissions (included in `deliverables/`). 
