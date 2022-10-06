#  Работаем в FoxPro 9

вот ссылочка 
https://drive.google.com/drive/folders/19ZZFUAOf29R6J0Km-eYR0RZHvOx58wtf

# Условимся, что у нас будут таблицы
 * Train
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
 * platform/way  -- Путь/платформа --- U int (U short)


# Stations
 * station_id -- уникальный номер строки таблицы Stations --- U int
 * station_name -- имя станции (Ленинградский вокзал) --- string
 * location -- координаты для быстрого поиска станции (55.8888, 44.0009087) --- tuple(double, double) обратить внимание / string -- если всё плохо
 * platfrom/way_amount -- количество путей/платформ --- U int (U short)

# Trains_routes --- главная табличка
 * train_routes_id -- уникальный номер строки таблицы Trains_stats --- U int
 * train_route_name -- например №724В ЛАСТОЧКА  --- string
 * train_id -- данные о поезде, его модели и тд --- U int
 * station_from_id -- ID станции ОТКУДА уникальный номер строки таблицы Stations --- U int
 * station_to_id -- ID станции КУДА уникальный номер строки таблицы Stations  --- U int
 * arrival_to -- время прибытия --- time (HH:MM) 
 * departure_from  -- время отбытия --- time (HH:MM)

# Trains
 * train_id -- данные о поезде, его модели и тд --- U int
 * train_model -- модель поезда  --- string 
 * year_build -- дата выпуска поезда --- (date? YY) / U int
 * carriage_num -- количество вагонов --- U int (U short)
 * seats_per_cariage -- количество мест в вагоне, предполагаем, что в каждом вагоне определённого поезда одинаковое количество мест. --- U int (U short)
 * sleeper -- значения (true, false). Если true, в поезде тольео лежачие места(может быть нужен комплект белья), false в поезде только сидячие места --- bool
 * first_class -- типо СВ (true, false) --- bool
 * second_class -- типо купе (true, false) --- bool
 * third_class -- типо плацкарт (true, false) --- bool

### Вопросы на подумать и обсуждение (TODO)
* Что такое Логическая модель и как её сделать
* Что такое Физическая модель и как её сделать