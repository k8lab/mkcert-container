FROM golang:1.22.5-alpine3.20

RUN apk update && \
    apk add git && \
    cd src && \
    git clone https://github.com/FiloSottile/mkcert.git && \
    cd mkcert && \
    go build -ldflags "-X main.Version=$(git describe --tags)"

FROM alpine:3.20.1
COPY --from=0 /go/src/mkcert/mkcert /usr/local/bin