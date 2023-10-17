FROM golang:1.21

# Set working catalog inside the container
WORKDIR /var/www

# Copy and install dependencies of modules
COPY go.mod ./
COPY go.sum ./
RUN go mod download

# Copy source to container
COPY . .

# Build the app
RUN go build -o myapp

# CMD ["go", "run", "main.go"]
CMD ["./myapp"]
