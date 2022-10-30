# Introduction

Go is a compiled and static typed programming language.

## Many features

- built in concurrent programming support
  - goroutines and starting a new goroutine
  - `channels` and `select` mechanisms to do synchroniztions between goroutines
- polymorphism through interfaces.
- pointers
- function closures
- deferred function calls
- methods
- type embedding
- type deduction
- memory safety
- automatic garbage collection
- great cross-platform compatibility (making binaries for windows on linus or mac environment and vice versa)
- custom generics

## Some more highlights

- Syntax is simple, clean
- Great set of standard code packages.
- Active community

Go also have many features as that of dynamic script languages. Go owns both the strictness and flexibility of the dynamic languages.

Most popular go compiler is `gc` -> go compiler. Go team also maintains a second compiler -> `gccgo`. It is less popular than `gc`. 

`gc` is provided in Go toolchain (a set of tools for Go development maintained by Go team). It also supports cross-platform compilation. For example, we can build a Windows executable on a linux OS, and vice versa.

### Note: 
Compilation time is fast compared to other languages. 

- Advantages of Go executables: 
  - small memory footprint
  - fast code execution
  - short warm-up duration



