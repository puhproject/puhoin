.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/puhproject/puhoin/cmd/swarm
	go build -o bin/geth     github.com/puhproject/puhoin/cmd/geth
	go build -o bin/bootnode github.com/puhproject/puhoin/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/puhproject/puhoin/swarm/...
