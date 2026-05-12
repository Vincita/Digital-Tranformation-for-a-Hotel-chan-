# Digital Transformation for Hotel Operations

## 1. Tổng quan dự án
Dự án xây dựng hệ thống phân tích vận hành khách sạn dựa trên dữ liệu booking thực tế.  
Mục tiêu là hỗ trợ doanh nghiệp theo dõi doanh thu, hiệu suất phòng, nguồn booking và tình hình thanh toán thông qua dashboard trực quan trong Power BI.

Dự án tập trung vào:
- Chuẩn hóa dữ liệu booking thực tế
- Xây dựng Data Warehouse theo mô hình Star Schema
- Hỗ trợ theo dõi hoạt động vận hành khách sạn theo thời gian thực
- Tạo dashboard phục vụ Operational Intelligence

---

## 2. Dataset
Dataset bao gồm dữ liệu booking khách sạn với các nhóm dữ liệu chính:

### Booking Information
- Mã đặt phòng
- Tên khách hàng
- Ngày check-in / check-out
- Số đêm lưu trú
- Trạng thái booking
- Số hóa đơn

### Room Information
- Tên phòng
- Loại phòng
- Giá trung bình

### Revenue & Payment
- Doanh thu phòng
- Doanh thu dịch vụ
- Tổng doanh thu
- Tiền mặt
- Thẻ tín dụng
- Chuyển khoản
- Công nợ
- Khoản còn thiếu

### Booking Channel
- Online
- OTA
- Walk-in
- Công ty
- Các nguồn booking khác

---

## 3. Quy trình xử lý dữ liệu

### Data Cleaning
- Làm sạch dữ liệu NULL
- Chuẩn hóa tên khách hàng
- Chuẩn hóa tên channel
- Loại bỏ khoảng trắng dư thừa
- Chuyển đổi dữ liệu tiền tệ sang numeric
- Chuẩn hóa định dạng ngày tháng

### Data Warehouse Modeling
- Xây dựng mô hình Star Schema
- Thiết kế:
  - fact_booking
  - dim_customer
  - dim_room
  - dim_roomtype
  - dim_channel
  - dim_date

### ETL Process
- Load dữ liệu vào staging table
- Transform dữ liệu bằng SQL
- Mapping khóa ngoại giữa fact và dimension tables

### Dashboard Development
- Xây dựng dashboard Power BI
- Thiết kế KPI và biểu đồ vận hành
- Tạo slicer filter theo:
  - thời gian
  - loại phòng
  - booking channel

---

## 4. Insight chính

### Revenue Analysis
- Tổng doanh thu đạt hơn 941 triệu
- Doanh thu tập trung chủ yếu ở kênh booked_ctv và online
- Doanh thu cao nhất nằm ở nhóm phòng STD-PNL và DELUXE-PNL

### Room Performance
- Tổng số booking: 734
- Tổng số đêm lưu trú: 1,535
- Giá phòng trung bình khoảng 582K
- Một số phòng có tần suất sử dụng cao hơn đáng kể

### Customer Analysis
- Xác định nhóm khách hàng lưu trú nhiều nhất
- Theo dõi khách hàng mang lại doanh thu cao

### Payment Analysis
- Chuyển khoản là hình thức thanh toán phổ biến nhất
- Một số channel có tỷ lệ công nợ cao hơn các kênh khác

---

## 5. Dashboard Features

### Hotel Operations Overview
- Total Revenue
- Total Bookings
- Average Room Rate
- Total Nights Stayed
- Monthly Revenue Trend
- Revenue by Room Type
- Revenue by Booking Channel
- Bookings by Room

### Hotel Operations Performance
- Top Customers by Revenue
- Top Customers by Nights Stayed
- Payment by Channel
- Payment Method Breakdown

---

## 6. Công cụ sử dụng
- SQL Server
- Microsoft Azure
- Power BI
- DataGrip
- Data Warehouse Modeling
- Star Schema
- ETL Process

---

## 7. Thực hiện
- Người thực hiện: Nguyễn Đinh Việt Thắng
- Thời gian thực hiện: 05/2026

---

## Lưu ý
Đây là dự án cá nhân nhằm thực hành:
- Data Engineering
- Data Warehouse
- Business Intelligence
- Operational Intelligence

Dữ liệu sử dụng là dữ liệu booking thực tế phục vụ mục đích học tập và nghiên cứu.
