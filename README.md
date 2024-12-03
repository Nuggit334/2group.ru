## Создание пустого проекта на laravel 11 в OSPanel
Запускаем OSPanel и открываем консоль
```shell
cd domains
```
Создаем папку для проекта
```shell
mkdir laravel-11.loc

cd laravel-11.loc
composer create-project laravel/laravel .
php artisan install:api
php artisan config:publish cors
php artisan storage:link
