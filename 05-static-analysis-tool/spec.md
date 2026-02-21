# Static Analysis Tool for Go

## What do you want to build?

Build a static analysis tool in Go that analyzes Go source code for bugs, security vulnerabilities, and code quality issues. The tool should parse Go code, build control flow and data flow graphs, and run configurable analysis passes.

The implementation must include:
- Go source code parsing (using go/ast and go/types)
- Control flow graph (CFG) construction
- Data flow analysis framework (reaching definitions, live variables)
- Analysis passes:
  - Null pointer dereference detection
  - Unused variable/import detection
  - Resource leak detection (unclosed files, connections)
  - SQL injection detection (taint analysis from user input to SQL queries)
  - Race condition detection (goroutine shared variable access without synchronization)
  - Integer overflow detection
- Configurable severity levels (error, warning, info)
- SARIF output format for IDE integration
- CLI with file/directory scanning and ignore patterns
- HTML report generation with source code annotations

## How do you consider the project is success?

1. Correctly identifies null pointer dereferences in a test corpus of 20 Go files with known bugs (>80% recall, <20% false positive rate)
2. Taint analysis correctly traces data flow from `http.Request` to `sql.Query` across function boundaries
3. Resource leak detection finds unclosed `os.File` and `net.Conn` in test cases
4. Race condition detector identifies shared variable access across goroutines (validated against `go vet -race` on 10 test programs)
5. SARIF output is valid and importable by VS Code SARIF viewer
6. Scans the Go standard library `net/http` package without crashing (<30 seconds)
7. False positive rate <30% on a benchmark corpus of real Go projects
8. Test suite with at least 40 test cases (positive and negative cases per analysis pass)
