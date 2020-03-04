Лаб.раб. № 1
Используя данные таблицы АВ:
A	B
3.1415	4
-45	0.707
5	9
-57.667	42
15	55
-7.2	5.3
1. Вычислить: модуль всех значений столбца А, cosA, sinA, tgA, eA
2. Найти наибольшее и наименьшее целое для значений столбцов А и В.
3. Вычислить 2В, -2А.
4. Определить знак для всех значений А и В.
5. Вычислить квадратный корень для значений столбца В.
6. Из таблицы PRODUCT вывести названия товаров (p¬_desc), цена продажи (price) которых кратна 0.6.
7. Объединить в один столбец название фирмы-производителя (m_name) и адрес фирмы-производителя (табл. MANUFACT):
name_country
Odejda"Kivi" – Aucland
Lampy Lama - Lima
8. Записать названия товаров (p_desc) прописными и строчными буквами (табл. PRODUCT).
9. Перед фамилией клиента (ct_name) поставить горизонтальную черту. Общая длина поля должна составить 15 символов (табл. CUSTOMER).
10. После фамилии клиента (c_name) поставить горизонтальную черту. Общая длина поля должна составить 15 символов (табл. CUSTOMER).
11.Удалить в названиях стран(country) в таблице COUNTRY первые 2 буквы 'US'.
12. Удалить в столбце sp_name все сочетания символов 'an' ( табл.SPERSON).
13. Заменить в столбце sp_name все сочетания символов 'an' на '_n' (табл.SPERSON).
14. Для данных столбца p_desc таблицы PRODUCT вывести в отдельный столбец 3 символа, начиная с четвертого.
15. Для данных столбца p_desc таблицы PRODUCT вывести в отдельный столбец хвостовые символы, начиная с седьмого. 
16. Вывести исходные данные для таблицы cod_ssn
ssn
300541117
301457111
459789998
в следующем виде:
ssn
300-54-1117
301-45-7111
459-78-9998
17. Определить номер позиции первой буквы 'o' в столбце sp_name (табл. SPERSON) с начала строки.
18. Определить номер позиции второй буквы 'o' в столбце sp_name (табл. SPERSON), начиная просмотр со второго символа.
19. Определить номер позиции второй буквы 'o' в столбце sp_name (табл. SPERSON), начиная просмотр с третьего символа.
20. Определить количество символов для каждой строки столбца sp_name таблицы SPERSON.
21. Вывести в отдельные столбцы фамилию и имя сотрудника.
 
select abs(-5) from dual – модуль (абсолютное значение числа)
5

select mod(5,2) from dual – остаток от деления 5 на 2
1
select sin(30*3.14159265/180), cos(30*3.14159265/180), tan(30*3.14159265/180),
sinh(30*3.14159265/180), cos(30*3.14159265/180), tan(30*3.14159265/180)
from dual – пример вычисления тригонометрических функций, аргумент указывается в радианах.

select floor(3.99), ceil(3.01), round(3.566,2), trunc(3.566, 2) from dual - округление
              3                  4                   3.57                     3.56

select power(-2, 5) from dual – возведение -2 в степень 5
-32

select sqrt(25) from dual – квадратный корень из 25
5

select sign(-10), sign(10), sign(0) from dual знак числа
              -1               1            0

select ln(45) from dual – натуральный логарифм
3.8

select log(2, 8) from dual логарифм от 8 по основанию 2
3

select c_name || ', ' || address f_a from customer – объединение строк
Djefferson, Chicago
Maltz, Zaltsburg
Gomes, Santiago
Wotaib, Tokyo

select chr(65) from dual - символ по коду
A

select ltrim('     a') from dual – убирает пробелы в начале строки (слева)
a

select ltrim(sp_name, 'Ba') from sperson – удаляет ‘Ва’ в начале строки (слева)
Masai Matsu
Terii Cardon
ridjit Bovari
Rodny Djons
Albert Aidj
Fransua Muar
Elena Ermana
Goro Atsuma
ster Sances
select rpad(c_name, 40, '_') spisok from customer – дополняет каждую фамилию горизонтальной чертой. Новая длина строки 40 символов.
Djefferson______________________________
Maltz___________________________________
Gomes___________________________________
Wotaib__________________________________
select substr(c_name, 2, 4)  spisok from customer – из с__name, начиная со 2 символа, выделяется подстрока длиной 4 символа
select substr(c_name, 2)  spisok from customer – из с__name, начиная со 2 символа, выделяется подстрока до конца строки


select replace(c_name, 'a', '**')  spisok from customer – в столбце c_name 'все буквы 'a' заменяются на '**'
Djefferson
M**ltz
Gomes
Wot**ib
select replace(c_name, 'a')  spisok from customer – из столбца c_name удаляются все буквы 'a'
Djefferson
Mltz
Gomes
Wotib

select translate(c_name, 'om', '12')  spisok from customer – каждая буква ‘а’ заменяется на 1, 
каждая буква ‘m’ заменяется на 2
Djeffers1n
Maltz
G12es
W1taib
select length(c_name)  spisok from customer – длина строки

select c_name, instr(c_name, 'e'), instr(c_name, 'e', 1, 2), instr(c_name, 'e',5, 2) from customer – определяется
позиция первой буквы ‘e’, поиск ведется с начала строки,
определяется позиция второй буквы ‘e’, поиск ведется с пятой позиции
select concat(c_name, concat(', ', address)) spisok  from customer – объединение строк.



