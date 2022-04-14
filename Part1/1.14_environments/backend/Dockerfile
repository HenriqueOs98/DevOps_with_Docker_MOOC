FROM golang:1.16

WORKDIR /usr/src/app 
EXPOSE 8080
COPY ./example-backend .
ENV REQUEST_ORIGIN=http://localhost:5000
RUN go build

CMD ./server