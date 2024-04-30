<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

# Kit básico de inicio de Docker Laravel 10
Aplicación base de laravel 10 en php 8.2, para sólo preocuparte de usar el framework Laravel.

Se ha usado como base el repositorio de [refactorian](https://github.com/refactorian) / [laravel-docker](https://github.com/refactorian/laravel-docker)


## Kit de inicio de Docker Laravel 10
- Laravel v10.x
- PHP v8.2.x
- MySQL v8.1.x (default)
- MariaDB v10.11
- PostgreSQL v16.x
- pgAdmin v4.x
- phpMyAdmin v5.x
- Mailpit v1.x
- Node.js v18.x
- NPM v10.x
- Yarn v1.x
- Vite v5.x
- Rector v1.x
- Redis v7.2.x

## Requerimientos
- Versión estable de [Docker](https://docs.docker.com/engine/install/)
- Versión compatible de [Docker Compose](https://docs.docker.com/compose/install/#install-compose)

## ¿Cómo implementar?

### ¡Solo por primera vez!
- `git clone https://github.com/jfuentes3002/docker-laravel10-php82-app.git prueba`
- `cd prueba`
- `docker compose up -d --build`
- `docker compose exec php bash`
- `composer setup`

### A partir de la segunda vez
- `docker compose up -d`

## Notas

### App Laravel
- URL: http://localhost

### Mailpit
- URL: http://localhost:8025

### phpMyAdmin
- URL: http://localhost:8080
- Server: `db`
- Username: `refactorian`
- Password: `refactorian`
- Database: `refactorian`

### Adminer
- URL: http://localhost:9090
- Server: `db`
- Username: `refactorian`
- Password: `refactorian`
- Database: `refactorian`

### Comandos básicos de docker compose
- Construir o re-construir servicios
    - `docker compose build`
- Crear e iniciar contenedores
    - `docker compose up -d`
- Detener y eliminar contenedores, redes.
    - `docker compose down`
- Detener todos los servicios
    - `docker compose stop`
- Reiniciar servicio de contenedores
    - `docker compose restart`
- Ejecutar un comando dentro de un contenedor
    - `docker compose exec [container] [command]`

### Comandos útiles de Laravel
- Mostrar información básica sobre su aplicación
    - `php artisan about`
- Elimina la caché de configuración del framework
    - `php artisan config:clear`
- Vaciar el caché de la aplicación
    - `php artisan cache:clear`
- Borrar todos los eventos y oyentes en caché
    - `php artisan event:clear`
- Elimina todos los trabajos de la cola especificada
    - `php artisan queue:clear`
- Elimina la caché del archivo de rutas
    - `php artisan route:clear`
- Limpia todos los archivos de vista compilados
    - `php artisan view:clear`
- Elimina el archivo de clase compilado
    - `php artisan clear-compiled`
- Elimina los archivos de bootstrap en caché
    - `php artisan optimize:clear`
- Elimina los archivos mutex en caché creados por el programador
    - `php artisan schedule:clear-cache`
- Vaciar los tokens de restablecimiento de contraseña caducados
    - `php artisan auth:clear-resets`

### Laravel Pint (Code Style Fixer | PHP-CS-Fixer)
- Formatear todos los archivos
    - `vendor/bin/pint`
- Formatear archivos o directorios específicos
    - `vendor/bin/pint app/Models`
    - `vendor/bin/pint app/Models/User.php`
- Formatear todos los archivos con vista previa
    - `vendor/bin/pint -v`
- Formatear cambios no confirmados según Git
    - `vendor/bin/pint --dirty`
- Inspeccionar todos los archivos
  - `vendor/bin/pint --test`

### Rector
- Prueba de funcionamiento
    - `vendor/bin/rector process --dry-run`
- Proceso
    - `vendor/bin/rector process`

