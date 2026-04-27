# MiniC Compiler

A compiler for a subset of the C programming language that generates LLVM IR, built as a deep-dive into systems software and compiler internals.

---

## Motivation

I became interested in how compilers like NVIDIA's PTX compiler work under the hood — how source code is transformed into low-level instructions and eventually executed efficiently on hardware.

To better understand that pipeline from scratch, I started studying compiler design concepts and implementing core compiler components including lexical analysis, parsing, AST construction, semantic analysis, and intermediate representation generation.

This project serves as both a learning project and a practical implementation of compiler construction concepts inspired by academic compiler design techniques and LLVM-based compilation workflows.

---

## Features

- Lexical analysis for MiniC tokenization
- Recursive descent parsing with operator precedence handling
- Abstract Syntax Tree (AST) generation
- Semantic analysis using scoped symbol tables
- LLVM IR generation
- Support for:
  - variables and expressions
  - conditional statements (`if/else`)
  - loops (`while`)
  - functions and recursion
- Test cases for validating parser and code generation behavior

---

## Compiler Pipeline

```text
MiniC Source Code
        ↓
      Lexer
        ↓
      Tokens
        ↓
      Parser
        ↓
        AST
        ↓
 Semantic Analysis
        ↓
   LLVM IR Generation
        ↓
     Executable

     ## Repository Structure

```text
minic-compiler/
│
├── Bonus/                     # Additional experimental features
│
├── expression testcases/      # Expression evaluation test cases
│
├── testcases/                 # Compiler test programs
│
├── MiniC.g4                   # Grammar definition
├── MiniCParser.cpp            # Parser implementation
├── MiniCLexer.cpp             # Lexer implementation
├── MiniCBuildASTVisitor.h     # AST builder
├── symboltable.h              # Symbol table implementation
├── ast.h                      # AST node definitions
├── main.cpp                   # Compiler entry point
│
├── stdlib.c                   # Runtime support library
│
├── README.md                  # Project documentation
└── TODO.md                    # Planned improvements
```
