<div id="header" align="center">
  <img src="https://i.imgur.com/c7iirLS.jpg" width="500"/>
    <div>
    </div>
    <h1>Internship</h1>
</div>

---

### :black_nib: SQL Basics 


- :pencil2: SQL hay Structured Query Language là ngôn ngữ truy vấn có cấu trúc. dùng cho việc thao tác lưu trữ và truy xuất dữ liệu được lưu trữ trong một cơ sở dữ liệu quan hệ. 

- :pencil2: RDBMS hay Relational Database Management System: hệ quản trị cơ sở dữ liệu, là nền tảng cho MySQL, Oracle, Microsoft SQL, 

- :pencil2: Table là nơi tập hợp các dữ liệu có quan hệ với nhau, bao gồm hàng và cột

- :arrow_up: Cột hay field là một thuộc tính cụ thể của các đối tượng, dùng để phân biệt các dữ liệu với nhau, VD bảng Student bao gồm các cột StudentID, Name,...

- :arrow_right: Dòng hay record là tượng trưng cho một đối tượng cụ thể thuộc bảng và có các thuộc tính của các cột, VD 1 sinh viên nào đó có StudentID, Name lần lượt là 20110011, Hoàng Lê Tiến Đạt

------

------

- :pencil2: SELECT: Lấy tất cả dữ liệu, hoặc theo từng cột Collumn1 từ bảng TABLENAME 

- SELECT * (hoặc Collumn1, Collumn2) FROM TABLENAME 

---

- :pencil2:  DISTINCT :point_right: Bỏ những phần lặp lại của dữ liệu

- VD: SELECT DISTINCT Column1 FROM TABLENAME; -> ví dụ column có Year: 1,2,3,4,4,1,5 thì sẽ chỉ lấy 1,2,3,4,5

---

- :pencil2: WHERE :point_right: Đưa ra cụ thể thuộc tính để lọc dữ liệu

- VD: SELECT * FROM Customers WHERE Country='Mexico'; -> lấy những đối tượng có thuộc tính Quốc tịch là Mexico

* Note: nếu thuộc tính là String thì phải để trong '' hoặc "" , có thể sử dụng '>','<' chứ không nhất thiết phải '='

- BETWEEN (giữa khoảng nào): WHERE Price BETWEEN 50 AND 60;

- LIKE (tựa như): WHERE City LIKE 's%';

- IN (trong tập hợp nào):WHERE City IN ('Paris','London');

---

- :pencil2: ORDER BY :point_right: Sắp xếp dữ liệu tìm được theo thứ tự

- VD: SELECT column1, column2, ... FROM table_name ORDER BY column1, column2, ... ASC|DESC; -> lấy các dữ liệu có trong cột column1
column2 từ bảng table_name sắp xếp theo thứ tự cột 1, cột 2 tăng dần | giảm dần

* Có nhiều cột thì sẽ ưu tiên sắp xếp theo cột đầu, nếu trùng nhau thì so sánh dựa trên cột 2: ORDER BY Country ASC, CustomerName DESC;

---

- :pencil2: ORDER BY :point_right: Sắp xếp dữ liệu tìm được theo thứ tự

- VD: SELECT * FROM Customers WHERE Country = 'Spain' AND CustomerName LIKE 'G%'; -> lấy tất cả dữ liệu từ bảng Khách hàng có QUốc tịch là TBN và tên bắt đầu bằng chữ G

---

- :pencil2: AND/OR :point_right: Khi có nhiểu đk thì có thể chọn và / hoặc

- AND thì cả hai điều kiện phải xảy ra thì mới được lấy, OR thì chỉ cần một trong hai điều kiện xảy ra là được

* Có thể sử dụng ngoặc: WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');

* AND là dấu x, OR là dấu + nên nếu bỏ ngoặc thì đk trên sẽ trở thành đất nước TBN và tên bắt đầu = G. Hoặc là những người chỉ cần có tên bắt đầu bằng R, đất nước không quan trọng

---

- :pencil2: NOT :point_right: Là loại bỏ các dữ liệu thuộc điều kiện phía sau NOT

- VD: SELECT * FROM Customers WHERE NOT Country = 'Spain'; : Lấy tất cả dữ liệu từ ... mà có quốc tịch không phải TBN

---

---

- :pencil2: INSERT INTO :point_right: Là loại bỏ các dữ liệu thuộc điều kiện phía sau NOT

