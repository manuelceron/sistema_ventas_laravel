mkdir poslaravel
cd poslaravel
git clone git@github.com:manuelceron/sistema_ventas_laravel.git ./
(para la fecha actual sirve eliminar el archivo composer.lock antes de ejecutar composer install)    
composer install

para el caso de xampp o similares crear una base de datos

por ejemplo con el nombre poslaravel
en el archivo .env
para crear el archivo .env debe crearlo en base al archivo
 .env.example

especificar también los datos de acceso a la base de datos

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=poslaravel
DB_USERNAME=root
DB_PASSWORD=

php artisan key:generate
php artisan:migrate
php artisan db:seed

https://localhost/poslaravel
email : admin@correo.com
password : admin