# Домашнее задание по теме "Базы Данных" - Подус Сергей

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

## Ответ:

Данные находящиеся в таблицах:

# 1.1

1. ФИО сотрудника
2. Оклад
3. Должность
4. Тип подразделения
5. Структурное подразделение
6. Дата найма
7. Адрес филиала
8. Название назначенного проекта

Тип данных в  таблицах:

1. фио - строковый (varchar)
2. ОКЛАД - числовой (decimal/numeric)
3. должность - строковый (varchar)
4. Тип подразделения - строковый (varchar)
5. Дата - дата и время (date)
6. Адрес - местонахождение филиала (varchar)
7. Проэкт - строковый (varchar)

#### employees (

1. id_employee, not null, auto_increment, primary_key
2. last_name, varchar(50), not null
3. first_name, varchar(50), not null
4. surname, varchar(50)
5. rank, foreign_key
6. salary, foreign_key
7. subdivision, foreign_key
8. office, foreign_key
9. project, foreign_key
10. hired_since, date, not null 

#### subdivisions (

1. id_subdivision, int, not null, auto_increment, primary_key
2. subdivision, varchar(100), not null
3. type_of_subdivision, foreign_key
4. office, foreign_key )

#### type_of_subdivision (

1. id_of_type, int, not null, auto_increment, primary_key
2. type )

#### offices (

1. id_office, int, not null, auto_increment, primary_key
2. office, varchar(200), not null )

#### projects (

1. id_project, int, not null, auto_increment, primary_key
2. project, varchar(100), not null )

#### ranks (

1. id_rank, int, not null, auto_increment, primary_key
2. rank, varchar(100), not null )

#### salary (

1. id_salary, int, not null, auto_increment, primary_key
2. salary, real, not null )