- VD: INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...); : Thêm vào dữ liệu có các thuộc tính cột 1 = value 1, cột 2 = value2,...

* Nếu thuộc tính nào không được khai báo thì coi như null, hoặc mặc định

* Có thể sử dụng "," để khai báo 1 lúc nhiều dữ liệu: INSERT INTO ... VALUES (a,b,c),(a1,b1,c1);

---

- :pencil2: NULL/NOT NULL :point_right: là giá trị rỗng / không rỗng

- VD: SELECT column_names
FROM table_name
WHERE column_name IS NULL; : lấy dữ liệu ... với đk column là rỗng

---

---

- :pencil2: UPDATE :point_right: cập nhật giá trị (của một hoặc nhiều thuộc tính) của một dữ liệu nào đó đã có trong table

- VD: UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition; : cập nhật giá trị cột 1 bằng value 1,... với điều kiện

---

---

- :pencil2: DELETE :point_right: xoá bỏ dữ liệu nào đó đã có trong table

- VD: UPDATE table_name

* Muốn xoá toàn bộ Table thì dùng DROP: DROP TABLE Customers;

---

---

- :pencil2: SELECT TOP :point_right: lấy dữ liệu với số lượng nhất định 

- VD: SELECT TOP 3 * FROM Customers;: lấy 3 đối tượng từ bảng Customer

* Note: có thể dùng PERCENT: TOP 50 PERCENT

<div id="header_1" align="center">
    <h1>Aggregate Functions</h1>
</div>

- :pencil2: Set Column Name (Alias) :point_right: Đặt tên

- VD: SELECT MIN(Price) AS SmallestPrice
FROM Products;:  lấy ra giá tiền nhỏ nhất từ bảng Sản phẩm, đặc tên là SmallestPrice

---

- :pencil2: MIN/MAX :point_right: Lấy giả trị nhỏ nhất / lớn nhất

- VD: SELECT MIN(Price) AS SmallestPrice
FROM Products;:  lấy ra giá tiền nhỏ nhất từ bảng Sản phẩm, đặc tên là SmallestPrice

---

- :pencil2: MIN/MAX :point_right: Lấy giả trị nhỏ nhất / lớn nhất

- VD: SELECT MIN(Price) AS SmallestPrice
FROM Products;:  lấy ra giá tiền nhỏ nhất từ bảng Sản phẩm, đặc tên là SmallestPrice

---

- :pencil2: MIN() with GROUP BY :point_right: Lấy nhỏ nhất của từng nhóm nào đó

- VD: SELECT MIN(Price) AS SmallestPrice, CategoryID
FROM Products
GROUP BY CategoryID;:  lấy ra giá tiền nhỏ nhất từ từ mỗi loại danh mục có ID...

---

- :pencil2: COUNT :point_right: Trả về giá trị số các dòng

- VD: SELECT COUNT(*)
FROM Products;:  tìm tổng số product

* Nếu nêu rõ cột thì phép đếm sẽ bỏ qua các dữ liệu có cột đó = null

* THêm Distinct thì sẽ bỏ những phần tử trùng :SELECT COUNT(DISTINCT Price)
FROM Products;

* Đặt tên: SELECT COUNT(*) AS [Number of records]
FROM Products;

---

- :pencil2: SUM()/ AVG() :point_right: Trả về tổng / trung bình cộng của một cột chỉ chứa giá trị số nào đó.

- VD: SELECT SUM(Quantity) 
FROM OrderDetails;  Tính tổng quantity từ orderdetails

* Các ví dụ dùng công thức và LEFT JOIN:
- SELECT SUM(Quantity * 10)
FROM OrderDetails;

- SELECT SUM(Price * Quantity)
FROM OrderDetails
LEFT JOIN Products ON OrderDetails.ProductID = Products.ProductID;

---

- :pencil2: LIKE :point_right: Lấy dữ liệu có dạng như là

- SELECT * FROM Customers
WHERE CustomerName LIKE 'a%'; :  lấy ra các khách hàng có tên bắt đầu bằng a

* % thay thế cho không, một hoặc nhiều kí tự nào (tức là cái nào cũng thoả mãn)

-> a% tức là bắt đầu bằng a, %a tức là kết thúc bằng a

* _ thay thế cho chỉ 1 kí tự (kí tự nào cũng được nhưng chỉ được 1 kí tự)

