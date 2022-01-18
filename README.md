Pasos:

1) Bajar laravel

git clone https://github.com/laravel/laravel.git nombreProyecto

2) pegar dentro de nombreProyecto -> docker y docker-compose

3) Instalar dependencias con composer
Linux: docker run --rm -v “$(pwd)”:/app composer install
Windows: docker run --rm -v ${pwd}:/app composer install
	

4) Generar key de la aplicación
   docker-compose exec app php artisan key:generate
   docker-compose exec app php artisan optimize


5) Instalar Fortify



a) docker run --rm -v ${pwd}:/app composer require laravel/fortify

b) docker-compose exec app php artisan vendor:publish --provider="Laravel\Fortify\FortifyServiceProvider"
c) docker-compose exec app php artisan migrate

6) Instalar Sactum


a) docker run --rm -v ${pwd}:/app composer require laravel/sanctum

b) docker-compose exec app php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
c) docker-compose exec app php artisan migrate


8) docker-compose up

pd: Si hay un problema con la table de session

docker-compose exec app php session:table
docker-compose exec app php artisan migrate





docker run --rm -v ${pwd}:/app composer install

docker run --rm -v ${pwd}:/app composer 
docker-compose exec app php artisan
docker exec container pwd

Ejecutar Composer
docker-compose exec app sh -c "cd /var/www && npm install"

Ejecutar artisan
docker-compose exec app php artisan inertia:middleware
