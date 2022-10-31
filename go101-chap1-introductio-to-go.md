# Introduction

Go is a compiled and static typed programming language.

## Many features

- built in concurrent programming support
  - goroutines and starting a new goroutine
  - `channels` and `select` mechanisms to do synchronizations between goroutines
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

- Syntax is simple and clean
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

- Go toolchain now supports modules to manage the project dependencies.

`pkg` -> store cached version of Go modules (collection of Go packages) depended by local go projects.

`GOBIN` -> env variable which controls where the Go program binary files are generated.

```go
package main // specifies the package name.

func main() {

}
```

`go run` -> good for small projects. Not recommended to compile and run large Go projects. Use `go build` or `go install` for large projects and then run the executable binary files instead.

`go mod init` -> to generate a `go.mod` file which is located in the root folder of the project. `go.mod` is needed for a project supporting the go modules.

source files starting with `_` or `.` are ignored by Go toolchain.

`go fmt` -> format go source code with consistent coding style.

`go test` -> command to run tests and benchmarks.

`go doc` -> to view go documentation in terminal windows.

`go mod tidy` -> add missing module dependencies into and remove unused module dependencies from the `go.mod` file by analyzing the source code of the project.

`go get` -> add / upgrade / downgrade / remove a single dependency. Used less frequently than `go mod tidy`

`go install` -> to install the latest version of a third-party go-program. E.g. `go install example.com/program@latest`

[refer this to learn more on commands](https://pkg.go.dev/cmd/go)
