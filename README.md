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
    "log"

    "github.com/devpeskov/go_greetings"
  )

  func main() {
    // Set properties of the predefined Logger, including
    // the log entry prefix and a flag to disable printing
    // the time, source file, and line number.
    log.SetPrefix("greetings: ")
    log.SetFlags(0)

    // uncomment for check error handler
    // message, err := go_greetings.Hello("")
    message, err := go_greetings.Hello("Kolya")

    if err != nil {
      log.Fatal(err)
    }

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
