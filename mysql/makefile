run:
	docker run -d -v `pwd`/data:/var/lib/mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=coldwar2 --restart=unless-stopped --name mysql mysql:latest
