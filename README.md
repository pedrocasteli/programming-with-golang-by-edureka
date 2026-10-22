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
