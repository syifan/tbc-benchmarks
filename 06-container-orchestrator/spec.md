# Container Orchestrator

## What do you want to build?

Build a simplified container orchestrator in Go that manages Docker containers across multiple worker nodes. Think of it as a minimal Kubernetes — scheduling workloads, monitoring health, and providing a CLI and API for management.

The implementation must include:
- Control plane with REST API
- Worker agent that runs on each node and manages local containers (via Docker API)
- Scheduler: bin-packing and spread strategies based on CPU/memory requests
- Health checking: HTTP, TCP, and command-based probes with configurable intervals
- Service abstraction: group containers, automatic restart on failure
- Rolling updates: deploy new versions with configurable parallelism and rollback on failure
- Networking: assign containers to a shared bridge network, expose services via port mapping
- Persistent state: store cluster state in an embedded database (BoltDB or SQLite)
- CLI tool: deploy, scale, inspect, logs, delete services
- Web dashboard showing cluster state, services, and container health

## How do you consider the project is success?

1. Deploy a 3-container web application (nginx + app + redis) across 2 worker nodes via CLI
2. Killing a container triggers automatic restart within 30 seconds
3. Rolling update replaces containers one-by-one with zero downtime (validated by continuous health check during update)
4. Scheduler respects CPU/memory constraints — rejects deployments that exceed cluster capacity
5. `ctl logs <service>` streams aggregated logs from all containers in a service
6. Web dashboard shows real-time cluster state (nodes, services, containers, health status)
7. Cluster survives control plane restart — state is fully recovered from persistent storage
8. Test suite with at least 30 tests covering scheduling, health checks, updates, and failure recovery
