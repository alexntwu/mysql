# Appendix 1. MySQL安裝

![image](https://github.com/alexntwu/mysql/assets/1982325/72e239c7-db20-4bd7-820c-a6a30423205c)

下載XAMPP
```
https://www.apachefriends.org/zh_tw/download.html
```
![image](https://github.com/alexntwu/mysql/assets/1982325/d6b25219-52e4-4351-9800-0593a7042cd7)


安裝 sakila 範例資料庫
```
https://dev.mysql.com/doc/sakila/en/
```

![image](https://github.com/alexntwu/mysql/assets/1982325/7f64bff6-1620-444b-9cd8-2ee9d4e02365)

參考 Installation 章節的說明
下載 Sakila 資料庫的 Zip file並解壓縮 到 C:\temp
或直接由以下網址下載
```
https://downloads.mysql.com/docs/sakila-db.zip
```

$> mysql -u root –p
```
mysql -u root –p
```

mysql> SOURCE C:/temp/sakila-db/sakila-schema.sql; 
```
SOURCE C:/temp/sakila-db/sakila-schema.sql;
```
mysql> SOURCE C:/temp/sakila-db/sakila-data.sql;
```
SOURCE C:/temp/sakila-db/sakila-data.sql;
```

mysql> USE sakila; 
Database changed 
```
USE sakila;
```
mysql> SHOW FULL TABLES;
```
SHOW FULL TABLES;
```
