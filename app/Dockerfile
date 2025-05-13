# FROM golang:1.24

# WORKDIR /app

# COPY . .

# RUN go build -o app

# CMD /app/app

FROM golang:1.24 AS builder

WORKDIR /app
COPY . .
RUN go build -o app
FROM alpine:3.19
RUN apk --no-cache add ca-certificates
WORKDIR /app
COPY --from=builder /app/app .
CMD ["/app/app"]
