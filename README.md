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
## 3/3/2024: Buổi học 2: Basic SQL

Có thể chia SQL ra làm 4 nhóm lệnh

- SELECT FROM (Query): được sử dụng để truy vấn dữ liệu từ cơ sở dữ liệu, để lấy thông tin từ một hoặc nhiều bảng dữ liệu và hiển thị kết quả theo yêu cầu

- DML(Data Manipulation Language): sử dụng để thực hiện các thay đổi trong bảng dữ liệu trong cơ sở dữ liệu. Các lệnh DML bao
gồm INSERT, UPDATE và
DELETE

- DDL(Data Definition Language): sử dụng để quản lý cấu trúc (phần khung) của cơ sở dữ liệu. Các lệnh
DDL bao gồm CREATE (tạo), ALTER
(sửa) và DROP (xóa) 

- DCL(Data Control Language):  quản lý quyền truy cập và an toàn dữ liệu trong cơ sở dữ liệu.

Trong khoá học này chỉ tập trung lệnh SELECT FROM và 1 ít lệnh DML. 

### Data Type
***1. Kiểu số***
- BIT: 0 hoặc 1 (Boolean)
- SMALLINT: số nguyên 2 bytes, từ -32768 đến +32767
- INTEGER (INT): số nguyên 4 bytes, từ -2147483648 đến +2147483647
- BIGINT: số nguyên 8 bytes, ừt -9223372036854775808 đến +9223372036854775807
- FLOAT: số thực 4 bytes, từ -7.2E+75 đến 7.2E+75 
- DOUBLE: số thực 8 bytes (giống float nhưng lưu trữ được nhiều hơn)

***2. Kiểu chuỗi***
- CHAR(n): Chuỗi có độ dài cố định n bytes (với n từ 1 255) (ví dụ: có thể dùng để lưu trữ tuổi)
- VARCHAR(n): Chuỗi có độ dài khác nhau với tối đa n bytes
(với n từ 1→ 65535) (ví dụ: có thể dùng để lưu trữ họ và tên)

2 kiểu sau naỳ giống với 2 kiểu trc, chỉ khác ở chỗ sẽ đổi thành chuỗi nhị phân trước khi lưu trữ.

- BINARY(n): Chuỗi nhị phân có độ dài cố định n bytes (với n
từ 1 → 255)
- VARBINARY(n): Chuỗi nhị phân có độ dài khác nhau với tối
đa nbytes (với ntừ 1→65535)

***3. Kiểu ngày giờ***
- DATE: Kiểu ngày với 3 giá trị năm, tháng, ngày (từ 0001- 01-01 đến 9999-12-31)
- TIME: Kiểu giờ với 3 giá trị giờ, phút, giây (từ 00.00.00
đến 24.00.00)
- TIMESTAMP: giống 2 kiểu trên nhưng thêm vào micro giây

***4. Kiểu dữ liệu lớn (LOB large object)***

### SELECT FROM
- Chức năng: Truy vấn dữ liệu từ bảng
- Cú pháp:

SELECT */tên cột hoặc các cột

FROM Tên bảng;

- từ khoá distinct: dùng để loại bỏ dữ liệu trùng lắp

### WHERE
- Chức năng: dùng để lọc dữ liệu cho bảng
- Cú pháp
SELECT */tên cột hoặc các cột

FROM Tên bảng

WHERE điều kiện lọc dòng;

***1. Kết hợp các điều kiện: AND và OR***
***2. Phủ định điều kiện: NOT***
***3. So sánh: =, !=, >, >=, <, =<***
***4. Toán tử: IN và BETWEEN***
***5. So sánh gần đúng: LIKE***
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

