ROOT := $(shell pwd)
BINARY=$(ROOT)/temp-bin/ebs-demo-binary

$(BINARY):
	./build-ebs-demo-binary

.PHONY: build-ebs-demo-image
build-ebs-demo-image: $(BINARY)
	./build-ebs-demo-image

