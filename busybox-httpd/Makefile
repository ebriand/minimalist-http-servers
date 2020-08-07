build:
	docker image build -t busybox-httpd .
run:
	docker container run -p 80:80 --init --rm --read-only --cap-drop all --cap-add SETGID --cap-add SETUID --cap-add NET_BIND_SERVICE busybox-httpd
