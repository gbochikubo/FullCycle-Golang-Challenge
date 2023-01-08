FROM golang:1.8 AS builder
WORKDIR /app
COPY full-cycle.go ./
RUN go build -o /full-cycle

FROM scratch
WORKDIR /
COPY --from=builder /full-cycle /full-cycle
ENTRYPOINT ["./full-cycle"]