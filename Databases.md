# Домашнее задание к занятию "Базы данных" - Боровский Юрий



### Задание 1

table = Сотрудники
columns:
        employee_id (primary_key) serial
        fio varchar(50)
        unit_type_id (foreign_key) int
        unit_id (foreign_key) int
        position_id (foreign_key) int
        project_id (foreign_key) int
        salary int
        employment_date date
        
       
table = Тип подразделения
columns:        
        unit_type_id (primary_key) serial
        unit_type varchar(50)



table = Структурное подразделения
columns:
        unit_id (primary_key) serial
        unit_type_id (foreign_key) int
        unit_name varchar(50)
        
        


table = Регион
columns: 
        region_id (primary_key) serial
        region varchar(50)

table = Город
columns: 
        city_id (primary_key) serial
        region_id (foreign_key) int
        city varchar(50)
        
        
        
        
table = Адрес филиала
columns: 
        region_id (primary_key) serial
        city_id (primary_key) serial
        adress varchar(50)
        
        
                
table = Проекты
columns: 
        project_id (primary_key) serial
        project varchar(100)
        
        
table = Должность
columns: 
        position_id (primary_key) serial
        position varchar(100)
        
        
