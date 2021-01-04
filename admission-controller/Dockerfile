# FROM amazonlinux
# COPY ./admission-controller /admission-controller
# RUN chmod +x /admission-controller
# ENTRYPOINT ["/admission-controller"]

# FROM golang:1.13-alpine AS builder

# RUN apk add --update --no-cache ca-certificates git
# RUN mkdir -p /build
# WORKDIR /build
# COPY go.* /build
# RUN go mod download
# COPY . /build
# RUN CGO_ENABLED=0 GOOS=linux go build -a -o /admission-controller ./admission-controller/

FROM alpine:3.10

COPY ./admission-controller /admission-controller
RUN chmod -R +x /admission-controller
CMD ["/admission-controller"]
# COPY --from=builder /admission-controller /admission-controller
# COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
# CMD ["/admission-controller"]
