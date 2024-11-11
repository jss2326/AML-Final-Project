<div align="center">

# Predicting Blue-Chip Financial Health Trajectory  

### COMS 4995 – Applied Machine Learning: Final Project 
Group 24: Yu-Heng Chi, Param Sejpal, Jessica Villanueva, Yihan Yang, Zhiyi Zhang 

<br>

![stocklogo](https://github.com/user-attachments/assets/3fccb9f8-36b9-4098-b516-139212f2b59b)

</div>

## Objective

The focus of this project is on measuring a company’s financial health and performance trajectory based on predicted financial metrics, such as *stock price*, *revenue*, and *EBITDA margins*. Positive performance is indicated by whether it is a *Growth* or *Non-Growth* company. The financial metrics considered are from 10-K reports from 2009-2023 of 12 investment grade companies.

<br>

## Dataset
This directory includes the following.

1. **FinancialGrowthMetrics.csv**: the final dataset we created and are using in this project.

2. **FinancialGrowthMetrics.xlsx**: the original Excel file where you can see how the dataset was created.
    * Financial metrics that were added to the dataset are marked orange.
    * Metrics that are not used are light grey and crossed out.

3. **Past project deliverables**; this is added for reference and contains notes that we can refer to throughout the project.


 **FinancialGrowthMetrics.csv** is Financial data from 12 investment grade companies. Income statement and balance sheet information was accessed from (1) a Kaggle dataset (2) Yahoo! Finance financials and (3) 10-K reports from the EDGAR archives on SEC.gov. 

Many companies report EBITDA or earnings differently, which is why we created a dataset based on what we determined is the most consistent reflection of income statement and balance sheet data.

<br> 

## Brief Description of Metrics

1. **Revenue**: Profit made in sales.

2. **Stock price**: Market valuation of company.

3. **Gross Profit**: Profit after deducting cost of goods sold.

4. **Net Income**: Company income after deducting expenses and cost of goods sold.
    $$\( \text{Net Income} = \text{Revenue} – \text{Expenses} – \text{COGS}\)$$

5. **Cash Flow From Operations**: Cash generated from business operations. 

6. **EBITDA per Employee**: The proportion of the company's EBITDA that each employee contributes to.

7. **Free Cash Flow**: Remaining cash after operating expenses and capital expenditures.
    $$\( \text{Free Cash Flow} = \text{Cash Flow from Operations} – \text{Capital Expenditures} \)$$

8. **EBITDA Margins %**: EBITDA as a percentage total revenue.

9. **Cash Flow from Operations % of Sales**: OCF as a percentage of revenue. 

10. **EBITDA Growth** and **Revenue Growth**: Growth percentage of current year's metric value from year before.


11. **Modified Free Cash Flow**: Free Cash Flow adjustment used to assess liquitidy by showing free cash available after reinvesting assets.

<br>

## Determining Company Financial Health Trajectory

“Is this company financial healthy” can be answered by several factors, including... 
* bankruptcy/restructuring events
* growth/non-growth
* credit ratings
* stock rating from top 3 banks
* multiple other metrics

### Predicting Financial Performance 
The financial metrics we considered include stock price, revenue, and EBITDA margin. A growth rate above 5-10% YOY signifies financial growth.
 
Which metrics indicate poor financial performance?:
* Debt/EBITDA ratio above 5x
* EBITDA/Interest Expense below 1.1x
* Stock price declines below 20% YTD
* Revenue declines over 5% fiscal-to-fiscal YOY
* Negative Free Cash Flow
* Low EBITDA margins 

### Growth Indication
A company will be classified as a **growth** or **non-growth** depending on certain indicators. 

Which metrics indicate growth?:
* Positive EBIDTA growth year-to-year
* Similarly, positive revenue growth year-to-year
* A high proportion of EBITDA per Employee
* High Cash Flow from Operations 
* Consistently positive Net Income 

---

These metrics reflect how well the company is doing, what investors think about a company's growth potential, etc. More information on why these metrics were chosen and which machine learning techniques we will used based on the nature of our dataset can be found under our Project Deliverable #1 and Project Deliverable #2 submissions (also listed under this directory). 
