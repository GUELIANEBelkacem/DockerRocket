FROM golang:1.16-alpine

WORKDIR /app

COPY go.mod ./
COPY go.sum ./
RUN go mod download

COPY server.go ./
COPY /users/user.go ./users/
COPY /recipe/recipe.go ./recipe/

RUN go build

EXPOSE 8000

CMD ["go", "run", "server.go"]
