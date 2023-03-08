.PHONY: serve
serve: build-docker-image
	docker run -d -v ${PWD}:/usr/src/app/volume -p 8081:9080 localhost/docker-serve-static
	echo "visit http://localhost:8081"

.PHONY: build-docker-image
build-docker-image:
	docker build -t localhost/docker-serve-static .

compile-sass:
	sass --watch scss/style.scss css/style.css &
