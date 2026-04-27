# MiniC Compiler

A compiler for a subset of the C programming language that generates LLVM IR,
built as a deep-dive into systems software and compiler internals.

## Motivation
I got interested in how compilers like NVIDIA's PTX compiler work under the hood —
how source code becomes GPU instructions. To understand that pipeline from scratch,
I started studying and implementing compiler components: lexers, parsers, ASTs,
and IR generation.

This project is my working reference as I learn. Code is based on academic
compiler construction techniques (Dragon Book, LLVM tutorial).

## What This Implements
- Hand-written lexer for C-subset tokenization
- Recursive descent parser with operator precedence
- AST construction and semantic analysis with scoped symbol tables  
- LLVM IR code generation via LLVM toolchain
- Control flow: if/else, while loops, functions, recursion

## Pipeline
