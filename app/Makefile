.PHONY: start build publish

export GOBIN=${CURDIR}/bin

version ?= master

$(GOBIN)/air:
	go install github.com/air-verse/air@latest

start: $(GOBIN)/air
	$(GOBIN)/air

build:
	#docker build . --tag ghcr.io/ipakyulibank/devops-test-task1/test-app:$(version)
	docker build . --tag ghcr.io/jamshiddint/devops-test-task1/test-app:$(version)


publish:
	#docker push ghcr.io/ipakyulibank/devops-test-task1/test-app:$(version)
	docker push ghcr.io/jamshiddint/devops-test-task1/test-app:$(version)
	
