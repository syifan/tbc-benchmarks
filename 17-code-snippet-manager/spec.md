# Code Snippet Manager

## What do you want to build?

Build a code snippet manager in Rust with both a CLI and TUI (terminal UI) for storing, organizing, and searching code snippets. The tool should support syntax highlighting, tagging, full-text search, and optional Git synchronization for backup and sharing across machines. Snippets are stored locally in a structured format with metadata, and the TUI provides an interactive browsing and editing experience.

The implementation must include:
- Snippet storage: save code with language, title, description, tags, and timestamps
- Syntax highlighting in the terminal using a library (syntect or similar)
- CLI commands: `add`, `edit`, `delete`, `list`, `search`, `show`
- TUI (using ratatui or tui-rs): interactive interface for browsing, searching, and editing snippets
- Full-text search: search in title, description, tags, and code content
- Tagging system: assign multiple tags, filter by tags
- Git sync: optionally initialize a Git repository for snippets and push/pull to remote
- Export/import: export snippets to JSON or markdown, import from files
- Support for 20+ programming languages with syntax highlighting

## How do you consider the project is success?

1. Can add, edit, delete, and view snippets through both CLI and TUI interfaces
2. Syntax highlighting works correctly for at least 20 languages (Rust, Python, Go, JavaScript, C++, Java, etc.)
3. Full-text search returns relevant results in under 50ms for 1000+ snippets
4. Tagging and filtering work correctly — can filter by multiple tags with AND/OR logic
5. TUI provides smooth keyboard navigation with Vim-style keybindings and responsive rendering
6. Git sync correctly initializes repository, commits changes, and supports push/pull to remote
7. Test suite with at least 15 tests covering snippet CRUD, search, tagging, and Git operations
8. Export produces valid JSON and markdown files that can be re-imported without data loss
