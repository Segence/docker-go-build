FROM golang:1.26.3-alpine3.23

# ARG LIBRDKAFKA_VERSION=v2.14.0

ENV PATH="/go/bin:${PATH}"
ENV GO111MODULE=on
ENV CGO_ENABLED=1
ENV GOOS=linux

RUN apk --no-cache add ca-certificates=20260413-r0
RUN apk update && \
    apk upgrade && \
    # apk --no-cache add pkgconf=2.5.1-r0 git=2.52.0-r0 bash=5.3.3-r1 build-base=0.5-r3 sudo=1.9.17_p2-r0 && \
    apk --no-cache add librdkafka=2.12.1-r0 && \
    rm -rf /var/cache/apk/*


# RUN git clone --depth 1 --branch ${LIBRDKAFKA_VERSION} https://github.com/confluentinc/librdkafka /tmp/librdkafka

# WORKDIR /tmp/librdkafka
# RUN ./configure --prefix /usr && make && make install

WORKDIR /go

# RUN rm -rf /tmp/librdkafka