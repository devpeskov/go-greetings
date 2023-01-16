## Example usage:

- Init new module: `go mod init`:
  ```
  mkdir hello
  cd hello
  go mod init example/name
  ```
- Create `hello.go`, with the following content:
  ```
  package main

  import (
    "fmt"
    "github.com/devpeskov/go_greetings"
  )

  func main() {
    // Get a greeting message and print it.
    message := go_greetings.Hello("Nikolay")
    fmt.Println(message)
  }
  ```
- Get remote-module:
  ```
  go mod tidy
  // or
  go get github.com/devpeskov/go_greetings
  ```
- Run: `go run .`
