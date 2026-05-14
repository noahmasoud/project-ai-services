REGISTRY?=icr.io/ai-services-private
<<<<<<< HEAD:images/python-base/Makefile
IMAGE=python-base
TAG?=v0.0.26
=======
IMAGE=rag-base
TAG?=v0.0.27
>>>>>>> origin/main:images/rag-base/Makefile
CREDS_ARG := $(if $(and $(REGISTRY_USER),$(REGISTRY_PASSWORD)),--creds="$(REGISTRY_USER):$(REGISTRY_PASSWORD)")

CONTAINER_BUILDER?=podman
build:
	cd prebuilder && $(CONTAINER_BUILDER) build -t prebuilder . && cd -
	$(CONTAINER_BUILDER) build -t $(REGISTRY)/$(IMAGE):$(TAG) .
.PHONY: build

push:
	$(CONTAINER_BUILDER) push $(CREDS_ARG) $(REGISTRY)/$(IMAGE):$(TAG)
.PHONY: push

image-tag:
	@echo $(TAG)
.PHONY: image-tag
