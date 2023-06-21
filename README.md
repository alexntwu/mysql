# MySQL資料庫建置與實作

## Chap 04 建立資料庫表格及索引
ch04.md [連結名稱](https://dddddd "游標顯示")

建立mydb資料庫
```mysql
create database mydb;
```
展示所有資料庫
```mysql
show databases;
```
使用employee 資料庫
```mysql
use mydb;
```
建立department表格
```mysql
create table department
(  
  departmentID int not null auto_increment primary key,
  name varchar(30)
) 
ENGINE=InnoDB;
```
建立employee表格
```mysql
create table employee
(
  employeeID int not null auto_increment primary key,
  name varchar(80),
  job varchar(30),
  departmentID int not null,
  FOREIGN KEY (departmentID) references department(departmentID)
);
```
建立employeeSkills表格
```mysql
create table employeeSkills
(
  employeeID int not null,
  FOREIGN KEY (employeeID)  references employee(employeeID),
  skill varchar(15) not null,
  primary key (employeeID, skill)
);
```

建立索引
```mysql
create index idx_emp_name on employee(name);
```
```mysql
alter table employee add index idx_emp_name_2 (name);
```

刪除索引
```mysql
drop index idx_emp_name on employee
```

