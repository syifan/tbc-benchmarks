# Log Aggregator and Alerting System

## What do you want to build?

Build a log aggregation and alerting system in Python that ingests logs from multiple sources (files, syslog), parses them with configurable patterns (regex), detects anomalies or error patterns, sends alerts via email/webhook, and provides a web dashboard for real-time log viewing and historical search. The system should handle high-volume log streams, support custom alert rules, and persist logs to a database for querying.

The implementation must include:
- Log ingestion: tail log files, receive syslog messages over UDP/TCP, and HTTP POST endpoints
- Parsing engine: apply regex patterns to extract structured fields (timestamp, level, message, custom fields)
- Alert rules: define conditions (error rate threshold, specific pattern match, anomaly detection) that trigger notifications
- Notification channels: email (SMTP) and webhooks with configurable templates
- Web dashboard: real-time log streaming, filtering by level/source/time, search with highlighting
- Storage: persist logs to SQLite or PostgreSQL with efficient indexing
- Log rotation: manage disk space with configurable retention policies
- Aggregation: group logs by fields and calculate statistics (count, rate per minute)

## How do you consider the project is success?

1. Successfully ingests logs from at least 3 sources simultaneously (file tail, syslog, HTTP) without message loss
2. Regex parsing correctly extracts structured fields from common log formats (Apache, Nginx, JSON logs)
3. Alert rules trigger notifications correctly when conditions are met (e.g., >10 errors per minute)
4. Alerts sent via email and webhook within 5 seconds of trigger condition
5. Dashboard displays real-time logs with <200ms latency and supports filtering by level, source, and time range
6. Handles at least 1000 log messages per second with efficient storage and indexing
7. Test suite with at least 20 tests covering ingestion, parsing, alert rules, notifications, and search
8. Retention policy correctly deletes old logs based on age or disk usage limits
