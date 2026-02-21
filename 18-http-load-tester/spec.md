# HTTP Load Tester

## What do you want to build?

Build an HTTP load testing tool in Go that sends concurrent requests to a target URL, measures latency and throughput, calculates percentiles (p50, p95, p99), supports different load patterns (constant, ramp-up, spike), and generates HTML reports with charts. The tool should provide a CLI for configuring tests and produce detailed metrics similar to tools like wrk or Apache Bench, but with more sophisticated load patterns and better reporting.

The implementation must include:
- Concurrent HTTP requests using goroutines with configurable concurrency level
- Load patterns: constant rate, linear ramp-up, step ramp-up, and spike testing
- Metrics collection: requests per second, latency (min, max, mean, median, p95, p99), success rate, error distribution
- Request customization: custom headers, body, HTTP method (GET, POST, PUT, DELETE)
- Duration or request count limits with timeout handling
- HTML report generation: charts showing latency over time, throughput, percentile distribution
- CSV export for raw data analysis
- CLI with intuitive interface: `loadtest --url https://example.com --concurrency 100 --duration 60s --ramp-up 10s`

## How do you consider the project is success?

1. Correctly executes load tests with specified concurrency and duration, sending accurate number of requests
2. Latency measurements are accurate within 5% compared to system timestamps
3. Percentile calculations (p50, p95, p99) match statistical expectations for the recorded latencies
4. Supports ramp-up: smoothly increases concurrency from 0 to target over specified duration
5. HTML report displays interactive charts (using Chart.js or similar) with latency over time and percentile distribution
6. Handles at least 10,000 requests per second on modern hardware with accurate metrics
7. Test suite with at least 15 tests covering concurrent execution, metrics calculation, load patterns, and report generation
8. Error handling gracefully manages timeouts, connection failures, and HTTP errors with proper categorization
