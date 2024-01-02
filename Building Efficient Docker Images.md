Task 1: Create a golang Docker Image to print Hello World
-------------------------------------------------------------
mkdir large optimal && cd large	
vi helloworld.go

package main
import "fmt"
func main() {
fmt.Println("hello world")
}


vi Dockerfile
FROM golang:1.12.5
WORKDIR /app
COPY helloworld.go .
RUN GOOS=linux go build -a -installsuffix cgo -o helloworld .
CMD ["./helloworld"]

docker build -t hello-go:v1 .

docker run hello-go:v1
-------------------------------------------------------------
Task 2: Create an optimal Docker Image using Multi-stage Dockerfile
-------------------------------------------------------------
cd ../optimal

vi Dockerfile

FROM golang:1.12.5 AS stage1
WORKDIR /app
COPY helloworld.go .
RUN GOOS=linux go build -a -installsuffix cgo -o helloworld .

FROM alpine:3.9.3
WORKDIR /root
COPY --from=stage1 /app/helloworld .
CMD ["./helloworld"]


cp ../large/helloworld.go .

docker build -t hello-go:v2 .

docker run hello-go:v2

docker image ls
docker history hello-go:v1

docker history hello-go:v2
