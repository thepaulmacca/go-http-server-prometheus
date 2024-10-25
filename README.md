# Go HTTP Server with Prometheus Instrumentation

A very simple Go HTTP Server with Prometheus instrumentation that adds a counter metric to keep count of the total number of requests processed by the server.

## Run Server

### Local

`go run server.go`

### Docker

`docker compose up --build`

Now open [http://localhost:8090/ping](http://localhost:8090/ping) in your browser and you'll see `pong`.

Go to [http://localhost:8090/metrics](http://localhost:8090/metrics) to view the metrics where you'll see:

```yaml
# HELP ping_request_count Number of requests handled by the Ping handler
# TYPE ping_request_count counter
ping_request_count 1
```

Keep hitting the `ping` endpoint to see the counter increase.
