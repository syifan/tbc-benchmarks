# Task Scheduler / Cron System

## What do you want to build?

Build a task scheduler in Go that parses cron expressions, manages scheduled jobs, handles retries on failure, and provides a web UI for monitoring. The system should execute tasks at specified times, support different execution strategies (immediate, scheduled, recurring), persist job state to survive restarts, and provide detailed execution logs. Similar to cron but with a modern API and dashboard.

The implementation must include:
- Cron expression parser supporting standard 5-field syntax (minute, hour, day, month, weekday)
- Job scheduler that executes tasks at the correct times with second-level precision
- Job types: one-time, recurring (cron), and interval-based (every N minutes)
- Retry logic: configurable retry attempts with exponential backoff on failure
- Job persistence: save job definitions and execution state to SQLite
- Web dashboard: view active jobs, execution history, logs, and manage jobs (pause, resume, delete)
- REST API for programmatic job management
- Concurrent execution: run multiple jobs in parallel with configurable worker pool

## How do you consider the project is success?

1. Cron parser correctly handles standard expressions: `*/5 * * * *`, `0 9 * * MON-FRI`, `0 0 1 * *`
2. Jobs execute within 1 second of their scheduled time under normal load
3. Failed jobs retry according to configured policy (max attempts, backoff) and are marked failed after exhausting retries
4. Job state persists across process restarts — scheduled jobs resume after crash/restart
5. Web UI displays active jobs, upcoming executions, and execution history with filtering and search
6. Handles at least 1000 concurrent jobs with different schedules without missing executions
7. Test suite with at least 18 tests covering cron parsing, scheduling, retries, persistence, and concurrent execution
8. REST API provides endpoints for CRUD operations on jobs and querying execution status
