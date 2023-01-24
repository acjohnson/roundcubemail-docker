FULLTAG=roundcube/roundcubemail:1.6.1-apache-custom
DOCKERFILE=Dockerfile
all: buildx

buildx:
	docker buildx build -t $(FULLTAG) --output type=docker -f $(DOCKERFILE) .

rebuild:
	docker buildx build --no-cache -t $(FULLTAG) --output type=docker -f $(DOCKERFILE) .

push: buildx
	docker push $(FULLTAG)

