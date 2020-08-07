FROM busybox

RUN addgroup -g 1000 http \
    && adduser -u 1000 -G http -D http

WORKDIR /http

COPY --chown=http:http index.html .

ENTRYPOINT ["httpd","-f","-u","http:http"]