* [ ] là giống tập hợp các kí tự thoả mãn: '[bsp]%'; tức là bắt đầu bằng chữ cái b hoặc s hoặc p

* "-" được sử dung trong array để viết tắt như là trong khoảng: '[a-f]%'; tức là bắt đầu bằng chữ cái trong khoảng từ a đến f đều được

---

- :pencil2: JOIN :point_right: Kết hợp dữ liệu (tương ứng một thuộc tính nào đó) được tập hợp từ hai hay nhiều bảng

- :red_square: JOIN (INNER JOIN) Kết hợp hai bảng và chỉ lấy những dòng nào mà tồn tại tương ứng ở cả 2 bảng

- :blue_square: LEFT (OUTER) JOIN  Kết hợp hai bảng và lấy tất cả dòng ở bảng bên trái (cho dù có record không tồn tại record tương ứng ở bảng còn lại)  

- :yellow_square: RIGHT (OUTER) JOIN Kết hợp hai bảng và lấy tất cả dòng ở bảng bên phải (cho dù có record không tồn tại record tương ứng ở bảng còn lại)  

- :purple_square: FULL (OUTER) JOIN Kết hợp hai bảng và lấy toàn bộ các dòng của cả hai bảng

* Note: Ví dụ khi xài RIGHT JOIN, dòng ở bảng bên phải mà không có dữ liệu tính tương ứng ở bảng bên trái thì sẽ để null toàn bộ thuộc tính ở bảng bên trái

- :brown_square: SELF JOIN Kết hợp hai bảng và lấy toàn bộ các dòng của cả hai bảng

* VD: SELECT A.CustomerName AS CustomerName1, B.CustomerName AS CustomerName2, A.City
FROM Customers A, Customers B
WHERE A.CustomerID <> B.CustomerID
AND A.City = B.City
ORDER BY A.City;: Sẽ tạo ra bảng có 2 cột Name 1, Name 2 sẽ là tên của 2 người cùng sống ở một thành phố

---

- :pencil2: UNION  :point_right: Lấy dữ liệu giống nhau từ các bảng khác nhau

- SELECT City FROM Customers
UNION
SELECT City FROM Suppliers
ORDER BY City; :  lấy các thành phố từ hai bảng Customers và Suppliers

*Note: Các cột được lấy từ SELECT phải có cùng tên, kiểu dữ liệu và thứ tự sắp xếp (nếu có nhiều cột)

*UNION ALL sẽ lấy cả những dữ liệu trùng (mặc định bỏ qua)

---

- :pencil2: UNION  :point_right: Lấy dữ liệu giống nhau từ các bảng khác nhau
- VD: SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;

---

- :pencil2: GROUP BY  :point_right: Nhóm các dữ liệu giống nhau ở một thuộc tính nào đó, có thể sự dụng arrgregate function (SUM, AVG,COUNT, MAX, MIN) để nhóm
- VD: SELECT Shippers.ShipperName, COUNT(Orders.OrderID) AS NumberOfOrders FROM Orders
LEFT JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID
GROUP BY ShipperName;: nhóm các record mà ở đó có chung shippername (nhóm lại thành một record shippername)

---

- :pencil2: HAVING  :point_right: Giống WHERE nhưng WHERE không xài các arrgregate function được còn HAVING thì có

- VD: SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5; xuất ra bảng có đất nước và số lượng người có quốc tịch đó

---

- :pencil2: EXISTS  :point_right: Test trong dữ liệu coi có record nào đó tồn tại không

- VD: SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20); trả về tên của các nhà cung cấp mà có sản phẩm trong bảng Products và giá nhỏ hơn 20

---

- :pencil2: ANY / ALL  :point_right: Giống phép so sánh ở trên nhưng là so sánh giữa một cột và tập hợp các cột

- VD: SELECT ProductName
FROM Products
WHERE ProductID = ANY
  (SELECT ProductID
  FROM OrderDetails
  WHERE Quantity = 10); sẽ trả về một bảng gồm các ProductName mà Quantity = 10

- VD: SELECT ProductName
FROM Products
WHERE ProductID = ALL
  (SELECT ProductID
  FROM OrderDetails
  WHERE Quantity = 10); sẽ trả về rỗng vì yêu cầu tất cả phải có QUantity = 10

---

