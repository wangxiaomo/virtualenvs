run:
	docker run -d --link=mysql:mysql --link=redis:redis -v `pwd`/www:/var/www/html -p 80:80 --name laravel laravel
build:
	docker build -t laravel .
php-ini:
	wget https://raw.githubusercontent.com/php/php-src/master/php.ini-production -O php.ini
