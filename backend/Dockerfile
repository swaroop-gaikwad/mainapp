
FROM golang:1.19

WORKDIR /app                        

# Copy go modules manifests and download dependencies
COPY go.mod go.sum ./
RUN go mod download

# Copy the source code
COPY . .

# Build the application
RUN go build -o main .

# Set environment variables (modify as needed)
ENV PORT=8080

# Expose the application port
EXPOSE 8080

# Start the application
CMD ["./main"]
