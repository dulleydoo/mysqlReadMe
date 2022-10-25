# mysqlReadMe
mysql> show tables;
+----------------------+
| Tables_in_year12flix |
+----------------------+
| KaremsVehicles    |
+----------------------+
1 row in set (0.01 sec)
mysql> describe KaremsVehicles;
+---------+-------------+------+-----+---------+-------------------+
| Field  | Type    | Null | Key | Default | Extra       |
+---------+-------------+------+-----+---------+-------------------+
| vehicle | int     | NO  | PRI | NULL  | auto_increment  |
| year  | int     | NO  |   | 0    | DEFAULT_GENERATED |
| make  | varchar(30) | NO  |   |     |          |
| model  | varchar(30) | NO  |   |     |          |
+---------+-------------+------+-----+---------+-------------------+
4 rows in set (0.01 sec)
mysql> insert into KaremsVehicles (year, make, model)
  -> (‘2005’,‘Ford’,‘Focus’),
  -> (‘2008’,‘Hyundia’,‘Accent’),
  -> (‘2012’,‘Buick’,‘Verano’),
  -> (‘2017’,‘Honda’,‘Civic’),
  -> (‘2015’,‘Mercedes’,‘CLA 45 AMG’);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ’'2005',‘Ford’,‘Focus’),
(‘2008’,‘Hyundia’,‘Accent’),
(‘2012’,‘Buick’,‘Verano’),
' at line 2
mysql> insert into KaremsVehicles (year, make, model) values (‘2005’,‘Ford’,‘Focus’), (‘2008’,‘Hyundia’,‘Accent’),(‘2012’,‘Buick’,‘Verano’),(‘2017’,‘Honda’,‘Civic’),(‘2015’,‘Mercedes’,‘CLA 45 AMG’);
Query OK, 5 rows affected (0.01 sec)
Records: 5 Duplicates: 0 Warnings: 0
mysql> select * from KaremsVehicles;
+---------+------+----------+------------+
| vehicle | year | make   | model   |
+---------+------+----------+------------+
|    1 | 2005 | Ford   | Focus   |
|    2 | 2008 | Hyundia | Accent   |
|    3 | 2012 | Buick  | Verano   |
|    4 | 2017 | Honda  | Civic   |
|    5 | 2015 | Mercedes | CLA 45 AMG |
+---------+------+----------+------------+
5 rows in set (0.00 sec)
12:03
mysql> show databases;
+--------------------+
| Database      |
+--------------------+
| homework12     |
| information_schema |
| mysql       |
| performance_schema |
| sys        |
| year12flix     |
+--------------------+
6 rows in set (0.07 sec)
mysql> use homework12;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A
Database changed
mysql> select * from movies;
+----+---------------+-----------+----------+
| id | title     | genre   | duration |
+----+---------------+-----------+----------+
| 1 | MetroPolis  | Sci-fi  |   153 |
| 2 | Nosferatu   | Horror  |    94 |
| 3 | The Kid    | Comedy  |    68 |
| 4 | The Gold Rush | Adventure |    95 |
+----+---------------+-----------+----------+
4 rows in set (0.00 sec)
