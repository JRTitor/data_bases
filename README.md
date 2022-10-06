#  Работаем в FoxPro 9

вот ссылочка 
https://drive.google.com/drive/folders/19ZZFUAOf29R6J0Km-eYR0RZHvOx58wtf

# У нас есть таблицы
 * Trains_stats
 * Stations
 * Schedules

# Schedules -- расписание для всех станций 
 * schedules_id -- уникальный номер строки таблицы Scheules --- U int
 * station_id -- уникальный номер строки таблицы Stations  --- U int 
 * train_routes_id -- уникальный номер строки таблицы Trains_routes --- U int 
 * date -- дата прибытия поезда на стацию --- date 
 * arrival -- время прибытия --- они изменяются и в Trains_routes --- time (HH:MM) ///  NONE
 * departure  -- время отбытия --- они изменяются и в Trains_routes --- time (HH:MM) /// NONE
 * platform/way  -- Путь/платформа --- U int


# Stations
 * station_id -- уникальный номер строки таблицы Stations --- U int
 * station_name -- имя станции (Ленинградский вокзал) --- string
 * city -- город станции --- string 
 * platfrom/way_amount -- количество путей/платформ --- U int

# Trains_routes --- главная табличка
 * train_routes_id -- уникальный номер строки таблицы Trains_stats --- U int
 * train_route_name -- например №724В ЛАСТОЧКА  --- string
 * station_from_id -- ID станции ОТКУДА уникальный номер строки таблицы Stations --- U int
 * station_to_id -- ID станции КУДА уникальный номер строки таблицы Stations  --- U int
 * arrival_to -- время прибытия --- time (HH:MM) 
 * departure_from  -- время отбытия --- time (HH:MM)

### Вопросы на подумать и обсуждение (TODO)
* Заполнить табоицу данными
* Что такое Логическая модель и как её сделать
* Что такое Физическая модель и как её сделать