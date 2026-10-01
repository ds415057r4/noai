FROM golang:1.21 AS builder
WORKDIR /app
COPY <<-EOF main.go
package main

import "fmt"

func main() { fmt.Println("Hello World") }
EOF

ENV CGO_ENABLED=0

RUN go mod init hello \
&& go mod tidy \
&& go build -o hello main.go

FROM scratch

COPY --from=builder /app/hello /hello

CMD ["/hello"]
