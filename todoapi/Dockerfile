FROM golang:latest

LABEL maintainer="Ye Htet Aung <yehtetag.y@gmail.com>"

COPY todolist.go /go/src

WORKDIR /go/src

RUN go mod init todoapp/todoapi && \
    go mod tidy && \
    go build 
