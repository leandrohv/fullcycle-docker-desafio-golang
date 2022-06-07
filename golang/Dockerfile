FROM golang:1.18.3-alpine3.16 AS builder

WORKDIR /usr/src/main

COPY . .

RUN go build ./main.go

FROM scratch

WORKDIR /usr/src/main

COPY --from=builder /usr/src/main .

ENTRYPOINT ["./main"]
