<div id="header" align="center">
  <img src="https://i.imgur.com/c7iirLS.jpg" width="100"/>
    <div id="badges">
        <a href="your-linkedin-URL">
            <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
        </a>
        <a href="your-youtube-URL">
            <img src="https://img.shields.io/badge/YouTube-red?style=for-the-badge&logo=youtube&logoColor=white" alt="Youtube Badge"/>
        </a>
        <a href="your-twitter-URL">
            <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
        </a>
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


