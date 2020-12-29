# FROM amazonlinux
# COPY ./admission-controller /admission-controller
# RUN chmod +x /admission-controller
# ENTRYPOINT ["/admission-controller"]

FROM golang:1.13-alpine AS builder

# RUN apk add --update --no-cache ca-certificates git
RUN mkdir -p /admission-controller
COPY ./admission-controller /admission-controller
WORKDIR /admission-controller
CMD ["/admission-controller"]
# ENTRYPOINT ["/admission-controller"]
# RUN CGO_ENABLED=0 GOOS=linux go build -a -o /admission-controller ./cmd/admission-controller/

# FROM alpine:3.10

# COPY --from=builder /admission-controller /admission-controller
# COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
# CMD ["/admission-controller"]
