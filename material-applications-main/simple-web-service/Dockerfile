FROM golang:1.15 AS build

WORKDIR /usr/src/app

COPY . .

RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build

FROM scratch

COPY --from=build /usr/src/app/simple-web-service /usr/src/app/server

WORKDIR /usr/src/app/

ENTRYPOINT [ "/usr/src/app/server" ]
