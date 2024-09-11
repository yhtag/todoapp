FROM golang:latest AS builder

LABEL maintainer="Ye Htet Aung <yehtetag.y@gmail.com>"

COPY todolist.go /go/src

WORKDIR /go/src

RUN export CGO_ENABLED=0 && \
    go mod init todoapp/todo-api && \
    go mod tidy && \
    go build .

FROM alpine

LABEL maintainer="Ye Htet Aung <yehtetag.y@gmail.com>" \
      description="Required Environment Variables: DB_USER, DB_PASS, DB_HOST, DB_PORT, DB_NAME"

WORKDIR /app
COPY --from=builder /go/src/todo-api /app
CMD ["/app/todo-api"]

