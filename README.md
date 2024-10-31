# So sánh 1 ngân hàng với ngành (Benchmarking)
The report has been published on Power BI service at here: [**_SALE REPORT_**](https://app.powerbi.com/view?r=eyJrIjoiNDhmZWUxNzAtZTljNi00MDVhLWFmZTYtMTc4MTgzMDNhNTY3IiwidCI6ImFmMWYzNzUzLTM5MjUtNGU2Zi05NDliLTk3YzAwNzMyMDgwMyIsImMiOjEwfQ%3D%3D&fbclid=IwAR19SyBorqdDhtuXZaKvqBwRLDbzsqN-1SsMNP7veJgnAn43vM0rNTJC4YQ)
---

Table of contents
=================

<!--ts-->
* [Bài toán và Dữ liệu](#Business-scenario-dataset)
* [Làm sạch dữ liệu với Python](#Data-cleaning)
* [Visualization](#Visualization)
   * [Overview Page](#overview-page)
   * [Sales by Product/Region](#Product-region)
   * [Customer Analysis](#Customer-analysis)
* [Insights](#Insights)
<!--te-->
<a name="Business-scenario-dataset"/> </br>
## Bài toán và dữ liệu
---

Tôi muốn thực hiện 1 báo cáo có thể so sánh hiệu quả hoạt động của một ngân hàng bất kì với các ngân hàng trong ngành, từ đó có thể thấy được điểm mạnh, điểm yếu và cơ hội của ngân hàng đó.
I want to know how well a bank is doing compared to the industry, ....

Ngân hàng so sánh được lựa chọn bất kì: Ngân hàng Nam Á Bank- NAB
The benchmarked bank is randomly selected: Nam Á Bank - NAB.

Data used is the financial statements of all commercial banks over the period of 2018-2023, acquired through the platform [FiinPro](https://fiinpro.com/fiinpro-x)

<a name="Data-cleaning"/> </br>
## Data cleaning  

The data is in form of excels file and structured in conventionally financial wide format - panel data. 

Dữ liệu ở dưới dạng file excel, theo format tài chính truyền thống - dữ liệu dạng bảng. 
Tôi sử dụng các thư viện os, openpyxl để có thể truy cập các file excel và import thành dataframe. Sau đó sử dụng panda để chỉnh sửa cấu trúc dữ liệu, làm sạch dữ liệu
Khó khăn:
- Dữ liệu ở dạng bảng, các cột là các chỉ tiêu tài chính trải theo chiều thời gian (năm, quý). </br>


The library used:</br>
- os, openpyxl: to access folder directory and excel files
- panda, re: to convert data into long-format structure for analysis purposes and clean data . </br>
- numpy, seaborn: perform mathematic data transformations and EDA </br>

Thư viện sử dụng:</br>
- os, openpyxl: truy cập đường dẫn folder và file excels. </br>
- panda, re: biến đổi cấu trúc dữ liệu thành long-format phù hợp với phân tích; làm sạch tên cột, dữ liệu. </br>
- numpy, seaborn: biến đổi số học dữ liệu và tạo chart để khai phá dữ liệu tại một số cột </br>

<a name="Visualization"/> </br>
## Visualization:

đã khiến $\color{rgb(31,119,180)}{\textsf{tăng 20%}}$	

<a name="Overview-page"/> </br>
### Overview page:
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_2.jpg)</br>
The page provides the user with a big picture of sales performance via some important KPIs over the last year. Generally speaking, it seemed the company saw great growth compared to the previous year (except for the last quarter, September specifically). 
However, it lacked insightful information in terms of regional and product-wise sales. That is why I created the second page:

<a name="Product-region"/> </br>
### Sales by Product/Sale
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_3.jpg)</br>
For this page, I hope that the users can gain insights about sales for a specific region or for a specific product category, or both. That is why I created two 2 simultaneous slicers and also edit the interaction between certain visuals to be "Filter". For example, the user want to now the sales and top 10 product categories sold in Bahia:</br>
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_4.jpg)</br>
Or how much Art-labeled products was selling in Rio de Janeiro:</br>
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_5.jpg)</br>
Lastly, I address the sales manager's requirement regarding customer insight in the third page:

<a name="Customer-analysis"/> </br>
### Customer Analysis:
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_8.jpg)</br>
For this page, I want to show how many customers are returning for a second purchase, how positive their reviews are and how on-time our delivery is. I also included the segmentation of customers based on RFM analysis that I conducted with SQL [**here**](https://github.com/thaianhnguyen/RFM-analysis-with-SQL/blob/main/rfm%20read%20me.md).

_The highlight of this page, firstly, is the cohort analysis of returning customer_. This gives us insights of how many new customers are returning for the subsequent months. For example, we can see that for January 2018, there are 6838 new customers, only 23 of who return in the February and 25 of who return in March and so on.</br>
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_9.jpg)</br>

_The second highlight is that the manager can decide the period, based on which retention rate are calculated_. For example, retention rate with a period of 6 months would mean a returning customer is one that has made repeated purchase for the last 6 months. 

The last page is a decompostion tree visual, which should deepen insights about what total sales are made of, across dimensional variables, which are State, Product Category and Date here. </br>
![alt text](https://github.com/thaianhnguyen/Sales-Report-for-E-commerce-Company/blob/main/images%20BI/Screenshot_7.jpg)</br>

<a name="Insights"/> </br>
## Insights
- Sales this year has seen an great increase in all aspects, compared to last year. This is a good sign.
- Top selling product categories are beauty products and watches gifts while the top 3 states are Sao Paulo, Rio de Janeiro and Minas Gerais, the first of which triples the other two.
- However, the retention rate is alarmingly low, compared to the expected ratio of 15-30% in e-commerce industry. And it seems it is not the sellers, but __the logistics__, to be blamed:
   - The reason might not be the product quality as the CSAT ratio is greater than 75% (even for churn customer segment). 
   - The on time delivery rate is not good (below 95%).
   - The average delivery days increases and on time delivery rate decreases for the "likely to churn" and "churn" segment. </br> 
Therefore, it might be useful conducting further analysis into the correlation between late delivery and retention rate.
- The "middle" segment is witnessing drastic decreases in sales for the past 6 months. It's worth giving more attention to these customers.

This is the end of my blog. I hope with my report, the sales manager can draw useful insights that are actionable. 



Thank you for reading my blog.
