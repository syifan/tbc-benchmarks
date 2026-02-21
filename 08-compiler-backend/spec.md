# Compiler Backend

## What do you want to build?

Build a compiler backend in Rust that takes a simple high-level IR (intermediate representation) and produces optimized x86-64 machine code. The backend should support a C-like input language and generate executables that run on Linux.

The implementation must include:
- Input IR: SSA (Static Single Assignment) form with basic types (i32, i64, f64, bool, pointers)
- IR parser (text format) and in-memory representation
- Optimization passes:
  - Dead code elimination
  - Constant folding and propagation
  - Common subexpression elimination
  - Loop-invariant code motion
  - Strength reduction
- Register allocation: linear scan or graph coloring
- x86-64 code generation: arithmetic, comparisons, branches, function calls (System V AMD64 ABI)
- Stack frame management and calling convention compliance
- ELF object file output (linkable with system linker)
- A simple frontend that compiles a C-subset language to the IR (variables, functions, if/else, while, arrays, structs)

## How do you consider the project is success?

1. Compile and correctly execute 20 test programs covering: arithmetic, control flow, recursion, arrays, structs, function calls
2. Fibonacci(40) computed correctly and within 2x of GCC -O1 performance
3. Register allocation produces code with <10% spill rate on typical functions
4. Dead code elimination removes all provably dead instructions (validated on 10 test cases)
5. Generated ELF objects link successfully with `ld` and produce working executables
6. Function calls follow System V AMD64 ABI — interop with C functions (printf, malloc) works
7. Constant folding evaluates `3 + 4 * 2` at compile time (verified via IR dump)
8. Test suite with at least 40 tests covering parsing, optimization passes, codegen, and end-to-end execution
