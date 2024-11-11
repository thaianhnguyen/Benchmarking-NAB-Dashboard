# So sánh 1 ngân hàng với ngành (Benchmarking)
Xem dashboard trên Power BI tại: [**Dashboard Power BI**](https://app.powerbi.com/view?r=eyJrIjoiNDhmZWUxNzAtZTljNi00MDVhLWFmZTYtMTc4MTgzMDNhNTY3IiwidCI6ImFmMWYzNzUzLTM5MjUtNGU2Zi05NDliLTk3YzAwNzMyMDgwMyIsImMiOjEwfQ%3D%3D&fbclid=IwAR19SyBorqdDhtuXZaKvqBwRLDbzsqN-1SsMNP7veJgnAn43vM0rNTJC4YQ)
---
## Version: [**_English_**](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/README_Eng.md)
Table of contents
=================

<!--ts-->
* [Bài toán và dữ liệu](#Business-scenario-dataset)
* [Làm sạch dữ liệu với Python](#Data-cleaning)
* [Trực quan_hóa](#Visualization)
   * [Insights](#insights)
   * [Chi tiết](#details)
       * [Vị thế thị trường](#market-position)
       * [Khả năng sinh lời](#profitability)
       * [Chất lượng tài sản](#asset)<!--te-->
<a name="Business-scenario-dataset"/> </br>
## Bài toán và dữ liệu
Với dự án này, tôi mong muốn có thể phân tích dữ liệu báo cáo tài chính của ngành ngân hàng trong vòng 5 năm qua để so sánh hiệu suất của một ngân hàng với ngành, từ đó rút ra những thông tin hữu ích về điểm mạnh, điểm yếu, cũng như cơ hội tăng trưởng và thách thức trong tương lai.

Ngân hàng benchmarked được chọn ngẫu nhiên: Ngân hàng Nam Á - NAB.

Dữ liệu báo cáo tài chính của các ngân hàng thương mại trong giai đoạn 2018-2023 được thu thập thông qua nền tảng [FiinPro](https://fiinpro.com/fiinpro-x)
<a name="Data-cleaning"/> </br>
## Data cleaning  

Dữ liệu ở dưới dạng file excel, theo format tài chính - dữ liệu dạng bảng. 
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/data.jpg)</br>

Thư viện sử dụng:</br>
- os, openpyxl: truy cập đường dẫn folder và file excels. </br>
- panda, re: biến đổi cấu trúc dữ liệu thành long-format phù hợp với phân tích; làm sạch tên cột, dữ liệu. </br>
- numpy, seaborn: biến đổi số học dữ liệu và tạo chart để khai phá dữ liệu tại một số cột </br>

Xem thêm về quá trình xử lý bằng Python tại: [Python Script](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/clean%20bank%20data.ipynb)

<a name="Visualization"/> </br>
## Trực quan hóa dữ liệu: </br> <a name="insights"/> </br>
### Insights:
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/Slide_Vie.JPG) </br>
### Chi tiết: <a name="details"/> </br>
### Vị thế thị trường: <a name="market-position"/> </br>
- Theo số liệu năm 2023, doanh thu, lợi nhuận NAB còn nằm ở nhóm thấp trong nhóm ngân hàng có quy mô tài sản trung bình (từ 100k tỷ đến 500k tỷ). Tuy vậy, tỉ lệ tăng trưởng quy mô tài sản lẫn doanh thu/ lợi nhuận đều chạm hoặc cao hơn mức TB ngành/nhóm NH cùng quy mô.
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/mkt_position_1.jpg)</br>

- Thị phần về huy động và tài sản của NAB cũng đã tăng trưởng đáng kể so với giai đoạn năm 2018. Tuy nhiên, 3 năm gần đây thị phần có chững lại hay thậm chí tăng trưởng âm → Điều này có thể hạn chế tiềm năng tăng trưởng của NAB về hoạt động tín dụng
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/mkt_2.jpg)</br>

- Nhìn vào cơ cấu huy động của NAB, tiền gửi không kì hạn (CASA) đang chiếm tỷ lệ rất thấp so với TB ngành. Đây lại là nguồn huy động với lãi suất rất thấp → cho thấy chi phí vốn của NAB cao hơn so với ngành, làm giảm biên lợi nhuận của ngân hàng này. </br>
![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/mk_position_3.jpg)</br>

### Khả năng sinh lời: <a name="profitability"/> </br>
- Các chỉ số sinh lời còn khiêm tốn so với TB ngành, tuy nhiên có sự cải thiện dần ở từng năm và đã tiệm cận với TB ngành vào năm 2023.
    - 1 động lực có thấy được cho việc này chính là từ việc NAB ngày càng kiểm soát chi phí tốt hơn trong những năm qua
</br>

![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/profit_1.jpg)</br>

### Chất lượng tài sản: <a name="asset"/> </br>
- Chất lượng tài sản của NAB đang ở mức tốt khi mà tỷ lệ CAR và LDR đều đang trong ngưỡng an toàn cho phép của NHNN và tỷ lệ nợ xấu của NAB thấp hơn TB ngành.
- Tuy nhiên, việc LDR ở ngưỡng tối đa cho phép 85% → NAB sẽ cần gia tăng quy mô huy động để có thể gia tăng quy mô tín dụng mà vẫn đảm bảo tỷ lệ thanh khoản
</br>

![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/asset_1.jpg)</br>

- Tỷ lệ bao phủ nợ xấu (PCR) thấp cho thấy NAB đang trích lập dự phòng ít hơn so với tổng dư nợ xấu hiện tại, đánh đổi rủi ro tín dụng lấy lợi nhuận trong ngắn hạn. Trong tương lai, nếu như tỷ lệ nợ xấu không được kiểm soát tốt và các khoản nợ xấu hiện tại không được khắc phục, lợi nhuận của NAB sẽ bị ảnh hưởng nghiêm trọng.
</br>

![alt text](https://github.com/thaianhnguyen/Benchmarking-NAB-Dashboard/blob/main/image/asset_2.jpg)</br>
