PROJECT ?= k8s-staging-perf-tests
IMG = gcr.io/$(PROJECT)/perf-tests-util/network/netperfbenchmark
TAG = 0.4

all: push

.PHONY: build
build: cmd
	docker build --pull -t $(IMG):$(TAG) .
	@echo Built $(IMG):$(TAG)

.PHONY: push
push: build
	docker push $(IMG):$(TAG)
	@echo Pushed $(IMG) with :$(TAG) tag
