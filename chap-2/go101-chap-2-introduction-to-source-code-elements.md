```go
package main // specify the source file's package

import "math/rand" // import a standard package

const MaxRnd = 16 // a named constant declaration

// A function declaration
/*
 StatRandomNumbers produces a certain number of
 non-negative random integers which are less than
 MaxRnd, then counts and returns the numbers of
 small and large ones among the produced randoms.
 n specifies how many randoms to be produced.
*/
func StatRandomNumbers(n int) (int, int) {
	// Declare two variables (both as 0).
	var a, b int
	// A for-loop control flow.
	for i := 0; i < n; i++ {
		// An if-else control flow.
		if rand.Intn(MaxRnd) < MaxRnd/2 {
			a = a + 1
		} else {
			b++ // same as: b = b + 1
		}
	}
	return a, b // this function return two results
}

// "main" function is the entry function of a program.
func main() {
	var num = 100
	// Call the declared StatRandomNumbers function.
	x, y := StatRandomNumbers(num)
	// Call two built-in functions (print and println).
	print("Result: ", x, " + ", y, " = ", num, "? ")
	println(x+y == num)
}
```

to run this basic-code-element-demo, use command

`go run basic-code-element-demo.go`

## Basic Types and Basic Value literals:

- Types can be imagined as templates for values.
- Value can be imagined as instances of types.

### Built-in basic types in Go

- `bool` - true or false - one boolean built-in type.
- `int8, unit8, int16, unit16, int32, unit32, int64, unit64, int, unint` and `uintptr` - 11 - built in integer type.
- `float32, float64` - 2 built-in floating point numeric type.
- `complex64, complex128` - 2 built-in complex numeric type.
- `string` - one built-in string type.

#### Note:

Go also support two built-in type aliases.

- `byte` for `uint8` -> they can be viewed as the same type.
- `rune` for `int32` -------------------"-------------------

u - unsigned -> values are always non-negative (positive)

`uint8` -> the number at the end represents the number of bits it occupies in the memory, (2^8-1)

`int8` -> similarly for int8 ranges from -128 (-2^7) to 127 (2^7-1)

## Zero Values

- boolean - always false
- numeric type - always 0, depending upon the type, the size might vary
- string - '' - empty string


