# Programming with Golang

This course was taught by Edureka, on the Coursera platform.

[Link to course](https://www.coursera.org/learn/programming-with-golang)

## Golang origin

- The development of Go began on **September 2007** and was officially announced on **November 2009**.
- The first version of Go was **go1**, released in March 28, 2012.
- The current version of Go, at the time of writing this file, is **go1.27.0**, released in August 19, 2026.

## Packages and import

- Every **Go** program is made of **packages**.
- Programs run in the **main package** of a **Go** program.
- Package statements should always be the first line of any **Go** source file.
- A **Go** program is incomplete without a **main** package.
- Each **Go** source file must declare its package at the top of the file.
- The package declaration specifies the name of the package to which the file belongs.
- Package names should be lowercase, and short but meaningful

- `import` is a statement that is used to bring in the capabilities of an existing package into our code.
- We can access the exported identifiers (functions, variables and types) of these packages.
- Exported identifiers are the ones that start with an uppercase letter.

- `main` is a special package name that is used for executable programs.
- An executable program **must have** a `main()` function.
- Packages can have an `init()` function that is executed before the `main()` function.
- It's often used for package-level setup, such as initializing variables or establishing connections.

## Data Types

- Numeric Type: `int`, `float` and `complex`
- Text Type: `string`
- Boolean Type: `bool`
- Composite Type: `array`, `slices`, `maps`, `struct`, `pointer`

### Numeric Types

- `int`: The `int` type represents signed integers. The size of `int` depends onn the architecture and is either 32 or 64 bits.
- `int8`, `int16`, `int32`, `int64`: These are signed integer types with specific sizes (8, 16, 32 and 64 bits, respectively)
- `uint`: The `uint` typesd represents unsigned integers. Like `int`, its size varies with the architecture.
- `uint8`, `uint16`, `uint32`, `uint64`: These are unsigned integer types with specific sizes (8, 16, 32 and 64 bits, respectively)
- `float32`: Represents 32-bit floating-point numbers.
- `float64`: Represents 64-bit floating-point numbers (double precision).
- `complex64`, `complex128`: These types represent complex numbers with 64-bit or 128-bit components, respectively.

### Strings

- Strings in **Go** are immutable. Once created, they can't be modified.
- We can concatenate strings using the `+` operator.

### Boolean Type

- Represents **only one bit** of information. Either 0 or 1, or `true` or `false`.
- They're not converted implicitly or explicitly to any other type.

### Constants

- They are created using the `const` keyword.
- A `const` statement can appear anywhere a variable statement can.
- We can declare them for primitive data types:

```
const Greeting = "Hello, there"
const IsReady = true
```

- The `iota` identifier is used within a `const` declaration to create a sequence of values.
- It is used to **simplify** definitions of incrementing numbers

```
const (
    Red = iota
    Green
    Blue
)
```

### Goto Statements

It is a control flow statement that allows us to unconditionally jump to a labeled section of your code. However, its use is discouraged in modern programming languages becasue it can lead to complex and hard-to-understand code. In most cases, structered control flow constructs and conditional statements should be preferred over `goto`.

### Defer Statements - I

- It's used to schedule a function call to be executed when the surrounding function returns.
- It's commonly used for tasks such as resource cleanup, closing files, releasing locks, and ensuring that certain operations are performed just before a function returns.

```
package main
import (
    "fmt"
    "os"
)

func main() {
    file, err := os.Open("example.txt")

    if err != nil {
        fmt.Println("Error: ", err)
        return
    }

    defer file.Close()
}
```

#### Panic

- The `panic` function is used to trigger a panic or runtime error explicitly.
- When a `panic` occurs, all defered functions are executed.
- The program exits with an error message, including the panic value, which can be of any type.

```
func doSomething() {
    if someCondition {
        panic("An error occured")
    }
    // Rest of the code
}
```

#### Recover

- The `recover` function is used to catch and handle panics.
- It's only valid, and should only be called in, a `defer` function.
- When `recover` is called and there is a `panic` in progress, it stops the `panic` and returns the value that was passed to the `panic` function
