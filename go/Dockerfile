FROM golang:latest AS builder

WORKDIR /usr/src/app

COPY ./go/app/ .

RUN go build fullcycle.go

FROM scratch

COPY --from=builder /usr/src/app .

CMD [ "./fullcycle" ]

