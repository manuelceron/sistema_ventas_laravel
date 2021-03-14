# Instalar Composer y Git
# En la consola de Git, terminal o cmd
# Ir a la carpeta public_html, www o htdocs
cd C:/xampp/htdocs
# crear la carpeta deseada, por ejemplo poslaravel
mkdir poslaravel
# ingresar a la carpeta
cd poslaravel
# Ejecutar el comando git para clonar el repositorio
git clone git@github.com:manuelceron/sistema_ventas_laravel.git ./
#
# (para la fecha actual sirve eliminar el archivo composer.lock antes de ejecutar composer install)    
# Ejecutar composer para instalar dependencias
composer install
# (Tambien sirve composer update)
#
# para el caso de xampp o similares crear una base de datos
#
# por ejemplo con el nombre poslaravel
# en el archivo .env
# para crear el archivo .env debe crearlo en base al # archivo
.env.example
#
# especificar también los datos de acceso a la base de datos

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=poslaravel
DB_USERNAME=root
DB_PASSWORD=
# Ejecutar el comando key generate para crear una llave necesaria para la configuración del proyecto
php artisan key:generate
# en base de datos se debe crear una base de datos con los datos anteriormente suministrados, si ya henos hecho esto, entonces ya podremos ejecutar los 2 comandos siguintes:
php artisan:migrate
php artisan db:seed
# para ingresar debemos acceder al enlace
https://localhost/poslaravel
# las credenciales que se encuentran en el sedder por defecto son:
email : admin@correo.com
password : admin