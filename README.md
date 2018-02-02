Установка и проверку расширение: 
--------------------------------------
yii2-pkk5-component и yii2-pkk5-modile
Эти расширение уже добавлено в composer.json
* После клонирование проекта нужно обновить composer:
```
composer update or php composer.phar update
```
и инитализации проекта: 
```
php init
```
и настройка БД, в файле 
```
common\config\main-local.php
```

* Выполнить миграцию для создания нужной таблицы в базе данных (консоль):
```
yii migrate --migrationPath=@muxtor/pkk5module/migrations --interactive=0
```

* Для работа с броузером:
```
http://yourdomain.com/index.php?r=pkk5
```
или в меню пункт Pkk5 parser

* Для работа с console:
```
php yii pkk5/pkk5console/parse 69:27:0000022:1306,69:27:0000022:1307
```

Удачи всем!

DIRECTORY STRUCTURE
-------------------

```
common
    config/              contains shared configurations
    mail/                contains view files for e-mails
    models/              contains model classes used in both backend and frontend
    tests/               contains tests for common classes    
console
    config/              contains console configurations
    controllers/         contains console controllers (commands)
    migrations/          contains database migrations
    models/              contains console-specific model classes
    runtime/             contains files generated during runtime
backend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains backend configurations
    controllers/         contains Web controller classes
    models/              contains backend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for backend application    
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
frontend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains frontend configurations
    controllers/         contains Web controller classes
    models/              contains frontend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for frontend application
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
    widgets/             contains frontend widgets
vendor/                  contains dependent 3rd-party packages
environments/            contains environment-based overrides
```
