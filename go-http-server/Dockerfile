FROM golang:1.14

WORKDIR /go/src/app

COPY main.go .

RUN CGO_ENABLED=0 go build -a -v -tags netgo -ldflags '-w -extldflags "-static"' -o http-server *.go

FROM scratch

COPY --from=0 /go/src/app/http-server .

COPY index.html /static/

ENTRYPOINT ["/http-server"]
