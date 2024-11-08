# Bank Performance Benchmarking Dashboard
The report has been published on Power BI service at here: [**_Bank Benchmarking Dashboard_**](https://app.powerbi.com/view?r=eyJrIjoiNDhmZWUxNzAtZTljNi00MDVhLWFmZTYtMTc4MTgzMDNhNTY3IiwidCI6ImFmMWYzNzUzLTM5MjUtNGU2Zi05NDliLTk3YzAwNzMyMDgwMyIsImMiOjEwfQ%3D%3D&fbclid=IwAR19SyBorqdDhtuXZaKvqBwRLDbzsqN-1SsMNP7veJgnAn43vM0rNTJC4YQ)
---

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
       * [Asset quality](#asset)
<!--te-->
<a name="Business-scenario-dataset"/> </br>
## Business scenario and dataset
---

In this project, I conducted a data analysis on financial statement data from the banking sector over the past five years to see if how a bank is performing compared to the sector, then to draw some useful insights about its strengths, weaknesses as well as its growth opportunity and threat in the future.

The benchmarked bank is randomly selected: Nam Á Bank - NAB.

Data used is the financial statements of all commercial banks over the period of 2018-2023, acquired through the platform [FiinPro](https://fiinpro.com/fiinpro-x)

<a name="Data-cleaning"/> </br>
## Data cleaning  

The data is in form of excels file and structured in conventionally financial wide format - panel data. 
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/data.jpg)</br>

The library used:</br>
- os, openpyxl: to access folder directory and excel files
- panda, re: to convert data into long-format structure for analysis purposes and clean data . </br>
- numpy, seaborn: perform mathematic data transformations and EDA </br>

The python script can be found here: [Python Script]()

<a name="Visualization"/> </br>
## Visualization:

đã khiến $\color{rgb(31,119,180)}{\textsf{tăng 20%}}$	

<a name="insights"/> </br>
### Insights:
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/Slide_eng.JPG)</br>

<a name="details"/> </br>
### Details
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_3.jpg)</br>
For this page, I hope that the users can gain insights about sales for a specific region or for a specific product category, or both. That is why I created two 2 simultaneous slicers and also edit the interaction between certain visuals to be "Filter". For example, the user want to now the sales and top 10 product categories sold in Bahia:</br>
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_4.jpg)</br>
Or how much Art-labeled products was selling in Rio de Janeiro:</br>
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_5.jpg)</br>
Lastly, I address the sales manager's requirement regarding customer insight in the third page:

<a name="market-position"/> </br>
### Market positions:
- Although the average revenue and profit over the past 5 years are in the lower range compared to other banks in the medium asset size group (from 100K to 500K billion), NAB's asset growth rate as well as revenue/profit growth are higher than industry and medium banks group average.
- NAB has seen market share increases in asset, deposit and credit, however there has been no growth, or even slight shrinking in market share in the past two years. </br>

![alt text]()</br>

<a name="profitability"/> </br>
### Profitability:

-dasj </br>
![alt text]()</br>

<a name="asset"/> </br>
### Asset quality:

-dasj </br>
![alt text]()</br>




