.PHONY: build
newtag ?= latest
image = wicksy/synology

build:
	docker build --no-cache=true -t "${image}:latest" .
	docker tag "${image}:latest" "${image}:${newtag}"

testbuild:
	docker build -t "${image}:testing" .

