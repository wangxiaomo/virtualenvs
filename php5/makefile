run:
	docker run -d --link=mysql:mysql --link=redis:redis -v `pwd`/www:/var/www/html -P --name php5 php5
build:
	docker build -t php5 .
php-ini:
	wget https://raw.githubusercontent.com/php/php-src/master/php.ini-production -O php.ini
