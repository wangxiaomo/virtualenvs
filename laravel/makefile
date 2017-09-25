run:
	docker run -d --link=mysql:mysql --link=redis:redis -v `pwd`/www:/var/www/html -p 80:80 --name laravel dev_laravel
build:
	docker build -t dev_laravel .
php-ini:
	wget https://raw.githubusercontent.com/php/php-src/master/php.ini-production -O php.ini
