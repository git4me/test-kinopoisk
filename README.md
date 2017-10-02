# Тестовое задание для веб-разработчика

Необходимо написать скрипт, собирающий данные с рейтинга Кинопоиска (http://www.kinopoisk.ru/top/), и сохраняющего позицию, рейтинг, оригинальное название, год и кол-во проголосовавших людей в БД (любой на выбор). Также необходимо добавить соответствующие поля в БД для выборки рейтинга на определенную дату. Скрипт должен быть написан с учетом возможности постановки в cron.
Также необходимо создать базовую веб-страницу, выводящую топ-10 фильмов на указанную дату. На ней должно присутствовать поле, где пользователь может указать дату выборки. При выгрузке данных из СУБД должен быть использован кэширующий слой, что бы избежать запросов к базе, каждый раз, когда рейтинг должен быть показан.
Критерии оценки:

 - чистый, читаемый, структурируемый php код, объектное ориентированный дизайн;
 - схема базы данных;
 - чистота верстки.
 
# Решение

#### Установка
 0) ./app build - собераем
 1) ./app start - запустит сайт на localhost:8000
 2) ./app migrate - установить схему базы данных
 
 По умолчанию данные берутся из базы данных. 
 
#### Загрузка данных
 
 ```
 ./app run-task date=2017-01-10  //спарсит данные за указанный день
 ./app run-task                  //спарсит данные за текущий день
  ```
 ## Остальное
 
```
 ./app stop  //остановить приложение
 ./app       //вызов справки по командам
 
```
 
 ## Проблемы
  - нет логера
  - нет обработчика ошибок для web и console 
