
<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

To run a Laravel app downloaded from GitHub on your system and ensure all dependencies are installed, follow these steps:

Step 1: Clone the Repository
If you haven't already cloned the project, use git to clone the Laravel project from GitHub.

```php
git clone https://github.com/username/repository-name.git
cd repository-name
```
Step 2: Install Dependencies with Composer
Laravel uses Composer to manage its dependencies. Run the following command in your project directory to install all required packages:

```php
composer install
```
This will install all the dependencies listed in the composer.json file.

Step 3: Set Up Environment Variables
Create the .env file: Laravel requires a .env file for environment variables. Most Laravel projects come with a .env.example file. You can copy it to create a new .env file.
```php
cp .env.example .env
```
Configure the .env file: Open the .env file and set up your environment variables. You'll need to configure database settings, app URL, and other settings such as mail, cache, etc.
dotenv
Copy code
APP_NAME=Laravel
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
Step 4: Generate the Application Key
Laravel requires an application key to be set. You can generate this by running:

```php
php artisan key:generate
```
This will set the APP_KEY in your .env file.

Step 5: Set Up the Database
Create the database: Make sure the database you specified in the .env file exists. You can create it via your database management tool (e.g., MySQL, PostgreSQL) or via the command line:
```php
CREATE DATABASE your_database;
```
Run Migrations: Run Laravel migrations to set up your database schema:
```php
php artisan migrate
```
If the project contains seeders to populate the database with initial data, run:

```php
php artisan db:seed
```
Step 6: Run the Application
To serve the Laravel application locally, you can use the built-in Laravel development server:

```php
php artisan serve
```
You should now be able to access your Laravel application at http://localhost:8000 (or a custom URL if specified in .env).

Step 7: Additional Steps (Optional)
Install Node.js Dependencies: If the project has front-end assets (like Vue, React, or Blade components), install the Node.js dependencies and compile them:
```php
npm install
npm run dev
```
To avoid run all time npm run dev for login UI not to be broken use code:
```php
npm run build
```
This will add the path for:
public/build/manifest.json              0.28 kB │ gzip:  0.15 kB
public/build/assets/app-DBEl1KqF.css  227.39 kB │ gzip: 30.87 kB
public/build/assets/app-CXpObi_1.js   117.01 kB │ gzip: 38.54 kB

Cache Clearing: If you're having issues with configuration or routing, clear the cache:
```php
php artisan config:clear
php artisan cache:clear
php artisan route:clear
php artisan view:clear
```
Summary:
Clone the repository.
Install dependencies using composer install.
Copy the .env.example file to .env and configure it.
Generate an application key using php artisan key:generate.
Set up your database and run migrations (php artisan migrate).
Run the app with php artisan serve.
With these steps, your Laravel app should be up and running on your system!

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[WebReinvent](https://webreinvent.com/)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Jump24](https://jump24.co.uk)**
- **[Redberry](https://redberry.international/laravel/)**
- **[Active Logic](https://activelogic.com)**
- **[byte5](https://byte5.de)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
