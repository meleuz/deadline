## Задача №1 - Скоро deadline

Разработчикам не особо до вас ("им ведь нужно пилить новые фичи"), поэтому они подготовили для вас сборку, работающую с СУБД и даже приложили схему БД (см. файл schema.sql), но при этом сказали "остальное вам нужно сделать самим, там не сложно" smiling_imp.

Что вам нужно сделать:

1. Внимательно изучить схему
   
2. Создать Docker Container на базе MySQL 8 (прописать создание БД, пользователя, пароля)

3. Запустить SUT (app-deadline.jar): для указания параметров подключения к БД можно использовать:
  
   -либо переменные окружения DB_URL, DB_USER, DB_PASS 
  
   -либо указать их через флаги командной строки при запуске: -P:jdbc.url=..., -P:jdbc.user=..., -P:jdbc.password=... (внимание: при запуске флаги не нужно указывать через запятую!). Данное приложение не использует файл application.properties в качестве конфигурации, конфигурационный файл находится внутри jar архива.
  
   -либо можете схитрить и попробовать подобрать значения, зашитые в саму SUT

Итого в результате у вас должно получиться:

1.docker-compose.yml*

2.app-deadline.jar

3.schema.sql

4.код ваших авто-тестов
