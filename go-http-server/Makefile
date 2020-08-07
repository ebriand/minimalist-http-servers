build:
	docker image build -t go-http-server .
run:
	docker container run -p 80:80 --rm --read-only --cap-drop all --cap-add NET_BIND_SERVICE go-http-server
