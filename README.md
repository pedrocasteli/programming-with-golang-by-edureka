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
