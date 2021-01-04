FROM golang:1.13-alpine AS builder

RUN apk add --update --no-cache ca-certificates git
RUN mkdir -p /build
WORKDIR /build
COPY go.* /build
RUN go mod download
COPY ./admission-controller /build
RUN CGO_ENABLED=0 GOOS=linux go build -a -o /admission-controller /build

FROM amazonlinux

COPY --from=builder /admission-controller /admission-controller
COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
RUN chmod -R +x /admission-controller
CMD ["/admission-controller"]
