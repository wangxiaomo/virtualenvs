run:
	docker run \
	  --volume=/:/rootfs:ro \
	  --volume=/var/run:/var/run:rw \
      --volume=/cgroup:/cgroup:ro \
	  --volume=/sys:/sys:ro \
	  --volume=/var/lib/docker/:/var/lib/docker:ro \
	  --volume=/dev/disk/:/dev/disk:ro \
	  --publish=8080:8080 \
      --privileged=true \
	  --detach=true \
	  --name=cadvisor \
	  google/cadvisor:latest
