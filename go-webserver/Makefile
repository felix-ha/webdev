.PHONY: docker_build
docker_build:
	docker build --tag go-webserver .

.PHONY: docker_run
docker_run:
	docker run --publish 80:8080 --name go-webserver --rm go-webserver

.PHONY: docker_request
docker_request:
	curl -i http://0.0.0.0:80/json

.PHONY: download_request
download_request:
	curl -H "Content-Type: application/json" -d '{"filename": "file.txt"}' -i http://0.0.0.0:80/download

