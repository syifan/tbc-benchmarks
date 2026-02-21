# Chat Application

## What do you want to build?

Build a real-time chat application in TypeScript/Node.js using WebSockets that supports multiple chat rooms, user authentication, message history persistence, and file sharing. The application should include both a server (Node.js with Express and Socket.IO) and a web-based client with a clean, responsive UI. Messages should be delivered instantly to all connected users in a room.

The implementation must include:
- WebSocket server using Socket.IO with room-based message routing
- User authentication and session management (JWT or session cookies)
- Multiple chat rooms: users can create, join, and leave rooms
- Message persistence: store chat history in a database (SQLite or PostgreSQL)
- File sharing: upload files, share links in chat, store files on server
- User presence: show who's online in each room, typing indicators
- Message features: timestamps, user avatars, markdown rendering
- Web client: responsive React or vanilla TypeScript UI with real-time updates
- Private direct messages between users

## How do you consider the project is success?

1. Messages sent in a room are delivered to all connected users in that room within 100ms
2. User authentication works correctly with signup, login, and protected routes
3. Chat history is persisted and loads when users join a room, showing last 100 messages
4. File upload and sharing works for images and documents up to 10MB with proper MIME type handling
5. User presence accurately shows online/offline status and typing indicators update in real-time
6. Supports at least 50 concurrent users across multiple rooms without message loss or performance degradation
7. Test suite with at least 20 tests covering WebSocket events, authentication, message routing, and file upload
8. UI is responsive and works on desktop and mobile browsers with clean design
