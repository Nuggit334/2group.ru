## Создание пустого проекта на laravel 11 в OSPanel
Запускаем OSPanel и открываем консоль
```shell
cd domains
```
Создаем папку для проекта
```shell
mkdir laravel-11.loc
```
Переходим в папку с проектом
```shell
cd laravel-11.loc
```
Создаем новый проект на laravel в текущей директории
```shell
composer create-project laravel/laravel .
```
Устанавливаем поддержку API и модуль Sanctum
```shell
php artisan install:api
```
```shell
php artisan config:publish cors
```
```shell
php artisan storage:link
```
В корне проекта создан файл .htaccess
```php
RewriteEngine on
RewriteRule ^(.*)$ public/$1
```
## Установка проекта из репозитория
Клонирование репозитория в папку domains
```shell
cd domains
git clone https://github.com/Nuggit334/2group.ru.git
```
Перейдем в папку с проектом и установим composer-зависимости
```shell
cd  2group.ru
composer install
```
Скопируем файл .env.example в файл .env
```shell
copy .env.example .env
```
Генерируем ключ щифрования
```shell
php artisan key:generate
```
Меняем файл конфигурации .env (пример для БД MySql)
```php
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Имя_БД
DB_USERNAME=Логин_пользователя_БД
DB_PASSWORD=Пароль_пользователя_БД

SESSION_DRIVER=file
```
