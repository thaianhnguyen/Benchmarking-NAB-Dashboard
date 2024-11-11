# Bank Performance Benchmarking Dashboard
The report has been published on Power BI service at here: [**_Bank Benchmarking Dashboard_**](https://app.powerbi.com/view?r=eyJrIjoiN2JhNDUwZDQtMTRmZC00MWM4LTg5ZTYtZTM2OTgyNmZjZDRlIiwidCI6ImFmMWYzNzUzLTM5MjUtNGU2Zi05NDliLTk3YzAwNzMyMDgwMyIsImMiOjEwfQ%3D%3D)
---
## Version: [**_Vietnamese_**](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/README.md)
Table of contents
=================

<!--ts-->
* [Business scenario and dataset](#Business-scenario-dataset)
* [Data cleaning with Python](#Data-cleaning)
* [Visualization](#Visualization)
   * [Insights](#insights)
   * [Details](#details)
       * [Market position](#market-position)
       * [Profitability](#profitability)
       * [Asset quality](#asset)<!--te-->
<a name="Business-scenario-dataset"/> </br>
## Business scenario and dataset

In this project, I conducted a data analysis on financial statement data from the banking sector over the past five years to see if how a bank is performing compared to the sector, then to draw some useful insights about its strengths, weaknesses as well as its growth opportunity and threat in the future.

The benchmarked bank is randomly selected: Nam Á Bank - NAB.

Data used is the financial statements of all commercial banks over the period of 2018-2023, acquired through the platform [FiinPro](https://fiinpro.com/fiinpro-x)
<a name="Data-cleaning"/> </br>
## Data cleaning  

The data is in form of excels file and structured in conventionally financial wide format - panel data. 
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/data.jpg)</br>

The library used:</br>
- os, openpyxl: to access folder directory and excel files
- panda, re: to convert data into long-format structure for analysis purposes and clean data . </br>
- numpy, seaborn: perform mathematic data transformations and EDA </br>

The python script can be found here: [Python Script](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/clean%20bank%20data.ipynb)

<a name="Visualization"/> </br>
## Visualization: </br> <a name="insights"/> </br>
### Insights:
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/Slide_eng.JPG) </br>
### Details: <a name="details"/> </br>
### Market positions: <a name="market-position"/> </br>
- In 2023, NAB’s revenue and profits are still in the lower range within the group of banks with medium-sized assets (100K billion VND to 500K billion VND). However, the growth rates of both asset size and revenue/profit are at or higher than the industry average.
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/mkt_position_1.jpg)</br>

- NAB's market share in deposits and assets has grown since 2018. However, in the last 3 years, market share growth has stagnated or even turned negative → This could limit NAB's growth potential in its credit activities.
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/mkt_2.jpg)</br>

- For NAB’s deposit composition, the CASA ratio is very low compared to the industry average. → This indicates that NAB’s cost of capital is higher than the industry, which reduces the bank’s profit margin. </br>
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/mk_position_3.jpg)</br>

### Profitability: <a name="profitability"/> </br>
- NAB’s profitability is modest compared to the industry average, but has gradually improved over years and approached the industry average in 2023.
    - One reason for this improvement can be attributed to effective cost control over the past years.
</br>

![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/profit_1.jpg)</br>

### Asset quality: <a name="asset"/> </br>
- NAB’s asset quality is good, as the Capital Adequacy Ratio (CAR) and Loan-to-Deposit Ratio (LDR) are both within the safe limits set by the State Bank of Vietnam, and NAB's non-performing (NPL) ratio is lower than the industry average.
- However, the LDR is at the regulatory maximum of 85% → NAB has to increase its deposit in order to expand its loan portfolio while maintaining good liquidity.
</br>

![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/asset_1.jpg)</br>

- A low Provision Coverage Ratio (PCR) suggests that NAB is provisioning less for loan losses compared to its current NPL . NAB is trading off credit risk for short-term gains in profitability. If the current NPL is not effectively controlled and loans are to default in the future, NAB’s profitability could be heavily impacted.
</br>

![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/asset_2.jpg)</br>




