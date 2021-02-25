FROM golang:1.14-alpine
ENV PORT=4001
WORKDIR /go/src
COPY . .
RUN go build
CMD ["./vuego-demoapp"] 
EXPOSE 4001