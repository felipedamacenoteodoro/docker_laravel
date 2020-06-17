FROM golang:1.14.4-alpine3.12 as builder

WORKDIR $GOPATH/src/
COPY hello-world.go .
RUN go build -o /go/app

FROM scratch
COPY --from=builder /go/app /go/app

CMD ["/go/app"]
