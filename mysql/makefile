run:
	docker run -d -v `pwd`/data:/var/lib/mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=coldwar2 --name mysql dev_mysql
build:
	docker build -t dev_mysql .
