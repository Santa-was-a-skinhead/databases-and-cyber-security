# Домашнее задание к занятию "Работа с данными (DDL/DML)" - Боровский Юрий



---

### Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.
sudo apt install mysql-server
![](https://github.com/Santa-was-a-skinhead/databases-and-cyber-security/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-05-06%2013-57-33.png)

1.2. Создайте учётную запись sys_temp.
mysql
CREATE USER sys_temp IDENTIFIED BY 12345;

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)
SELECT host, user FROM mysql.user;
![](https://github.com/Santa-was-a-skinhead/databases-and-cyber-security/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-05-06%2013-56-57.png)

1.4. Дайте все права для пользователя sys_temp.
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'%' WITH GRANT OPTION;

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
SHOW GRANTS FOR 'sys_temp'@'%';
![](https://github.com/Santa-was-a-skinhead/databases-and-cyber-security/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-05-06%2014-00-13.png)
1.6. Переподключитесь к базе данных от имени sys_temp.
ALTER USER 'sys_test'@'%' IDENTIFIED WITH mysql_native_password BY '12345'

CLIENT COMMANDS
sudo apt install mysql-client-8.0
dbeaver: Локальный клиент = /usr/bin/

![](https://github.com/Santa-was-a-skinhead/databases-and-cyber-security/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-05-06%2016-06-38.png)
1.7. Восстановите дамп в базу данных.
![](https://github.com/Santa-was-a-skinhead/databases-and-cyber-security/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-05-06%2016-08-25.png)

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
![](https://github.com/Santa-was-a-skinhead/databases-and-cyber-security/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-05-06%2015-32-54.png)

---

### Задание 2


![](https://github.com/Santa-was-a-skinhead/databases-and-cyber-security/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-05-06%2015-53-04.png)


