run:
	docker run -d --link=mysql:mysql --link=redis:redis -v `pwd`/www:/var/www/html -P --name php dev_php
build:
	docker build -t dev_php .
php-ini:
	wget https://raw.githubusercontent.com/php/php-src/master/php.ini-production -O php.ini
