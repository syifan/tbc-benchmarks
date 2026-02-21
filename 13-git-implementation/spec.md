# Git Implementation

## What do you want to build?

Build a simplified but functional Git implementation in Python that supports the core version control operations: init, add, commit, log, diff, branch, and merge. The implementation should use Git's object model (blobs, trees, commits) and store data in a `.mygit` directory using content-addressable storage with SHA-1 hashing, similar to how Git works internally.

The implementation must include:
- Repository initialization (`init`) — create `.mygit/objects`, `.mygit/refs`, and HEAD
- Staging area (`add`) — hash file contents, store blobs, update index
- Committing (`commit`) — create tree and commit objects, update HEAD
- History (`log`) — traverse commit history, display commit metadata
- Diffing (`diff`) — show differences between working directory and staged/committed versions
- Branching (`branch`, `checkout`) — create branches, switch between them
- Merging (`merge`) — fast-forward and three-way merge with conflict detection
- Proper object storage using SHA-1 hashing and zlib compression
- CLI interface matching Git's command structure

## How do you consider the project is success?

1. Can initialize a repository, add files, and create commits that are stored as proper Git objects (blobs, trees, commits)
2. Object storage uses content-addressable SHA-1 hashing and zlib compression — objects are identical to real Git when possible
3. Branch creation and switching work correctly, updating HEAD and working directory
4. Log command traverses commit history and displays commit hash, author, date, and message
5. Diff shows line-by-line changes between working directory and staged/last commit
6. Merge performs fast-forward merges automatically and detects conflicts in three-way merges
7. Test suite with at least 18 tests covering init, add, commit, branching, merging, and diff scenarios
8. Can perform a realistic workflow: init, add multiple files, commit, create branch, make changes, merge back
