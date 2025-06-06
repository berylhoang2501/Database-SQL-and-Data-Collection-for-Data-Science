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

- DML(Data Manipulation Language): sử dụng để thực hiện các thay đổi trong bảng dữ liệu trong cơ sở dữ liệu. Các lệnh DML bao gồm INSERT, UPDATE và DELETE

- DDL(Data Definition Language): sử dụng để quản lý cấu trúc (phần khung) của cơ sở dữ liệu. Các lệnh DDL bao gồm CREATE (tạo), ALTER
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
- Cú pháp:
  
SELECT */tên cột hoặc các cột

FROM Tên bảng

WHERE điều kiện lọc dòng;

***1. Kết hợp các điều kiện: AND và OR***

***2. Phủ định điều kiện: NOT***

***3. So sánh: =, !=, >, >=, <, =<***

***4. Toán tử: IN và BETWEEN***

between điểm bắt đầu and điểm kết thúc

***5. So sánh gần đúng: LIKE***

%: không có ký tự hoặc có các ký tự bất kỳ 

_:có đúng một ký tự

- So sánh với null. lưu ý đối với so sánh null phải sử dụng is null chứ không được sử dụng = null

## 7/3/2024: Buổi học 3: Basic SQL
### Limit và Order by

- Order by: sắp thứ tự kết quả truy vấn (ASC: sắp xếp tăng, DESC: sắp xếp giảm). thứ tự sắp xếp ưu tiên từ trái sang phải theo câu lệnh truy vấn. mặc định là sắp xếp tăng

- Limit: giới hạn số dòng kết quả truy vấn

limit[bỏ qua n dòng đầu tiên, lấy n dòng tiếp theo]

- Cú pháp:

SELECT */tên cột 

FROM Tên bảng

WHERE điều kiện lọc dòng 

ORDER BY cột sắp thứ tự [ASC|DESC]

LIMIT số dòng giới hạn [OFFSET số dòng bỏ qua]; 

### Aggregate Functions (các hàm dùng để thống kê)

- Hàm count(): đếm. count(*): đếm dòng -> có bao nhiêu dòng trả về bấy nhiêu dòng

count(distinct _ )

- Hàm sum(): tính tổng
- Hàm avg(): tính giá trị trung bình
- Hàm min và max(): tính tổng

### Group by, Having
- Group by: truy vấn có nhóm
- Thứ tự thưc hiện select:

SELECT

FROM

WHERE

GROUP BY Cộtnhóm/Biểuthứcnhóm

Những cột nào không thực hiện thống kê tính toán trên cột đó thì phải được khai báo vào group by

HAVING [điều kiện lọc nhóm]

lưu ý: khi đã có sự xuất hiện của having thì chắc chắn phải có group by, nhưng điều này không có nghĩa ngược lại

ORDER BY

LIMIT

### Built-in Functions
***1. Nhóm hàm về chuỗi (String
Functions)*** 

Ví dụ: hàm UPPER(), LOWER(), CHAR_LENGTH ('') 

***2. Nhóm hàm về số
(Numeric Functions)*** 

Ví dụ: hàm ABS(),POW()

***3. Nhóm hàm về ngày (Date Functions)*** 

Ví dụ: hàm CURRENT_DATE(), CURRENT_TIME()

DATE_ADD(date, INTERVAL 1 DAY): Thêm một ngày vào ngày date.

DATE_SUB(date, INTERVAL 1 WEEK): Trừ một tuần khỏi ngày date.

https://www.w3schools.com/mysql/mysql_ref_functions.asp

https://www.w3schools.com/sql/func_mysql_date_format.asp

## 9/3/2024: Buổi học 4: Advanced SQL

### Sub Query 

- Chức năng: là câu lệnh truy vấn con  (sub query) , dùng để hỗ trợ câu lệnh truy vấn chính (main query). 

Truy vấn con (inner query) luôn thực hiện trước truy vấn chính (outer query) và trả về kết quả cho truy vấn chính. sub query phải được viết trong cặp ngoặc đơn

- Thứ tự:
SELECT

FROM

WHERE <biểu thức> <toán tử so sánh> (Truy vấn con)

- 3 trường hợp trả về của sub query:

***Trả về 1 giá trị (1 dòng)***

sử dụng toán tử so sánh 

***Trả về 1 cột các giá trị (1 cột nhiều dòng)***

sử dụng toán tử so sánh in

***Trả về nhiều cột nhiều dòng***

Dùng để làm nguồn cho câu lệnh truy vấn khác (Đặt tên cho dữ liệu trả về của sub query 1 cái tên tạm)

### Query in Multiple Table

***Sử dụng phép toán kết hợp - JOIN***

