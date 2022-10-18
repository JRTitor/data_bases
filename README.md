#  Работаем в FoxPro 9

вот ссылочка 
https://drive.google.com/drive/folders/19ZZFUAOf29R6J0Km-eYR0RZHvOx58wtf

# У нас есть таблицы
 * Trains_stats
 * Stations
 * Schedules

# Schedules -- расписание для всех станций 
 * schedules_id -- уникальный номер строки таблицы Scheules --- numeric
 * station_id -- уникальный номер строки таблицы Stations  --- numeric
 * train_routes_id -- уникальный номер строки таблицы Trains_routes --- numeric
 * date -- дата прибытия поезда на стацию --- date 
 * arrival -- время прибытия --- они изменяются и в Trains_routes --- time (HH:MM) ///  NONE
 * departure  -- время отбытия --- они изменяются и в Trains_routes --- time (HH:MM) /// NONE
 * platform/way  -- Путь/платформа --- numeric


# Stations
 * station_id -- уникальный номер строки таблицы Stations --- numeric
 * station_name -- имя станции (Ленинградский вокзал) --- string
 * city -- город станции --- string 
 * platfrom/way_amount -- количество путей/платформ --- numeric

# Trains_routes --- главная табличка
 * train_routes_id -- уникальный номер строки таблицы Trains_stats --- numeric
 * train_route_name -- например №724В ЛАСТОЧКА  --- string
 * station_from_id -- ID станции ОТКУДА уникальный номер строки таблицы Stations --- numeric
 * station_to_id -- ID станции КУДА уникальный номер строки таблицы Stations  --- numeric
 * arrival_to -- время прибытия --- time (HH:MM) 
 * departure_from  -- время отбытия --- time (HH:MM)

### Вопросы на подумать и обсуждение (TODO)
* Заполнить табоицу данными
* Что такое Логическая модель и как её сделать
* Что такое Физическая модель и как её сделать


##  Роли на заполнние 

Мы выбираем вокзал, заполняем данные о вокзале /b Stations, запоняем /b Train_routes с выбранным маршрутом, добавляем вторую станцию, добавляем две записи в /b Schedules, первая откуда, вторая куда. Так как у нас есть маршруты, то мы добавляем несколько записей в /b Schedules (3-5 на маршрут), маршрутов выбираем не менее 7

 * Сергей : Ленинградский вокзал
  