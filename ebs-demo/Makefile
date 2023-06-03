ROOT := $(shell pwd)
SOURCEDIR=./
EBS_METRICS_SOURCES=$(shell find $(SOURCEDIR) -name '*.go')

EBS_METRICS_DIR=$(SOURCEDIR)
EBS_METRICS_BINARY=$(ROOT)/bin/ebs-demo-binary

$(EBS_METRICS_BINARY): $(EBS_METRICS_SOURCES)
	rm -rf $(ROOT)/tar-files
	CGO_ENABLED=0 go build -o $(EBS_METRICS_BINARY) $(EBS_METRICS_DIR)

.PHONY: build-ebs-demo-image
build-ebs-demo-image: $(EBS_METRICS_BINARY)
	./ebs-demo-image

