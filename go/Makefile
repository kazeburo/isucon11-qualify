all: deploy_remote

deploy_remote:
	ssh 192.168.0.11 'cd webapp/go && make deploy'
	ssh 192.168.0.12 'cd webapp/go && make deploy'
	ssh 192.168.0.13 'cd webapp/go && make deploy'

deploy: build
	sudo service isucondition.go restart

build: pull
	PATH=/home/isucon/local/go/bin/:$(PATH) ;\
	go build

pull:
	git pull
