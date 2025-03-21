IMAGE_NAME = fastapi-app
CONTAINER_NAME = fastapi-container
PORT = 8000

build:
	docker build -t $(IMAGE_NAME) .

run:
	docker run -d --name $(CONTAINER_NAME) -p $(PORT):8000 $(IMAGE_NAME)

logs:
	docker logs -f $(CONTAINER_NAME)

stop:
	docker stop $(CONTAINER_NAME)

rm:
	docker rm -f $(CONTAINER_NAME)

rmi:
	docker rmi -f $(IMAGE_NAME)

rebuild: stop rm rmi build run

shell:
	docker exec -it $(CONTAINER_NAME) /bin/sh
