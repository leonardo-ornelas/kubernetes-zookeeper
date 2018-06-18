VERSION=latest
PROJECT=ornelas

all: build

build:
	docker build --pull -t ${PROJECT}/kubernetes-zookeeper:${VERSION} .

push: build
	docker push ${PROJECT}/kubernetes-zookeeper:${VERSION}

.PHONY: all build push

