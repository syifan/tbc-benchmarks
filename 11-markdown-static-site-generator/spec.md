# Markdown Static Site Generator

## What do you want to build?

Build a static site generator in Go that converts a directory of Markdown files into a complete HTML website with templating, live reload during development, and RSS feed generation. The tool should support hierarchical page organization, custom themes, front matter metadata (YAML), and an integrated development server with automatic browser refresh when source files change.

The implementation must include:
- Markdown parser with support for tables, code blocks (syntax highlighting), and inline HTML
- Template engine for layouts, partials, and custom page types
- Front matter parser (YAML) for page metadata (title, date, tags, custom fields)
- Live development server with file watching and browser auto-reload
- RSS/Atom feed generation from blog posts or dated content
- Static asset pipeline (CSS, JS, images) with optional minification
- CLI with commands: `init`, `build`, `serve`, `new-post`
- A test suite and example theme demonstrating the system

## How do you consider the project is success?

1. Correctly parses Markdown files with front matter and renders them using Go templates into valid HTML
2. The development server watches for file changes and triggers browser reload within 500ms
3. Generates valid RSS 2.0 feed from posts with proper pubDate, link, and content fields
4. CLI supports creating a new site (`init`), building the site (`build`), running dev server (`serve`), and creating new posts (`new-post`)
5. Template engine supports layouts, partials, and template inheritance — users can customize without editing code
6. Handles at least 1000 pages and builds the entire site in under 5 seconds
7. Test suite with at least 15 tests covering Markdown parsing, templating, RSS generation, and file watching
8. Documentation includes a quickstart guide and example site that builds successfully
