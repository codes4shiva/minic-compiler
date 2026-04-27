# MiniC Compiler — Study & Reference Implementation

This repository contains a compiler for a subset of the C programming language,
using LLVM for code generation.

> **Note:** This is a reference/study implementation. I am actively studying
> compiler internals — lexing, parsing, AST construction, IR generation, and
> code optimization — as part of my preparation for systems software engineering.
> Original implementation credit: [swetanjal/MiniC-Compiler](https://github.com/swetanjal/MiniC-Compiler)

## What I'm Learning From This

- How a hand-written lexer tokenizes C-like source code
- Recursive-descent parsing and AST construction
- LLVM IR generation using the LLVM toolchain
- Control flow graphs, basic blocks, and SSA form
- How compilers like Clang/PTX map high-level code to machine instructions

## Project Structure

- `src/` — Lexer, Parser, AST nodes
- `codegen/` — LLVM IR code generation
- `examples/` — Sample MiniC programs

## Build Instructions

```bash
mkdir build && cd build
cmake ..
make
```

## Why This Matters to Me

I'm deeply interested in how compilers work at a systems level — particularly
how GPU compilers like NVIDIA's PTX compiler translate high-level constructs
into efficient machine code. Understanding the full pipeline from source →
IR → assembly is foundational to that goal.
