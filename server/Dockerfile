FROM golang:1.16-alpine

WORKDIR /app

COPY go.mod ./
COPY go.sum ./
RUN go mod download

COPY *.go ./
RUN go build -o /docker-gs-ping

EXPOSE 4000

CMD [ "/docker-gs-ping" ]
