FROM golang
WORKDIR /task/
COPY go.mod .
COPY go.sum .
RUN go get google.golang.org/grpc
COPY . /task/
RUN go build -o cmd/server.bin cmd/server.go
CMD [ "bash", "-c" ,"/task/cmd/server.bin"]