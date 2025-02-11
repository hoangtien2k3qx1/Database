![JDBC](https://images.viblo.asia/e832d1ef-84d2-4d48-bc1f-a2e933bf07e6.png)

[**Tài Liệu Tham Khảo (SQL Server)**](https://hoc.tv/hoc-sql-server)

![](https://images.viblo.asia/d1aba5c0-21a2-4b37-9f71-629d1dc9c782.png)

## Những Kiến Thức Cơ Bản Cần Học Trong Sql Server:

### [Cơ bản về SQL]()
	SQL là gì
	Các khái niệm RDBMS
	Database là gì
	Cú pháp SQL cơ bản
	Kiểu dữ liệu
	Toán tử
	Biểu thức (Expression)

### [SQL Database]()
	Lệnh Create Database
	Lệnh Drop Database
	Lệnh Select Database
	Lệnh Rename Database
	
### [SQL Table]()
	Lệnh Create Table
	Lệnh Drop Table
	Lệnh Delete Table
	Lệnh Rename Table
	Lệnh Truncate Table
	Lệnh ALter Table
	Sao chép bảng
	Bảng tạm (Temp Table)
	
### [Nhóm lệnh thao tác cơ bản]()
	Truy vấn Update
	Truy vấn Insert
	Truy vấn Select
	Mệnh đề Order By
	Mệnh đề Group By
	Từ khóa Distinct
	Sắp xếp kết quả
	
### [Mệnh đề trong SQL]()
	Mệnh đề Where
	Mệnh đề AND & OR
	Mệnh đề WITH
	Mệnh đề Like
	Mệnh đề Top
	
### [Hoạt động SQL nâng cao]()
	Mệnh đề Union
	Giá trị NULL
	Cú pháp Alias
	Chỉ mục (Index)
	Sử dụng View
	Mệnh đề Having
	SQL Transaction
	Toán tử Wildcard
	Truy vấn con
	Sử dụng Sequence
	Xử lý bản sao
	SQL Injection
	
### [Ràng buộc trong SQL]()
	Ràng buộc (Constraint)
	Ràng buộc NOT NULL
	Ràng buộc DEFAULT
	Ràng buộc UNIQUE
	Ràng buộc PRIMARY KEY
	Ràng buộc FOREIGN KEY
	Ràng buộc CHECK
	Ràng buộc INDEX
	
### [SQL Join]()
	Sử dụng Join
	Inner Join
	Left Join
	Right Join
	Full Join
	Self Join
	Cartesian Join
	
### [Hàm trong SQL]()
	Hàm hữu ích
	Hàm xử lý Date
	Hàm xử lý chuỗi
	Hàm xử lý số


# GIỚI Thiệu Cơ Bản Về Sql Server:


## SQL là gì ?
- SQL là viết tắt của Structured Query Language, là ngôn ngữ truy vấn mang tính cấu trúc.
- SQL là ngôn ngữ cơ sở dữ liệu, được sử dụng để tạo, xóa trong cơ sở dữ liệu, lấy các hàng và sửa đổi các hàng, …


## RDBMS là gì ?
- RDBMS là viết tắt của Relational Database Management System ((Hệ thống quản lý cơ sở dữ liệu quan hệ)).

## Bảng (Table) là gì ?
- RDBMS Database sử dụng các bảng để lưu trữ dữ liệu.
- Một bảng là một tập hợp các dữ liệu có liên quan và chứa các hàng và các cột để lưu dữ liệu.

```Sql
    +----+---------+-----+-----------+---------+
    | ID |  TEN    | TUOI|  KHOAHOC  | HOCPHI  |
    +----+---------+-----+-----------+---------+
    |  1 | Hoang   |  21 | CNTT      | 4       |
    |  2 | Viet    |  19 | DTVT      | 3.0     |
    |  3 | Thanh   |  18 | KTDN      |  4      |
    |  4 | Nhan    |  19 | CK        |   4.5   |
    |  5 | Huong   |  20 | TCNH      |   5     |
    +----+---------+-----+-----------+---------+
```

## Field (Trường) là gì ?
Trường, là một thực thể nhỏ nhất của bảng, chứa thông tin cụ thể về mỗi bản ghi trong bảng.

Ví Dụ:
  - trường trong bảng sinh viên là id, ten, tuoi, khoahoc, hocphi.

## Hàng hoặc bản ghi là gì ?
- Một hàng của một bảng cũng được gọi là bản ghi.
- Nó chứa thông tin cụ thể về một entry riêng rẽ trong bảng.
- Hàng là một thực thể nằm ngang trong bảng.

Ví Dụ:
```Sql
    +----+----------+-----+-----------+----+
    |  1 | Hoang    |  21 | CNTT    |  4   |
    +----+----------+-----+-----------+----+ 
```

## Column (cột) là gì ?
- Một cột, là một thực thể dọc trong bảng, chứa tất cả thông tin được liên kết với một trường cụ thể trong một bảng.

Ví Dụ:
```html
                  +-----------+
                  | TEN       |
                  +-----------+
                  | Hoang     |
                  | Viet      |
                  | Thanh     |
                  | Nhan      |
                  | Huong     |
                  +-----------+
```

## Giá trị NULL là gì ?
- Giá trị NULL của một bảng xác định rằng trường đã bị để trống trong khi tạo bản ghi.

## Ràng buộc (Constraint) trong SQL ?
- Ràng buộc (Constraint) là các qui tắc cho các cột dữ liệu trong bảng.

Dưới đây là các Ràng buộc (Constraint) được sử dụng phổ biến có sẵn trong SQL:
- Ràng buộc [NOT NULL]() trong SQL: Bảo đảm một cột không thể có giá trị NULL.
- Ràng buộc [DEFAULT]() trong SQL: Cung cấp một giá trị mặc định cho cột khi không được xác định.
- Ràng buộc [UNIQUE]() trong SQL: Bảo đảm tất cả giá trị trong một cột là khác nhau.
- Ràng buộc [PRIMARY]() Key trong SQL: Mỗi hàng/bản ghi được nhận diện một cách duy nhất trong một bảng.
- Ràng buộc [FOREIGN]() Key trong SQL: Mỗi hàng/bản ghi được nhận diện một cách duy nhất trong bất kỳ bảng nào.
- Ràng buộc [CHECK]() trong SQL: Bảo đảm tất cả giá trị trong một cột thỏa mãn các điều kiện nào đó.
- Ràng buộc [INDEX]() trong SQL: Sử dụng để tạo và lấy dữ liệu từ Database một cách nhanh chóng.


## Toàn vẹn dữ liệu trong SQL ?
- Toàn vẹn dữ liệu (Data Integrity) là việc đặt ra các quy tắc trong một cơ sở dữ liệu nhằm kiểm tra các giá trị của dữ liệu trước khi được lưu trữ phải đảm bảo tính chính xác và hợp lý bên trong một cơ sở dữ liệu.

Dưới đây là một số loại về tính toàn vẹn dữ liệu tồn tại với mỗi RDBMS:
- [Entity Integrity](): Xác định rằng trong một bảng không nên có bản sao các hàng.
- [Domain Integrity](): Bắt buộc các entry hợp lệ cho một cột đã cho bằng cách giới hạn kiểu, định dạng hoặc dãy giá trị.
- [Referential integrity](): Xác định rằng, các hàng/bản ghi không thể bị xóa, mà được sử dụng bởi các hàng/bản ghi khác.
- [User-Defined Integrity](): Áp dụng một số qui tắc được định nghĩa bởi người dùng. Các qui tắc này là khác với các loại toàn vẹn dữ liệu trên.


## Chuẩn hóa cơ sở dữ liệu (Database Normalization) trong SQL ?
- huẩn hóa cơ sở dữ liệu (Database normalization) là tiến trình tổ chức dữ liệu một cách hiệu quả trong một Database.

#### Có hai lý do của tiến trình chuẩn hóa:
- Để loại bỏ các dữ liệu thừa, ví dụ, lưu giữ cùng dữ liệu trong nhiều hơn một bảng.
- Bảo đảm độc lập dữ liệu (dữ liệu liên quan với nhau được đặt trong cùng một bảng).





## Dưới đây là một số câu truy vấn dữ liệu phổ biến trong SQL Server:

#### [SELECT](): Lấy dữ liệu từ cơ sở dữ liệu
```roomsql
SELECT * FROM Customers;
```

#### [WHERE](): Lấy các bản ghi thỏa mãn điều kiện
```roomsql
SELECT * FROM Customers WHERE City = 'Hanoi';
```

#### [ORDER BY](): Sắp xếp các bản ghi theo thứ tự tăng hoặc giảm dần
```roomsql
SELECT * FROM Customers ORDER BY CustomerName ASC;
```

#### [JOIN](): Kết hợp dữ liệu từ hai hoặc nhiều bảng khác nhau dựa trên một điều kiện
```roomsql
SELECT Orders.OrderID, Customers.CustomerName FROM Orders INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

#### [GROUP BY](): Nhóm các bản ghi theo một hoặc nhiều trường
```roomsql
SELECT Country, COUNT(*) FROM Customers GROUP BY Country;
```

#### [HAVING](): Lọc các bản ghi nhóm dựa trên một điều kiện
```roomsql
SELECT Country, COUNT() FROM Customers GROUP BY Country HAVING COUNT() > 5;
```

#### [INSERT INTO](): Thêm bản ghi mới vào bảng
```roomsql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country) VALUES ('Alfreds Futterkiste', 'Maria Anders', 'Obere Str. 57', 'Berlin', '12209', 'Germany');
```

#### [UPDATE](): Cập nhật giá trị cho các bản ghi trong bảng
```roomsql
UPDATE Customers SET ContactName = 'Alfred Schmidt' WHERE CustomerID = 1;
```

#### [DELETE](): Xóa bản ghi từ bảng
```roomsql
DELETE FROM Customers WHERE CustomerID = 1;
```

#### [LIKE](): Lấy các bản ghi thỏa mãn điều kiện đặc biệt với sử dụng phép so sánh chuỗi
```roomsql
SELECT * FROM Customers WHERE City LIKE 'H%';
```

#### [IN](): Lấy các bản ghi mà giá trị của một trường nằm trong danh sách giá trị cho trước
```roomsql
SELECT * FROM Customers WHERE Country IN ('USA', 'Canada');
```

#### [NOT](): Lấy các bản ghi mà không thỏa mãn điều kiện được chỉ định
```roomsql
SELECT * FROM Customers WHERE NOT Country = 'Germany';
```

#### [BETWEEN](): Lấy các bản ghi trong khoảng giá trị cho trước
```roomsql
SELECT * FROM Orders WHERE OrderDate BETWEEN '2022-01-01' AND '2022-12-31';
```

#### [EXISTS](): Kiểm tra xem có bản ghi thỏa mãn câu truy vấn con được chỉ định hay không
```roomsql
SELECT * FROM Customers WHERE EXISTS (SELECT * FROM Orders WHERE Customers.CustomerID = Orders.CustomerID);
```

#### [UNION](): Kết hợp các kết quả của hai hoặc nhiều câu truy vấn SELECT khác nhau vào một bảng
```roomsql
SELECT CustomerName, ContactName FROM Customers UNION SELECT SupplierName, ContactName FROM Suppliers;
```

#### [DISTINCT](): Lấy các giá trị duy nhất từ một trường trong bảng
```roomsql
SELECT DISTINCT Country FROM Customers;
```

#### [MAX và MIN](): Lấy giá trị lớn nhất hoặc nhỏ nhất từ một trường trong bảng
```roomsql
SELECT MAX(Price) FROM Products WHERE CategoryID = 1;
```

#### [COUNT](): Đếm số bản ghi thỏa mãn điều kiện
```roomsql
SELECT COUNT(*) FROM Customers WHERE Country = 'Germany';
```

#### [AVG](): Tính trung bình giá trị của một trường trong bảng
```roomsql
SELECT AVG(Price) FROM Products WHERE CategoryID = 1;
```

#### [SUM](): Tính tổng giá trị của một trường trong bảng
```roomsql
SELECT SUM(Quantity) FROM Orders WHERE CustomerID = 1;
```

#### [GROUP BY WITH ROLLUP](): Nhóm các bản ghi theo một hoặc nhiều trường và tính tổng giá trị của các nhóm
```roomsql
SELECT Country, City, SUM(Quantity) FROM Orders WHERE CustomerID = 1 GROUP BY Country, City WITH ROLLUP;
```

#### [INNER JOIN](): Lấy các bản ghi từ hai hoặc nhiều bảng khác nhau dựa trên một điều kiện, giống như câu lệnh JOIN nhưng chỉ lấy các bản ghi trùng khớp
```roomsql
SELECT Customers.CustomerName, Orders.OrderID FROM Customers INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```

#### [LEFT JOIN](): Lấy tất cả các bản ghi từ bảng bên trái và các bản ghi trùng khớp từ bảng bên phải dựa trên một điều kiện
```roomsql
SELECT Customers.CustomerName, Orders.OrderID FROM Customers LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```

#### [RIGHT JOIN](): Lấy tất cả các bản ghi từ bảng bên phải và các bản ghi trùng khớp từ bảng bên trái dựa trên một điều kiện
```roomsql
SELECT Customers.CustomerName, Orders.OrderID FROM Customers RIGHT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```

#### [FULL OUTER JOIN](): Lấy tất cả các bản ghi từ cả hai bảng, bao gồm các bản ghi trùng khớp và các bản ghi không trùng khớp, dựa trên một điều kiện
```roomsql
SELECT Customers.CustomerName, Orders.OrderID FROM Customers FULL OUTER JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```

#### [CROSS JOIN](): Tạo ra tất cả các cặp bản ghi từ hai bảng, không có điều kiện kết hợp
```roomsql
SELECT * FROM Customers CROSS JOIN Orders;
```

#### [TOP](): Lấy một số bản ghi đầu tiên từ một bảng
```roomsql
SELECT TOP 5 * FROM Customers;
```



# Example Table: 

## dbo.BOMON:

| MABN   | TENBN                 | PHONG | DIENTHOAI    | TRUONGBM | KHOA  | NGAYNHANCHUC |
|--------|-----------------------|-------|--------------|----------|-------|--------------|
| CNTT   | Công nghệ tri thức    | B15   | 0838126126   | NULL     | CNTT  | NULL         |
| CNTT	  | Công nghệ tri thức    | B15	  | 0838126126 	 | NULL	    | CNTT	 | NULL         |
| HHC 	  | Hóa hữu cơ            | B44	  | 0838222222 	 | NULL	    | HH  	 | NULL         |
| HL  	  | Hóa Lý                | B42	  | 0838878787 	 | NULL	    | HH  	 | NULL         |
| HPT 	  | Hóa phân tích         | B43	  | 0838777777 	 | 007	     | HH  	 | 2007-10-15   |
| HTTT	  | Hệ thống thông tin    | B13	  | 0838125125 	 | 002	     | CNTT	 | 2004-09-20   |
| MMT 	  | Mạng máy tính         | B16	  | 0838676767 	 | 001	     | CNTT	 | 2005-05-15   |
| SH  	  | Sinh hóa              | B33	  | 0838898989 	 | NULL	    | SH  	 | NULL         |
| VLĐT	  | Vật lý điện tử        | B23	  | 0838234234 	 | NULL	    | VL  	 | NULL         |
| VLUD	  | Vật lý ứng dụng       | B24	  | 0838454545 	 | 005	     | VL  	 | 2006-02-18   |
| VS  	  | Vi Sinh               | B32	  | 0838909090 	 | 004	     | SH  	 | 2007-01-01   |


## dbo.CHUDE:

| MACD | TENCD                     |
|------|---------------------------|
| NCPT | 	Nghiên cứu phát triển    |
| QLGD | 	Quản lý giáo dục         |
| UDCN | 	Ứng dụng công nghệ       |


## dbo.CONGVIEC:

| MADT   | SOTT   | TENCV                        | NGAYBD                    | NGAYKT                     |
|--------|--------|------------------------------|---------------------------|----------------------------|
| 001 	  | 1	     | Khởi tạo và Lập kế hoạch	    | 2007-10-20 00:00:00.000	  | 2008-12-20 00:00:00.000    |   
| 001 	  | 2	     | Xác định yêu cầu	            | 2008-12-21 00:00:00.000	  | 2008-03-21 00:00:00.000    |   
| 001 	  | 3	     | Phân tích hệ thống	          | 2008-03-22 00:00:00.000	  | 2008-05-22 00:00:00.000    |   
| 001 	  | 4	     | Thiết kế hệ thống	           | 2008-05-23 00:00:00.000	  | 2008-06-23 00:00:00.000    |  
| 001 	  | 5	     | Cài đặt thử nghiệm	          | 2008-06-24 00:00:00.000	  | 2008-10-20 00:00:00.000    |  
| 002 	  | 1	     | Khởi tạo và lập kế hoạch	    | 2009-05-10 00:00:00.000	  | 2009-07-10 00:00:00.000    |  
| 002 	  | 2	     | Xác định yêu cầu	            | 2009-07-11 00:00:00.000	  | 2009-10-11 00:00:00.000    |  
| 002 	  | 3	     | Phân tích hệ thống	          | 2009-10-12 00:00:00.000	  | 2009-12-20 00:00:00.000    |  
| 002 	  | 4	     | Thiết kế hệ thống	           | 2009-12-21 00:00:00.000	  | 2010-03-22 00:00:00.000    |
| 002 	  | 5	     | Cài đặt thử nghiệm	          | 2010-03-23 00:00:00.000	  | 2010-05-10 00:00:00.000    |  
| 006 	  | 1	     | Lấy mẫu	                     | 2006-10-20 00:00:00.000	  | 2007-02-20 00:00:00.000    |  
| 006 	  | 2	     | Nuôi cấy	                    | 2007-02-21 00:00:00.000	  | 2008-09-21 00:00:00.000    |  


## dbo.DETAI

| MADT  | TENDT                                     | CAPQL                   | KINHPHI       | NGAYBD      | NGAYKT         | MACD   | GVCNDT       |
|-------|-------------------------------------------|-------------------------|---------------|-------------|----------------|--------|--------------|
| 001   | 	HTTT quản lý các trường ĐH               | 	ĐHQG                   | 20            | 	2007-10-20 | 	2008-10-20    | 	QLGD  | 	002         |
| 002   | 	HTTT quản lý giáo vụ cho một Khoa        | 	Trường                 | 	20           | 	2000-10-12 | 	2001-10-12    | 	QLGD  | 	002         |
| 003   | 	Nghiên cứu chế tạo sợi Nanô Platin       | 	ĐHQG                   | 	300          | 	2008-05-15 | 	2010-05-15    | 	NCPT  | 	005         |
| 004   | 	Tạo vật liệu sinh học bằng màng ối người | 	Nhà nước               | 	100          | 	2007-01-01 | 	2009-12-31    | 	NCPT  | 	004         |
| 005   | 	Ứng dụng hóa học xanh                    | 	Trường                 | 	200          | 	2003-10-10 | 	2004-12-10    | 	UDCN  | 	007         |
| 006   | 	Nghiên cứu tế bào gốc                    | 	Nhà nước               | 	4000         | 	2006-10-12 | 	2009-10-12    | 	NCPT  | 	004         |
| 007   | 	HTTT quản lý thư viện ở các trường ĐH    | 	Trường                 | 	20           | 	2009-05-10 | 	2010-05-10    | 	QLGD  | 	001         |


## dbo.GIAOVIEN:

| MAGV  | HOTEN            | LUONNG  | PHAI  | NGSINH         | DIACHI                                | GVQLCM  | MABM   |
|-------|------------------|---------|-------|----------------|---------------------------------------|---------|--------|
| 001   | 	Nguyễn Hoài An  | 	2000   | 	Nam  | 	1973-02-15    | 	25/3 Lạc Long Quân, Q.10,TP HCM      | 	NULL   | 	MMT   |
| 002   | 	Trần Trà Hương  | 	2500   | 	Nữ   | 	1960-06-20    | 	125 Trần Hưng Đạo, Q.1, TP HCM       | 	NULL   | 	HTTT  |
| 003   | 	Nguyễn Ngọc Ánh | 	2200   | 	Nữ   | 	1975-05-11    | 	12/21 Võ Văn Ngân Thủ Đức, TP HCM    | 	002    | 	HTTT  |
| 004   | 	Trương Nam Sơn  | 	2300   | 	Nam  | 	1959-06-20    | 	215 Lý Thường Kiệt,TP Biên Hòa       | 	NULL   | 	VS    |
| 005   | 	Lý Hoàng Hà     | 	2500   | 	Nam  | 	1954-10-23    | 	22/5 Nguyễn Xí, Q.Bình Thạnh, TP HCM | 	NULL   | 	VLĐT  |
| 006   | 	Trần Bạch Tuyết | 	1500   | 	Nữ   | 	1980-05-20	   | 127 Hùng Vương, TP Mỹ Tho             | 	004    | 	VS    |
| 007   | 	Nguyễn An Trung | 	2100   | 	Nam  | 	1976-06-05    | 	234 3/2, TP Biên Hòa                 | 	NULL   | 	HPT   |
| 008   | 	Trần Trung Hiếu | 	1800   | 	Nam	 | 1977-08-06     | 	22/11 Lý Thường Kiệt,TP Mỹ Tho       | 	007    | 	HPT   |
| 009   | 	Trần Hoàng nam  | 	2000   | 	Nam	 | 1975-11-22	234 | Trấn Não,An Phú, TP HCM               | 	001    | 	MMT   |
| 010   | 	Phạm Nam Thanh  | 	1500   | 	Nam	 | 1980-12-12	221 | Hùng Vương,Q.5, TP HCM                | 	007    | 	HPT   |


## dbo.GV_DT

| MAGV  | DIENTHOAI    |
|-------|--------------|
| 001   | 	0838912112  | 
| 001   | 	0903123123  |
| 002   | 	0913454545  |
| 003   | 	0838121212  |
| 003   | 	0903656565  |
| 003   | 	0937125125  |
| 006   | 	0937888888  |
| 008   | 	0653717171  |
| 008   | 	0913232323  |


## dbo.KHOA

| MAKHOA | TENKHOA               | NAMTL | PHONG | DIENTHOAI   | TRUONGKHOA   | NGAYNHANCHUC             |
|--------|-----------------------|-------|-------|-------------|--------------|--------------------------|
| CNTT   | 	Công nghệ thông tin  | 	1995 | 	B11  | 	0838123456 | 	002         | 	2005-02-20 00:00:00.000 |
| HH     | 	Hóa học              | 	1980 | 	B41  | 	0838456456 | 	007         | 	2001-10-15 00:00:00.000 |
| SH     | 	Sinh học             | 	1980 | 	B31  | 	0838454545 | 	004         | 2000-10-11 00:00:00.000  |
| VL     | 	Vật lý               | 	1976 | 	B21  | 	0838223223 | 	005         | 	2003-09-18 00:00:00.000 |



## dbo.NGUOITHAN

| MAGV | TEN     | NGSINH      | PHAI            |
|------|---------|-------------|-----------------|
| 001  | 	Hùng   | 	1990-01-14 | 00:00:00.000    |	Nam|
| 001  | 	Thủy   | 	1994-12-08 | 00:00:00.000    |	Nữ|
| 003  | 	Hà     | 	1998-09-03 | 00:00:00.000    |	Nữ|
| 003  | 	Thu    | 	1998-09-03 | 00:00:00.000    |	Nữ|
| 007  | 	Mai    | 	2003-03-26 | 00:00:00.000    |	Nữ|
| 007  | 	Vy     | 	2000-02-14 | 00:00:00.000    |	Nữ|
| 008  | 	Nam    | 	1991-05-06 | 00:00:00.000    |	Nam|
| 009  | 	An     | 	1996-08-19 | 00:00:00.000    |	Nam|
| 010  | 	Nguyệt | 	2006-01-14 | 00:00:00.000    |	Nữ |


## dbo.THAMGIADT

| MAGV | MADT   | STT | PHUCAP | KETQUA  |
|------|--------|-----|--------|---------|
| 001  | 	002   | 	1  | 	0     | 	NULL   |
| 001  | 	002   | 	2  | 	2     | 	NULL   |
| 002  | 	001   | 	4  | 	2     | 	Đạt    |
| 003  | 	001   | 	1  | 	1     | 	Đạt    |
| 003  | 	001   | 	2  | 	0     | 	Đạt    |
| 003  | 	001   | 	4  | 	1     | 	Đạt    |
| 003  | 	002   | 	2  | 	0     | 	NULL   |
| 004  | 	006   | 	1  | 	0     | 	Đạt    |
| 004  | 	006   | 	2  | 	1     | 	Đạt    |
| 006  | 	006   | 	2  | 	1.5   | 	Đạt    |
| 009  | 	002   | 	3  | 	0.5   | 	NULL   |
| 009  | 	002   | 	4  | 	1.5   | 	NULL   |







