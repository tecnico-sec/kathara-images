.PHONY: base sirsbase quagga frr sdn all pushall

all: base sirsbase quagga frr sdn

pushall:
	docker push xtrm0/sirsbase:debian10
	docker push xtrm0/quagga:debian10
	docker push xtrm0/frr:debian10
	docker push xtrm0/sdn:debian10
	docker tag xtrm0/sirsbase:debian10 xtrm0/sirsbase:latest
	docker tag xtrm0/quagga:debian10 xtrm0/quagga:latest
	docker tag xtrm0/frr:debian10 xtrm0/frr:latest
	docker tag xtrm0/sdn:debian10 xtrm0/sdn:latest
	docker push xtrm0/sirsbase:latest
	docker push xtrm0/quagga:latest
	docker push xtrm0/frr:latest
	docker push xtrm0/sdn:latest

base:
	docker pull kathara/base:debian10

sirsbase: base
	cd sirsbase && docker build -t xtrm0/sirsbase:debian10 .

quagga: sirsbase
	cd quagga && docker build -t xtrm0/quagga:debian10 .

frr: sirsbase
	cd frr && docker build -t xtrm0/frr:debian10 .

sdn: sirsbase
	cd sdn && docker build -t xtrm0/sdn:debian10 .
