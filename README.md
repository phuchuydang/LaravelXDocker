# Docker config

## Stack technique

- Docker & Docker compose
- PHP 8.3
- Laravel 11.1 (Back)
- MySQL 8.0

## Installation

From the "Terminal" tab, and run the following command.

1. Go to the root folder: `cd LaravelXDocker`
2. Copy the .env file: 
   - Linux: `cp .env.dist .env`
   - Windows: `copy .env.dist .env`
3. Creates and start the containers: `docker-compose up --build `
4. Go inside php container: `docker exec -it php /bin/sh`
5. Install the dependencies: `composer install`
6. Grant permissions to the storage folder:
    - `chown -R www-data:www-data /home/source/main`
    - `chmod -R 775 /home/source/main/storage`
    - `chmod -R 775 /home/source/main/bootstrap/cache`
7. Copy the .env file: 
    - Linux: `cp .env.example .env`
    - Windows: `copy .env.example .env`
8. Generate the key: `php artisan key:generate`
9. Run the migrations: `php artisan migrate`

## Usage
1. To access the site: http://localhost:8000
2. To access the database: http://localhost:8080
    - User: laravel_user
    - Password: laravel_pwd
    - Database: laravel
