FROM golang:1.21 AS builder
WORKDIR /app
COPY . .
ENV CGO_ENABLED=0
RUN go mod init go-http \
&& go mod tidy \
&& go build -o hello .

FROM scratch
COPY --from=builder /app/hello /hello
ENTRYPOINT ["/hello"]
