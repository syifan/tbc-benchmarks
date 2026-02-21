# Collaborative Text Editor

## What do you want to build?

Build a real-time collaborative text editor in TypeScript that allows multiple users to edit the same document simultaneously, with changes synchronized via CRDTs (Conflict-free Replicated Data Types). The system should work in a browser with a Node.js backend.

The implementation must include:
- CRDT-based text data structure (e.g., RGA or YATA algorithm) — implemented from scratch
- WebSocket server for real-time synchronization
- Rich text support: bold, italic, headings, bullet lists, code blocks
- Cursor presence: show other users' cursor positions and selections in real-time
- Offline editing with automatic merge on reconnect
- Document persistence (save/load from server)
- Version history: view and restore previous versions
- User authentication (simple token-based)
- Frontend: React-based editor with toolbar, document list, and user presence indicators
- Conflict resolution that preserves user intent (no lost edits)

## How do you consider the project is success?

1. Two users editing the same paragraph simultaneously see each other's changes within 200ms
2. CRDT convergence: after all messages are delivered, all clients show identical document state — validated with a fuzzer that generates 1000 random concurrent operations
3. Offline editing works: disconnect a client, make edits, reconnect — all edits are merged correctly without data loss
4. Rich text formatting is preserved through concurrent edits (e.g., one user bolds while another types)
5. Cursor presence shows correct positions for 5 simultaneous users
6. Version history correctly stores and restores at least 100 versions
7. Server handles 20 simultaneous connections editing the same document without degradation
8. Test suite with at least 30 tests covering CRDT operations, sync protocol, conflict resolution, and offline merge