3 cách Dùng để kết hợp dữ liệu giữa hai bảng

- INNER JOIN: phép kết bằng. chọn các dòng dữ liệu khớp trong cả 2 bảng. không bắt buộc thứ tự của các bảng

- OUTER JOIN: phép kết ưu tiên. các nào khai báo trước sẽ được ưu tiên trước. coi chữ join là tâm, phân chia thành 2 trường hợp ở dưới:

LEFT OUTER JOIN

RIGHT OUTER JOIN

- CROSS JOIN: phép kết chéo. chọn tất cả các dòng của 2 bảng

![z5228694410812_da07a9dc0baa313055a00c42feecb365](https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/4312aba7-5e8d-47b5-8270-06e40b733cc0)

Cú pháp:

SELECT */ tên cột

FROM Bảng A ACROS JOIN Bảng B;

<img width="557" alt="Ảnh màn hình 2025-05-26 lúc 13 19 57" src="https://github.com/user-attachments/assets/75d95051-69f6-42f0-a281-8b140328fd92" />


### UNION

- Dùng để kết hợp hai bộ kết quả của hai truy vấn SELECT với nhau.
- kết hợp theo vị trí cột thay vì tên cột

***1. Union***

loại bỏ những giá trị trùng 

![Ảnh màn hình 2024-03-09 lúc 23 50 33](https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/c0c0b2fa-8604-4df1-a0e7-80652229c52a)

***2. Union all***

lấy luôn cả giá trị trùng 

![Ảnh màn hình 2024-03-09 lúc 23 50 57](https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/5409fa19-37f1-4f0e-8c84-3fc97d1c6be8)

## 10/3/2024: Buổi học 5: Advanced SQL

### CTE (common table expression)

- là cách đặt tên cho truy vấn con (trong câu truy vấn chính) bằng từ khóa WITH
- cú pháp:

<img width="636" alt="Ảnh màn hình 2024-03-19 lúc 00 01 51" src="https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/70d2023c-8cc3-4c16-bdaf-238e2d488020">

### View

- View tạo ra từ câu truy vấn →View cũng được xem là bảng ảo (virtual table)

- View cung cấp dữ liệu như một bảng
SELECT *FROM <tên view>

### Window Functions

sử dụng các hàm tính toán và các hàm tính toán dựa trên tập hợp các dòng (subset ~window) mà vẫn giữ nguyên các dòng

Cú pháp chung:

<img width="1082" alt="Ảnh màn hình 2024-03-23 lúc 20 28 06" src="https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/3300ada2-7a24-4003-8d3d-36de09ef3771">

***1. Hàm ROW_NUMBER()***
- Chức năng: dùng đánh số thứ tự 
- order by: SELECT ROW_NUMBER OVER(ORDER BY SALARY DESC) 
- phân nhóm PARTITION: SELECT ROW_NUMBEROVER(PARTITION BY DEPARTMENT_ID ORDER BY SALARY DESC) 

***2. Hàm RANK()***
- Chức năng: xếp hạng
- order by: SELECT RANK() OVER(ORDER BY SALARY DESC) 
- dense_rank(): khác hàm rank ở chỗ sau khi xếp xong những người đồng hạng thì vẫn đánh số thứ tự tiếp nối chứ không bỏ qua bất kì số nào như hàm rank

***3. Hàm NTILE(n)***
- Chức năng: chia n nhóm
- order by: SELECT NTILE(20) OVER(ORDER BY SALARY)

***4. Aggregate functions***

## 14/3/2024: Buổi học 6: Truy cập Database từ Python
### Tổng quan
***Ưu điểm của Python khi làm việc với database***
- Thích hợp với các ứng dụng bóc tách, chuyển đổi, phân tích dữ liệu: big data - data mining
- Python có nhiều thư viện hỗ trợ trong việc xử lý dữ liệu: NumPy, Pandas, Matplotlib, Seaborn, SciPy,...

***Mô hình truy cập DB:***
- Python truy cập đến DB thông qua việc gọi các API (Application Programming Interface) tương ứng với mỗi loại DB
- API cung cấp nhiều hàm (có thể gọi) để truy cập vào các hệ quản trị CSDL nhằm đọc và xử lý dữ liệu

***Hoạt động cơ bản của DB APIs:***

<img width="545" alt="Ảnh màn hình 2024-03-15 lúc 16 56 17" src="https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/4cef7f7d-cc6a-4597-b78b-f0291d79548d">

- connect

- send là bước tạm ghi nhận 

- execute(): yêu cầu thực thi câu lệnh truy vấn

- status check()

- ok: phản hồi kết quả của 4 câu lệnh trên

- disconnect(): ngắt phiên làm việc với database

***DB APIs được sử dụng trên một số DBMS phổ biến:***
  
