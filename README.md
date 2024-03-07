# Database-SQL-and-Data-Collection-for-Data-Science
## 2/3/2024: Buổi học 1: Giới thiệu về Database và SQL
- Thực hiện viết câu lệnh truy vấn để có được dữ liệu
- Thu thập dữ liệu trên internet (web scraping)
### Giới thiệu về cơ sở dữ liệu 
***Các khái niệm cơ bản***
- Dữ liệu: văn bản, số, ngày tháng, hình ảnh (thường phục vụ cho machine learning)
- Bảng: dữ liệu lưu trong các bảng, bao gồm các dòng (bản ghi - record) và cột (thuộc tính - attribute)\
- SQL (structure query language): Ngôn ngữ truy vấn có cấu trúc. Thực hiện 4 thao tác chính (CREATE, READ, UPDATE and DELETE): truy vấn (đọc danh sách), chèn, cập nhật (sửa), xoá

Các lệnh như: select from, insert/update/delete

- DBMS: Hệ quản trị cơ sở dữ liệu
### Các loại cơ sở dữ liệu 

Gồm 2 loại chính: Cơ sở dữ liệu quan hệ(Relational Database), csdl không quan hệ (No SQL Database)

***1. Cơ sở dữ liệu quan hệ(Relational Database)***

Trong cơ sở dữ liệu quan hệ, có thể tạo mối quan hệ giữa các bảng.

- Một số Relational Database phổ biến: My SQL, PostgreSQL, SQLite, Microsoft SQL Server, Oracle Database
  
***2. Cơ sở dữ liệu không quan hệ (No SQL Database)***

{...} biểu diễn 1 đối tượng (object)

[...] biểu diễn một danh sách (collection)

### Tổng quan về SQL

***Tầm quan trọng của SQL trong Data Science***

- Data cleaning
- Data exploration: khám phá để phân tích mối quan hệ, insight dữ liệu
- Data transformation
- Feature engineering
- Data integration
- Data visualization and Model evaluation

### Cài đặt cơ sở dữ liệu MySQL

- Chọn phiên bản hỗ trợ theo hdh

## 7/3/2024: Buổi học 3: Basic SQL
### Limit và Order by
- Order by: sắp thứ tự kết quả truy vấn (ASC: sắp xếp tăng, DESC: sắp xếp giảm). thứ tự sắp xếp ưu tiên từ trái sang phải.
- Limit: giới hạn số dòng kết quả truy vấn

### Aggregate Functions

- Hàm count(): đếm. count(*): đếm dòng -> có bao nhiêu dòng trả về bấy nhiêu dòng
- Hàm sum(): tính tổng
- Hàm avg(): tính giá trị trung bình
- Hàm min và max(): tính tổng

### Group by, Having
- Group by: truy vấn có nhóm
- Thứ tự thưc hiện select:

SELECT

FROM

WHERE

GROUP BY

HAVING

ORDER BY

LIMIT

