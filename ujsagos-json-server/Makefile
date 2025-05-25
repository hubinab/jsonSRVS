IMAGE_NAME=rcsnjszg/ujsagos-json-server
CONTAINER_NAME=ujsagos-json-server
VERSION=latest
PORT=8888

.DEFAULT_GOAL := build

.PHONY: build run stop rm clean

build:
	docker build -t $(IMAGE_NAME):$(VERSION) .

run:
	docker run -d --name $(CONTAINER_NAME) -p $(PORT):3000 -v /app/node_modules $(IMAGE_NAME):$(VERSION)


stop:
	docker stop $(CONTAINER_NAME)

rm:
	docker rm $(CONTAINER_NAME)

clean:
	docker rmi $(IMAGE_NAME):$(VERSION)


