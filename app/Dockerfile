FROM golang:1.24

WORKDIR /app

COPY . .

RUN go build -o app

CMD /app/app

#FROM golang:1.24 AS builder

# WORKDIR /app
# COPY . .
# RUN go build -o app
# RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o app
# FROM alpine:3.19
# RUN apk --no-cache add ca-certificates
# WORKDIR /app
# COPY --from=builder /app/app .
# CMD ["/app/app"]
