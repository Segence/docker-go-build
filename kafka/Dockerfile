FROM golang:1.26.3-alpine3.23

ENV PATH="/go/bin:${PATH}"
ENV GO111MODULE=on
ENV CGO_ENABLED=1
ENV GOOS=linux

RUN apk --no-cache add ca-certificates=20260413-r0
RUN apk update && \
    apk upgrade && \
    apk --no-cache add build-base=0.5-r3 librdkafka=2.12.1-r0 && \
    rm -rf /var/cache/apk/*

WORKDIR /go
