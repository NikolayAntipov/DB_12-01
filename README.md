# Домашнее задание к занятию «Базы данных» - Антипов Н.С.

## Легенда
Заказчик передал вам файл в формате Excel, в котором сформирован отчёт.

На основе этого отчёта нужно выполнить следующие задания.

## Задание 1
Опишите не менее семи таблиц, из которых состоит база данных:

какие данные хранятся в этих таблицах;
какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Приведите решение к следующему виду:

Сотрудники (

идентификатор, первичный ключ, serial,
фамилия varchar(50),
...
идентификатор структурного подразделения, внешний ключ, integer).

## Ответ

##### Сотрудник 
•	ID_сотрудника, первичный ключ, serial  
•	ФИО, varchar(50)  
•	Дата_найма, date  
•	ID_подразделения, smallint, внешний ключ   
•	ID_структ_подразделения, smallint, внешний ключ  
•	ID_проекта, smallint, внешний ключ   
•	Оклад, money, внешний ключ  
##### Подразделение 
•	ID_подразделения, primary_key, serial  
•	Наименование_подразделения, varchar(50)  
•	Структурное_подр., smallint, внешний ключ ID_структ_подразделения.  
##### Структурное _подразделение   
•	ID_структ_подразделения, первичный ключ, serial  
•	Наименование_структ_подразделения, varchar(20)  
##### Должность   
•	ID_должности, первичный ключ, serial  
•	Наименование_должности, varchar(50)  
•	Оклад, money  
•	ID_подразделения, varchar(50), внешний ключ  
##### Адрес филиала 
•	ID_филиала, первичный ключ, serial  
•	Край, varchar(50)  
•	Город, varchar(50)  
•	Улица, varchar(100)  
•	Дом, varchar (30) 
##### Проект 
•	ID_проекта, первичный ключ, serial  
•	Наименование_проекта, varchar(100)
