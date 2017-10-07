run:
	docker run -d -v `pwd`/data:/data -p 127.0.0.1:6379:6379 --restart=unless-stopped --name redis redis

redis-conf:
	wget https://raw.githubusercontent.com/antirez/redis/unstable/redis.conf -O redis.conf

build:
	docker build . -t redis