- :pencil2: SELECT INTO  :point_right: Không chỉ chọn ra các dữ liệu mà còn đưa các dữ liệu vào một bảng mới

- VD: SELECT Customers.CustomerName, Orders.OrderID
INTO CustomersOrderBackup2017
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID; copy tên khách hàng và orderId vào bảng backup (orderID có thể rỗng do là LEFT JOIN)

* Note: SELECT * INTO newtable
FROM oldtable
WHERE 1 = 0; giúp tạo bảng với dữ liệu trống nhưng vẫn giữ các cột của oldtable

---

- :pencil2: INSERT INTO ... SELECT :point_right: Tương tự SELECT INTO nhưng là đưa dữ liệu vào bảng có sẵn

- VD: INSERT INTO Customers (CustomerName, City, Country)
SELECT SupplierName, City, Country FROM Suppliers
WHERE Country='Germany';: copy tên khách hàng, thành phố, quốc gia từ bảng Suppliers vào bảng Customers với điều kiện Quốc gia là Đức

* Note: Yêu cầu dữ liệu đưa vào phải khớp với dữ liệu có sẵn giống UNION

<div id="header_1" align="center">
    <h1>SQl Database</h1>
</div>

- CREATE DATABASE databasename;: Tạo CSDL

- DROP DATABASE databasename;: Xoá hoàn toàn CSDL
- BACKUP DATABASE databasename
TO DISK = 'filepath';: Backup bảng vào filepath

- BACKUP DATABASE databasename
TO DISK = 'filepath'
WITH DIFFERENTIAL;: Backup chỉ những thay đổi so với lần backup gần nhất

- CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255)
);: Tạo bảng với các thuộc tính

- DROP TABLE table_name;: Xoá bảng

- ALTER TABLE table_name
ADD column_name datatype; (hoặc DROP COLUMN column_name;): thay đổi bảng bằng thêm cột (xoá cột)

<div id="header_1" align="center">
    <h1>Các constraint của Database</h1>
</div>

- ID int NOT NULL : ID không được rỗng

- ID int NOT NULL UNIQUE: Tag UNIQUE đảm bảo rằng ID không thể bị trùng lặp

- CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);: Primary key để xác định thuộc tính chính để đánh dấu các record

- CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);: FOREIGN KEY để ánh xạ đến một Primary của bảng khác và ngăn cho mối liên hệ giữa hai bảng không bị cắt, cũng như xác định loại dữ liệu của foreign key phải trùng với primary key ấy

- CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
); CHECK đảm bảo rằng dữ liệu Age được đưa vào phải >=18

- CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);: Tạo ra dữ liệu mặc định cho một thuộc tính

- CREATE TABLE Persons (
    Personid int NOT NULL AUTO_INCREMENT,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (Personid)
);: AUTO_INCREMENT giúp để tự động tăng primary key khi tạo record mới

---

<div id="header_1" align="center">
    <h1>FUNCTIONS và TRIGGER của PosrgreSQL</h1>
</div>
- Fuction: A function in PostgreSQL is a named block of code that accepts arguments, performs a set of operations, and returns a result.
Hàm là một đoạn code có tên và sử dụng các tham số truyền vào để thực hiện một tập hợp các phép toán và trả về một kết quả. Function có thể được gọi và sử dụng bởi các function khác hoặc trigger.
- VD:
CREATE FUNCTION add_numbers(a integer, b integer)
RETURNS integer AS $$
BEGIN
    RETURN a + b;
END; $$
LANGUAGE plpgsql;

- Trigger: A Trigger cũng là một đoạn code có tên được tự động gọi lên để thực hiện khi có một sự kiện gì đó xảy ra (như INSERT, DELETE, UPDATE, ...). Trigger khi được gọi sẽ thực hiện các hàm, hoặc các thao tác xoá sửa thêm, ...
- VD:
CREATE OR REPLACE FUNCTION f_temp ()
RETURNS trigger AS
$$
     DECLARE
 
     BEGIN
          RAISE NOTICE 'NEW: %', NEW;
          IF NEW.value < 0
          THEN
               NEW.value := -1;
               RETURN NEW;
          END IF;
          RETURN NEW;
     END;
$$ LANGUAGE 'plpgsql';
- VD CREATE TRIGGER xtrig
     BEFORE INSERT ON t_temperature
     FOR EACH ROW EXECUTE PROCEDURE f_temp();