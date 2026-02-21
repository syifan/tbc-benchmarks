# Markdown Note-Taking App with Backlinks

## What do you want to build?

Build a markdown note-taking application in TypeScript that supports wiki-style bidirectional linking between notes, a graph visualization of note connections, full-text search, and local storage persistence. The app should run as a single-page web application with a clean, distraction-free interface inspired by tools like Obsidian or Roam Research, but simplified and focused on core features.

The implementation must include:
- Markdown editor with live preview and syntax highlighting
- Wiki-style links using `[[Note Title]]` syntax that creates bidirectional references
- Backlink panel: show all notes that link to the current note
- Graph view: interactive force-directed graph showing note relationships
- Full-text search across all notes with fuzzy matching and highlighting
- Local storage using IndexedDB for persistence
- Note organization: folders/tags for categorization
- Export/import: export all notes as markdown files, import from directory
- Keyboard shortcuts for common actions (new note, search, toggle preview)

## How do you consider the project is success?

1. Markdown rendering works correctly with live preview updating as user types with <100ms latency
2. Wiki links correctly parse `[[Note Title]]` syntax, create clickable links, and track bidirectional references
3. Backlinks panel accurately shows all notes referencing the current note and updates when links change
4. Graph view renders an interactive force-directed graph with nodes (notes) and edges (links) that can be panned, zoomed, and clicked
5. Search returns relevant results in under 100ms for 1000+ notes with fuzzy matching and result highlighting
6. All notes persist in IndexedDB and survive browser refresh/restart
7. Test suite with at least 18 tests covering markdown parsing, wiki links, backlinks, search, and graph generation
8. UI is responsive, keyboard-friendly, and provides a distraction-free writing experience