<img width="656" alt="Ảnh màn hình 2024-03-15 lúc 17 33 33" src="https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/cfd6d079-3efe-4304-8a70-42ca58faaf30">

### Thư viện truy cập Database DB-API
***1. Sử dụng DB-API***
- DB-API là thư viện chuẩn của Python dùng để truy cập cơ sở dữ liệu quan hệ.
- DB-API cho phép Python truy cập đến bất kỳ loại cơ sở dữ liệu quan hệ nào

***2. Một số thư viện thường dùng để kết nối:***

<img width="635" alt="Ảnh màn hình 2024-03-15 lúc 17 41 24" src="https://github.com/berylhoang2501/Database-SQL-and-Data-Collection-for-Data-Science/assets/152646327/3081d4db-4158-46c7-a120-0c8f6bbe4e6c">

***3. Các đối tượng chính trong Python DB API:***

**Đối tượng Connection:** Thực hiện kết nối đến Database, Quản lý các phiên (session) làm việc

Các phương thức của Connection:

- cursor(): trả về 1 đối tượng cursor (sử dụng cursor để thực hiện lệnh)

- commit(): dùng để cập nhật các thay đổi về Database

- rolback(): undo

- close(): ngắt kết nối với database

**Đối tượng Cursor:** Cursor được tạo ra từ Connection, Cursor cho phép thực hiện các truy vấn dữ liệu (thông qua Connection)

Các phương thức của Cursor:

- execute(): thực hiện câu truy vấn, đi tìm dòng câu lệnh truy vấn để đọc ra

- fetchone(): trả về dòng tiếp theo trong tập kết quả. Nếu đọc không có dòng thì trả về None

- fetchmany([numRows]): trả về số dòng được chỉ định. Nếu không còn dòng nào sẽ trả về rỗng, mặc định numRows = 1

- fetchall(): trả về tất cả các dòng (giống select *)

- close(): đóng cursor

***4. Thực hiện câu truy vấn có truyền tham số***

### Kết nối MySQL Database từ Python

### Magic SQL

### Lưu kết quả truy vấn vào DataFrame

# 16/3/2024: PostgreSQL, SQLite (mở rộng)

- data directory: /Library/PostgreSQL/16/data

**MySQL:**

=> Port: 3306

=> IDE: MySQL Workbench

=> Account: root - Beryl/1983

**PortgreSQL:**

=> Port: 5432

=> IDE: pgAdmin4

=> Account: postgres - Beryl/1983

Lỗi Restore => File => References => Paths => Binary paths => Browse đến thư mục bin của PostgreSQL  => Chọn phiên bản PostgreSQL phù hợp

- Làm việc trên Python: pip3 install psycopg2

**Trình tự:**

Kết nối => conn

cursor

execute

close

# 17/3/2024: Buổi học 8: FugueSQL
## Giới thiệu FugueSQL

- được thiết kế cho người dùng SQL với dữ liệu lớn (big data).

- FugueSQL đc dùng để xử lý phía client (các tập tin ngay trên máy mình)

- cho phép thể hiện logic cho quy trình công việc tính toán phân tán end-to-end.

- có thể được kết hợp với mã Python để sử dụng các lệnh SQL.

- hỗ trợ xử lý phân tán dữ liệu trên nhiều máy và có khả năng mở rộng (scale-out) để xử ýl lượng dữ liệu lớn.

- cung cấp khả năng xử ýl dữ liệu phi cấu trúc và có thể tương tác với các nguồn dữ liệu đa dạng như JSON, Parquet, csv,...

- cung cấp một giao diện thống nhất, cho phép cùng một mã SQL chạy trên Pandas, Dask và Spark.

**Cài đặt FugueSQL:**

MacOS: pip3 install "fugue[sql]"


## Đọc/Ghi dữ liệu từ tập tin 

***1. Phân loại tập tin***

- Tập tin có định dạng CSV:

- Tập tin có định dạng Parquet: hỗ trợ xử lý phân trang, khi dữ liệu nhiều quá thì chia trang web để đọc 

***Tóm tắt nội dung học***

- Ghi tập tin: SAVE OVERWRITE

- Đọc tập tin: LOAD

- Thực hiện câu lệnh truy vấn:

    + Dùng dataframe để làm nguồn cho câu lệnh truy vấn

    + Đọc tập tin và truy vấn trực tiếp từ tập tin đã đọc (không có mệnh đề FROM)

## Truy vấn dữ liệu

- infer_schema=true dùng để xác định thêm kiểu dữ liệu lúc hiển thị 

## Aggregate Functions và WindowFunctions (áp dụng những chức năng tính toán thống kê)

## Hàm tự định nghĩa
