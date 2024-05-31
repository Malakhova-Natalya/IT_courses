# Оконные функции SQL 🗃️


## 🗂️ 1: Введение
✒️ разделы:
- 1.1 О курсе
- 1.2 Зачем нужны оконные функции

## 🗂️ 2: Окна и функции
✒️ разделы:
- 2.1 Песочница и данные 
- 2.2 Ранжирование. Мои решения:
  - [Группы по зарплате в городах - пример на ntile()](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/01%20-%20группы%20по%20зарплате%20в%20городах.txt)
  - [Самые дорогие коллеги - пример на dense_rank() + CTE](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/02%20-%20самые%20дорогие%20коллеги.txt)
- 2.3 Смещение
  - [Следующий и предыдущий - пример на lag() и lead()](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/03%20-%20следующий%20и%20предыдущий.txt)
  - [Процент от максимальной зарплаты в городе - пример на first_value()](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/04%20-%20процент%20от%20максимальной%20зарплаты%20в%20городе.txt)
- 2.4 Агрегация
  - [Фонд оплаты труда по городу - пример на sum() over](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/05%20-%20фонд%20оплаты%20труда%20по%20городу.txt)
  - [Средняя зарплата по департаменту - пример на avg() и count() over](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/06%20-%20средняя%20зарплата%20по%20департаменту.txt)
- 2.5 Скользящие агрегаты
  - [Скользящее среднее по доходам - пример на rows between](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/07%20-%20скользящее%20среднее%20по%20доходам.txt)
  - [Фонд оплаты труда нарастающим итогом - пример на partition, order, rows between](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/08%20-%20фонд%20оплаты%20труда%20нарастающим%20итогом.txt)
- 2.6 Статистика
  - [Жаркий март - пример на cume_dist() и percent_rank()](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/09%20-%20жаркий%20март.txt)
  - [Начало весны - пример на cume_dist() и limit](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/10%20-%20начало%20весны.txt)
  - [Счастливые дни - пример на оконную функцию и CTE](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/11%20-%20счастливые%20дни.txt)
  - [Медиана температуры - пример на percentile_disc()](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/12%20-%20медиана%20температуры.txt)
- 2.7 Резюме

## 🗂️ 3: Фреймы
✒️ разделы:  
- ROWS и GROUPS
  - [ROWS-фрейм - пример на два окна и rows between](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/13%20-%20ROWS-фрейм.txt)
  - [GROUPS-фрейм - пример на cume_dist desc](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/14%20-%20GROUPS-фрейм.txt)
  - [GROUPS-фрейм ближайшая большая зарплата- пример на groups between без current row](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/15%20-%20GROUPS-фрейм%20-%20ближайшая%20большая%20зарплата.txt)
- RANGE
  - [RANGE-фрейм - пример на range between](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/16%20-%20RANGE-фрейм.txt)
  - [RANGE-фрейм - пример на range between preceding and preceding](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/17%20-%20RANGE-фрейм%20-%20макисмальное%20значение%20среди%20меньших%20в%20диапазоне.txt)
- EXCLUDE
  - [EXCLUDE - пример на исключение записи внутри определения окна](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/18%20-%20EXCLUDE.txt)
- FILTER
  - [Сравненте з/п со средней по городу - пример на FILTER](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/19%20-%20сравнение%20зп%20со%20средней%20по%20городу.txt)
  - [FILTER → CASE](https://github.com/Malakhova-Natalya/IT_courses/blob/main/%D0%9E%D0%BA%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5%20%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B8%20SQL/20%20-%20FILTER%20%E2%86%92%20CASE.txt)
  - [Меньше ИТ, больше HR - пример на case when внутри sum](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/21%20-%20Меньше%20ИТ%2C%20больше%20HR.txt)
- Резюме

## 🗂️ 4: Практика
✒️ разделы:  
- Финансы
  - [Выручка по тарифу gold - пример на lag и расчёт процента](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/22%20-%20выручка%20по%20тарифу%20gold.txt)
  - [Выручка по тарифам за 1 квартал - пример на накопительную сумму по секциям](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/23%20-%20выручка%20по%20тарифам%20за%201%20квартал.txt)
  - [Скользящее среднее по тарифу platinum - пример на preceding и following](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/24%20-%20скользящее%20среднее%20по%20тарифу%20platinum.txt)
  - [Сравнение с декабрем - пример на границы фрейма](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/25%20-%20сравнение%20с%20декабрем.txt)
  - [Вклад тарифов - пример на CTE и оконную функцию](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/26%20-%20вклад%20тарифов.txt)
  - [Высокая, средняя и низкая выручка - пример на CTE и NTILE](https://github.com/Malakhova-Natalya/IT_courses/blob/main/Оконные%20функции%20SQL/27%20-%20высокая%2C%20средняя%20и%20низкая%20выручка.txt)
- Кластеризация
- Очистка данных
- Итоги
