FROM golang:1.16

WORKDIR /go/src/app
# recommended by docker hub page. or /myownapp found on telegram
COPY . .

ENV PORT=8080

RUN go get -d -v ./...
RUN go install -v ./...
RUN go build
#RUN go test ./...

CMD ./server

#build and run from Docker hub
#$ sudo docker build -t golang-app .
#$ sudo docker run -it -p 8080:8080 --rm --name my-running-app golang-app

#${variable:-word} indicates that if variable is set then the result will be that value. If variable is not set then word will be the result.
