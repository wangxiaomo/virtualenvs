build:
	docker build -t ss-mgr .

node-up:
	docker run --name ss-node --rm -it \
	-v `pwd`/ssmgr:/root/.ssmgr \
	-p 4001:4001 -p 50000-50010:50000-50010 \
	-e SS_MANAGER_ADDRESS=127.0.0.1:4000 \
	--link mysql:mysql ss-mgr

master-up:
	docker run --name ss-master --rm -it \
	-v `pwd`/ssmgr:/root/.ssmgr \
	-v `pwd`/www:/usr/lib/node_modules/shadowsocks-manager \
	-p 9999:80 -p 4001:4001 -p 50000-50009:50000-50009 \
	-e SS_MANAGER_WEBGUI=true -e SS_MANAGER_ADDRESS=127.0.0.1:4000 \
	--link mysql:mysql ss-mgr
