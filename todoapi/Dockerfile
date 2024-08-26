FROM golang:latest AS builder

LABEL maintainer="Ye Htet Aung <yehtetag.y@gmail.com>"

COPY todolist.go /go/src

WORKDIR /go/src

RUN go mod init todoapp/todo-api && \
    go mod tidy && \
    go build .

FROM ubuntu
WORKDIR /app
COPY --from=builder /go/src/todo-api /app
CMD ["/app/todo-api"]

